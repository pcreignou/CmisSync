SUBDIRS = Pixmaps

ASSEMBLY = CmisSync
TARGET = exe

ASSEMBLY_INFO_SOURCE = Defines.cs

LIBS = $(REF_CMISSYNC) $(LOG4NET_LIBS) $(NOTIFY_SHARP_LIBS)

SOURCES =  \
	../AboutController.cs \
	../CertPolicyHandler.cs \
	../ControllerBase.cs \
	../EditController.cs \
	../Program.cs \
	../Properties/Resources.Designer.cs \
	../SetupController.cs \
	../StatusIconController.cs \
	../Windows/FolderTreeMVC/IgnoredFolderLoader.cs \
	../Windows/FolderTreeMVC/LoadingStatusModel.cs \
	../Windows/FolderTreeMVC/LocalFolderLoader.cs \
	../Windows/FolderTreeMVC/NodeLoader.cs \
	../Windows/FolderTreeMVC/NodeModel.cs \
	../Windows/FolderTreeMVC/NodeModelUtils.cs \
	About.cs \
	CertPolicyWindow.cs \
	CmisTree/CmisTreeStore.cs \
	CmisTree/StatusCellRenderer.cs \
	Controller.cs \
	Edit.cs \
	Setup.cs \
	SetupWindow.cs \
	Spinner.cs \
	StatusIcon.cs \
	UI.cs \
	UIHelpers.cs \
	Utils.cs

RESOURCES = $(RESOURCES_RESOURCES)

RESOURCES_RESX = $(wildcard $(srcdir)/../Properties/*.resx)
RESOURCES_RESOURCES = $(addprefix CmisSync.,$(patsubst %.resx,%.resources,$(notdir $(RESOURCES_RESX))))

CmisSync.%.resources: $(srcdir)/../Properties/%.resx
	resgen2 $< $@

bin_SCRIPTS = dataspacesync

Applicationsdir = $(datadir)/applications
dist_Applications_DATA = dataspacesync.desktop 

EXTRA_DIST = README.md

include $(top_srcdir)/build/build.mk

CLEANFILES += $(RESOURCES_RESOURCES)
