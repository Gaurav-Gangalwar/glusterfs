xlator_LTLIBRARIES = server.la
xlatordir = $(libdir)/glusterfs/$(PACKAGE_VERSION)/xlator/nfs
nfsrpclibdir = $(top_srcdir)/xlators/nfs/lib/src
server_la_LDFLAGS = -module -avoidversion
server_la_SOURCES = nfs.c nfs-common.c nfs-fops.c nfs-inodes.c nfs-generics.c mount3.c nfs3-fh.c nfs3.c nfs3-helpers.c $(nfsrpclibdir)/auth-null.c  $(nfsrpclibdir)/auth-unix.c $(nfsrpclibdir)/msg-nfs3.c  $(nfsrpclibdir)/rpc-socket.c  $(nfsrpclibdir)/rpcsvc-auth.c  $(nfsrpclibdir)/rpcsvc.c  $(nfsrpclibdir)/xdr-nfs3.c  $(nfsrpclibdir)/xdr-rpc.c
server_la_LIBADD = $(top_builddir)/libglusterfs/src/libglusterfs.la

noinst_HEADERS = nfs.h nfs-common.h nfs-fops.h nfs-inodes.h nfs-generics.h mount3.h nfs3-fh.h nfs3.h nfs3-helpers.h nfs-mem-types.h $(nfsrpclibdir)/xdr-rpc.h $(nfsrpclibdir)/msg-nfs3.h $(nfsrpclibdir)/xdr-common.h $(nfsrpclibdir)/xdr-nfs3.h $(nfsrpclibdir)/rpc-socket.h $(nfsrpclibdir)/rpcsvc.h
AM_CFLAGS = -fPIC -D_FILE_OFFSET_BITS=64 -D_GNU_SOURCE -Wall -D$(GF_HOST_OS)\
	-I$(top_srcdir)/libglusterfs/src -shared -nostartfiles $(GF_CFLAGS)\
	-I$(nfsrpclibdir) -L$(xlatordir)/ -I$(CONTRIBDIR)/rbtree

CLEANFILES =
