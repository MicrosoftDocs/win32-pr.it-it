---
title: Generazione dei file stub
description: Dopo aver definito l'interfaccia client/server, in genere si sviluppano i file di origine client e server.
ms.assetid: e4d08bee-ab9a-4426-a1af-72a7d763797f
keywords:
- RPC (Remote Procedure Call), attività, generazione di file stub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e092663711be60a3a0dc0dd8a4e99c0fa92a3ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856069"
---
# <a name="generating-the-stub-files"></a><span data-ttu-id="bfa21-104">Generazione dei file stub</span><span class="sxs-lookup"><span data-stu-id="bfa21-104">Generating the Stub Files</span></span>

<span data-ttu-id="bfa21-105">Dopo aver definito l'interfaccia client/server, in genere si sviluppano i file di origine client e server.</span><span class="sxs-lookup"><span data-stu-id="bfa21-105">After defining the client/server interface, you usually develop your client and server source files.</span></span> <span data-ttu-id="bfa21-106">Usare quindi un singolo makefile per generare lo stub e i file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="bfa21-106">Next use a single makefile to generate the stub and header files.</span></span> <span data-ttu-id="bfa21-107">Compilare e collegare le applicazioni client e server.</span><span class="sxs-lookup"><span data-stu-id="bfa21-107">Compile and link the client and server applications.</span></span> <span data-ttu-id="bfa21-108">Tuttavia, se si tratta della prima esposizione all'ambiente di elaborazione distribuita, potrebbe essere necessario richiamare il compilatore MIDL ora per vedere quali MIDL genera prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="bfa21-108">However, if this is your first exposure to the distributed computing environment, you may want to invoke the MIDL compiler now to see what MIDL generates before you continue.</span></span> <span data-ttu-id="bfa21-109">Il compilatore MIDL (Midl.exe) viene installato automaticamente quando si installa Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="bfa21-109">The MIDL compiler (Midl.exe) is automatically installed when you install the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="bfa21-110">Quando si compilano questi file, assicurarsi che Hello. idl e Hello. ACF si trovino nella stessa directory.</span><span class="sxs-lookup"><span data-stu-id="bfa21-110">When you compile these files, make sure that Hello.idl and Hello.acf are in the same directory.</span></span> <span data-ttu-id="bfa21-111">Il comando seguente genererà il file di intestazione Hello. h e gli stub client e server, Hello \_ c. c e Hello \_ s.c.</span><span class="sxs-lookup"><span data-stu-id="bfa21-111">The following command will generate the header file Hello.h, and the client and server stubs, Hello\_c.c and Hello\_s.c.</span></span>

<span data-ttu-id="bfa21-112">**MIDL Hello. idl**</span><span class="sxs-lookup"><span data-stu-id="bfa21-112">**midl hello.idl**</span></span>

<span data-ttu-id="bfa21-113">Si noti che Hello. h contiene i prototipi di funzione per HelloProc e Shutdown, nonché le dichiarazioni con prototipo per due funzioni di gestione della memoria, l' **\_ utente MIDL \_ allocate** e l' **\_ utente MIDL \_ Free**.</span><span class="sxs-lookup"><span data-stu-id="bfa21-113">Notice that Hello.h contains function prototypes for HelloProc and Shutdown, as well as forward declarations for two memory management functions, **midl\_user\_allocate** and **midl\_user\_free**.</span></span> <span data-ttu-id="bfa21-114">Queste due funzioni vengono fornite nell'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="bfa21-114">You will provide these two functions in the server application.</span></span> <span data-ttu-id="bfa21-115">Se i dati sono stati trasmessi dal server al client (tramite un \[  \] parametro out), è necessario fornire anche queste due funzioni di gestione della memoria nell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="bfa21-115">If data were being transmitted from the server to the client (by means of an \[**out**\] parameter) you would also need to provide these two memory management functions in the client application.</span></span>

<span data-ttu-id="bfa21-116">Si notino le definizioni per la variabile di handle globale, Hello \_ IfHandle e i nomi di handle dell'interfaccia client e server, Hello \_ V1 \_ 0 \_ c \_ ifspec e Hello \_ V1 \_ 0 \_ s \_ ifspec.</span><span class="sxs-lookup"><span data-stu-id="bfa21-116">Note the definitions for the global handle variable, hello\_IfHandle, and the client and server interface handle names, hello\_v1\_0\_c\_ifspec and hello\_v1\_0\_s\_ifspec.</span></span> <span data-ttu-id="bfa21-117">Le applicazioni client e server utilizzeranno i nomi di handle di interfaccia nelle chiamate di run-time.</span><span class="sxs-lookup"><span data-stu-id="bfa21-117">The client and server applications will use the interface handle names in run-time calls.</span></span>

<span data-ttu-id="bfa21-118">A questo punto, non è necessario eseguire alcuna operazione con i file stub Hello \_ c. c e Hello \_ s.c.</span><span class="sxs-lookup"><span data-stu-id="bfa21-118">At this point, you don't need to do anything with the stub files Hello\_c.c and hello\_s.c.</span></span>

``` syntax
/*file: hello.h */
/* this ALWAYS GENERATED file contains the definitions for the interfaces */
/* File created by MIDL compiler version 3.00.06 
/* at Tue Feb 20 11:33:32 1996 */
/* Compiler settings for hello.idl:
    Os, W1, Zp8, env=Win32, ms_ext, c_ext
    error checks: none */
//@@MIDL_FILE_HEADING(  )
#include "Rpc.h"
#include "rpcndr.h"
 
#ifndef __hello_h_
#define __hello_h_
 
#ifdef __cplusplus
extern "C"{
#endif 
 
/* Forward Declarations */ 
 
void __RPC_FAR * __RPC_USER MIDL_user_allocate(size_t);
void __RPC_USER MIDL_user_free( void __RPC_FAR * ); 
 
#ifndef __hello_INTERFACE_DEFINED__
#define __hello_INTERFACE_DEFINED__
 
/****************************************
 * Generated header for interface: hello
 * at Tue Feb 20 11:33:32 1996
 * using MIDL 3.00.06
 ****************************************/
/* [implicit_handle][version][uuid] */ 
 
            /* size is 0 */
void HelloProc( 
    /* [string][in] */ unsigned char __RPC_FAR *pszString);
    /* size is 0 */
void Shutdown( void);
extern handle_t hello_IfHandle;
 
extern RPC_IF_HANDLE hello_v1_0_c_ifspec;
extern RPC_IF_HANDLE hello_v1_0_s_ifspec;
#endif /* __hello_INTERFACE_DEFINED__ */
 
/* Additional Prototypes for ALL interfaces */
/* end of Additional Prototypes */
#ifdef __cplusplus
}
#endif
#endif
```

 

 




