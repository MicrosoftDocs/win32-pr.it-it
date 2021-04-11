---
title: Creazione di un handle di associazione
description: Il programma client di un'applicazione distribuita deve creare un handle di associazione che indichi il tempo di esecuzione RPC a cui deve essere contattato il server e il modo in cui il server deve essere contattato.
ms.assetid: 52c5d0bd-f9b4-4d3f-ac7f-f9b4fb919846
keywords:
- RPC (Remote Procedure Call), attività, creazione di un handle di associazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eddced351642d916f90cd5c127d0e51b764f7ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044418"
---
# <a name="creating-a-binding-handle"></a>Creazione di un handle di associazione

Il programma client di un'applicazione distribuita deve creare un handle di associazione che indichi il tempo di esecuzione RPC a cui deve essere contattato il server e il modo in cui il server deve essere contattato.

Il frammento di codice seguente illustra un approccio comune alla creazione di un handle di associazione:


```C++
RPC_STATUS status;
unsigned short *StringBinding;
RPC_BINDING_HANDLE BindingHandle;
status = RpcStringBindingCompose(NULL,  // Object UUID
             L"ncacn_ip_tcp",           // Protocol sequence to use
             L"MyServer.MyCompany.com", // Server DNS or Netbios Name
             NULL,
             NULL,
             &StringBinding);
// Error checking ommitted. If no error, we proceed below
status = RpcBindingFromStringBinding(StringBinding, &BindingHandle);

// free string regardless of errors from RpcBindingFromStringBinding
RpcStringFree(&StringBinding);

// Error checking ommitted. If no error, we have a valid binding handle
```



 

 




