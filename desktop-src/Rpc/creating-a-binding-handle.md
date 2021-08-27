---
title: Creazione di un handle di associazione
description: Il programma client di un'applicazione distribuita deve creare un handle di associazione che indica alla fase di esecuzione RPC quale server deve essere contattato e come deve essere contattato il server.
ms.assetid: 52c5d0bd-f9b4-4d3f-ac7f-f9b4fb919846
keywords:
- RPC Remote Procedure Call , attività, creazione di un handle di associazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b1d805a765649f640ff10f8cb825264e3402c8938786d183b0be351036c971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101711"
---
# <a name="creating-a-binding-handle"></a>Creazione di un handle di associazione

Il programma client di un'applicazione distribuita deve creare un handle di associazione che indica alla fase di esecuzione RPC quale server deve essere contattato e come deve essere contattato il server.

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



 

 




