set(classes
  vtkF3DSplatReader
  vtkQuakeMDLImporter
  )

set(_no_install "")
if(VTK_VERSION VERSION_GREATER_EQUAL 9.2.20220928)
  set(_no_install "NO_INSTALL")
endif()

vtk_module_add_module(f3d::vtkextNative
  ${_no_install}
  FORCE_STATIC
  CLASSES ${classes})
