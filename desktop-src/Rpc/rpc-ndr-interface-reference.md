---
title: Riferimento all'interfaccia RPC NDR
description: Microsoft RPC NDR supporta attualmente le funzioni e le strutture seguenti
ms.assetid: 2EBB2DD6-60DD-4C9F-9F79-231383B28517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a802720c584d08112c733135c3bb5640e7679c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338398"
---
# <a name="rpc-ndr-interface-reference"></a>Riferimento all'interfaccia RPC NDR

Microsoft RPC NDR supporta attualmente le funzioni e le strutture seguenti:

-   [**\_AddRef CStdStubBuffer**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_addref)
-   [**\_Connessione CStdStubBuffer**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_connect)
-   [**\_CountRefs CStdStubBuffer**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_countrefs)
-   [**\_DebugServerQueryInterface CStdStubBuffer**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_debugserverqueryinterface)
-   [**\_DebugServerRelease CStdStubBuffer**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_debugserverrelease)
-   [**Disconnessione CStdStubBuffer \_**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_disconnect)
-   [**CStdStubBuffer \_ Invoke**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_invoke)
-   [**\_IsIIDSupported CStdStubBuffer**](/windows/desktop/api/RpcProxy/nf-rpcproxy-cstdstubbuffer_isiidsupported)
-   [**CStdStubBuffer \_ QueryInterface**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-cstdstubbuffer_queryinterface)
-   [**\_Proxy AddRef \_ IUnknown**](/windows/desktop/api/unknwnbase/nf-unknwnbase-iunknown_addref_proxy)
-   [**\_Proxy QueryInterface \_ IUnknown**](/windows/desktop/api/unknwnbase/nf-unknwnbase-iunknown_queryinterface_proxy)
-   [**\_Proxy versione \_ IUnknown**](/windows/desktop/api/unknwnbase/nf-unknwnbase-iunknown_queryinterface_proxy)
-   [**NdrAsyncClientCall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrasyncclientcall)
-   [**NdrClearOutParameters**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrclearoutparameters)
-   [**NdrClientCall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrclientcall)
-   [**NdrClientCall2**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrclientcall2)
-   [**NdrConformantArrayUnmarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantarrayunmarshall)
-   [**NdrConformantStringBufferSize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantstringbuffersize)
-   [**NdrConformantStringMarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantstringmarshall)
-   [**NdrConformantStringUnmarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantstringunmarshall)
-   [**NdrContextHandleInitialize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcontexthandleinitialize)
-   [**NdrContextHandleSize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcontexthandlesize)
-   [**NdrContextHandleMemorySize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcontexthandlememorysize)
-   [**NdrConvert**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconvert)
-   [**Versione di NdrCStdStubBuffer \_**](/previous-versions/aa374242(v=vs.80))
-   [**Versione di NdrCStdStubBuffer2 \_**](/previous-versions/aa374240(v=vs.80))
-   [**NdrDllCanUnloadNow**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllcanunloadnow)
-   [**NdrDllGetClassObject**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllgetclassobject)
-   [**NdrDllRegisterProxy**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllregisterproxy)
-   [**NdrDllUnregisterProxy**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrdllunregisterproxy)
-   [**NdrGetUserMarshalInfo**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
-   [**NdrInterfacePointerBufferSize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointerbuffersize)
-   [**NdrInterfacePointerFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointerfree)
-   [**NdrInterfacePointerMarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointermarshall)
-   [**NdrInterfacePointerUnmarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrinterfacepointerunmarshall)
-   [**NdrOleAllocate**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndroleallocate)
-   [**NdrOleFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrolefree)
-   [**NdrPointerBufferSize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointerbuffersize)
-   [**NdrPointerFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointerfree)
-   [**NdrPointerMarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointermarshall)
-   [**NdrPointerUnmarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrpointerunmarshall)
-   [**NdrProxyErrorHandler**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxyerrorhandler)
-   [**NdrProxyFreeBuffer**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxyfreebuffer)
-   [**NdrProxyGetBuffer**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxygetbuffer)
-   [**NdrProxyInitialize**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxyinitialize)
-   [**NdrProxySendReceive**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrproxysendreceive)
-   [**NdrSimpleTypeMarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimpletypemarshall)
-   [**NdrSimpleTypeUnmarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimpletypeunmarshall)
-   [**NdrStubCall2**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrstubcall2)
-   [**NdrStubForwardingFunction**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrstubforwardingfunction)
-   [**NdrStubGetBuffer**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrstubgetbuffer)
-   [**NdrStubInitialize**](/windows/desktop/api/Rpcproxy/nf-rpcproxy-ndrstubinitialize)
-   [**NdrUserMarshalBufferSize**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrusermarshalbuffersize)
-   [**NdrUserMarshalFree**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrusermarshalfree)
-   [**NdrUserMarshalMarshall**](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrusermarshalmarshall)
-   [**\_Descrizione Stub \_ MIDL**](/windows/desktop/api/Rpcndr/ns-rpcndr-midl_stub_desc)
-   [**\_messaggio Stub \_ MIDL**](/windows/desktop/api/Rpcndr/ns-rpcndr-midl_stub_message)
-   [**ProxyFileInfo**](/windows/win32/api/rpcproxy/ns-rpcproxy-proxyfileinfo)
-   [**\_messaggio RPC**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message)

 

 