---
description: Un'azione personalizzata può chiamare una funzione definita in una libreria a collegamento dinamico (DLL) scritta in C o C++.
ms.assetid: 605c7b97-70bd-467a-9438-47b05d8b6b5d
title: Dynamic-Link librerie (Windows installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcd2548851dcef4dcf08c53f168ec0f6b43ee036a1c250f9f65f072427a19e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378263"
---
# <a name="dynamic-link-libraries-windows-installer"></a>Dynamic-Link librerie (Windows installer)

Un'azione personalizzata può chiamare una funzione definita in una libreria a collegamento dinamico (DLL) scritta in C o C++. La DLL può esistere come file installato durante l'installazione corrente o come flusso binario temporaneo proveniente dalla tabella [binaria](binary-table.md) del database di installazione.

Si noti che qualsiasi funzione chiamata, incluse le azioni personalizzate nelle DLL, deve specificare la \_ \_ convenzione di chiamata stdcall. Ad esempio, per chiamare CustomAction usare quanto segue.


```C++
#include <windows.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



Per altre informazioni, vedere Accesso alla sessione del programma di [installazione corrente dall'interno di un'azione personalizzata](accessing-the-current-installer-session-from-inside-a-custom-action.md)

I tipi seguenti di azioni personalizzate chiamano una libreria a collegamento dinamico.



| Tipo di azione personalizzata                                 | Descrizione                               |
|----------------------------------------------------|-------------------------------------------|
| [Tipo di azione personalizzata 1](custom-action-type-1.md)   | File DLL archiviato in un flusso di tabella binario. |
| [Tipo di azione personalizzata 17](custom-action-type-17.md) | File DLL installato con un prodotto.        |



 

> [!Note]  
> Per usare COM è necessario chiamare [**CoInitializeEx nell'azione**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) personalizzata. Non uscire se si trova che il thread è già stato inizializzato. Ad esempio, il thread viene inizializzato in un'installazione per computer, ma non in un'installazione per utente.

 

Per [un riepilogo di tutti](summary-list-of-all-custom-action-types.md) i tipi di azioni personalizzate e del modo in cui vengono codificate nella tabella [CustomAction,](customaction-table.md)vedere Elenco di riepilogo di tutti i tipi di azioni personalizzate .

 

 
