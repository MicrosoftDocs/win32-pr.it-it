---
description: Un'azione personalizzata può chiamare una funzione definita in una libreria a collegamento dinamico (DLL) scritta in C o C++.
ms.assetid: 605c7b97-70bd-467a-9438-47b05d8b6b5d
title: Librerie di Dynamic-Link (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f9ff0113d97d219220a4f42030c1563f16ce7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050147"
---
# <a name="dynamic-link-libraries-windows-installer"></a>Librerie di Dynamic-Link (Windows Installer)

Un'azione personalizzata può chiamare una funzione definita in una libreria a collegamento dinamico (DLL) scritta in C o C++. La DLL può esistere come file installato durante l'installazione corrente o come flusso binario temporaneo originato dalla [tabella binaria](binary-table.md) del database di installazione.

Si noti che tutte le funzioni chiamate, incluse le azioni personalizzate nelle DLL, devono specificare la \_ \_ convenzione di chiamata stdcall. Per chiamare CustomAction, ad esempio, usare il comando seguente.


```C++
#include <windows.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



Per altre informazioni, vedere [accesso alla sessione corrente del programma di installazione dall'interno di un'azione personalizzata](accessing-the-current-installer-session-from-inside-a-custom-action.md)

I tipi seguenti di azioni personalizzate chiamano una libreria a collegamento dinamico.



| Tipo di azione personalizzata                                 | Descrizione                               |
|----------------------------------------------------|-------------------------------------------|
| [Tipo di azione personalizzata 1](custom-action-type-1.md)   | File DLL archiviato in un flusso di tabella binario. |
| [Tipo di azione personalizzata 17](custom-action-type-17.md) | File DLL installato con un prodotto.        |



 

> [!Note]  
> Per usare COM è necessario chiamare [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) nell'azione personalizzata. Non uscire se si rileva che il thread è già stato inizializzato. Ad esempio, il thread viene inizializzato in un'installazione per computer, ma non in un'installazione per utente.

 

Vedere l' [elenco riepilogativo di tutti i tipi di azione personalizzati](summary-list-of-all-custom-action-types.md) per un riepilogo di tutti i tipi di azioni personalizzate e il modo in cui vengono codificati nella [tabella CustomAction](customaction-table.md).

 

 
