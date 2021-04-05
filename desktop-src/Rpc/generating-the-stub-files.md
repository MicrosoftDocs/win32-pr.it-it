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
# <a name="generating-the-stub-files"></a>Generazione dei file stub

Dopo aver definito l'interfaccia client/server, in genere si sviluppano i file di origine client e server. Usare quindi un singolo makefile per generare lo stub e i file di intestazione. Compilare e collegare le applicazioni client e server. Tuttavia, se si tratta della prima esposizione all'ambiente di elaborazione distribuita, potrebbe essere necessario richiamare il compilatore MIDL ora per vedere quali MIDL genera prima di continuare. Il compilatore MIDL (Midl.exe) viene installato automaticamente quando si installa Platform Software Development Kit (SDK).

Quando si compilano questi file, assicurarsi che Hello. idl e Hello. ACF si trovino nella stessa directory. Il comando seguente genererà il file di intestazione Hello. h e gli stub client e server, Hello \_ c. c e Hello \_ s.c.

**MIDL Hello. idl**

Si noti che Hello. h contiene i prototipi di funzione per HelloProc e Shutdown, nonché le dichiarazioni con prototipo per due funzioni di gestione della memoria, l' **\_ utente MIDL \_ allocate** e l' **\_ utente MIDL \_ Free**. Queste due funzioni vengono fornite nell'applicazione server. Se i dati sono stati trasmessi dal server al client (tramite un \[  \] parametro out), è necessario fornire anche queste due funzioni di gestione della memoria nell'applicazione client.

Si notino le definizioni per la variabile di handle globale, Hello \_ IfHandle e i nomi di handle dell'interfaccia client e server, Hello \_ V1 \_ 0 \_ c \_ ifspec e Hello \_ V1 \_ 0 \_ s \_ ifspec. Le applicazioni client e server utilizzeranno i nomi di handle di interfaccia nelle chiamate di run-time.

A questo punto, non è necessario eseguire alcuna operazione con i file stub Hello \_ c. c e Hello \_ s.c.

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

 

 




