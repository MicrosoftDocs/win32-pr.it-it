---
description: Funzioni di debug in attesa
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Funzioni di debug in attesa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f2aabec60a14ff36d74298a21d31c91b4bc6d94
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884031"
---
# <a name="wait-debugging-functions"></a>Funzioni di debug in attesa

Microsoft DirectShow fornisce diverse funzioni per il debug di attese infinite.

Nelle build di vendita al dettaglio, le funzioni [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) e [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) funzionano come le controparti dell'API Windows, **WaitForMultipleObjects** e **WaitForSingleObject**, con intervalli di timeout infiniti.

Nelle build di debug queste funzioni usano un valore di timeout globale. Se il timeout scade, la funzione attiva un'asserzione. La chiave del Registro di sistema seguente specifica il valore di timeout, espresso in millisecondi:

**HKEY \_ LOCAL \_ MACHINE \\ &lt; DebugRoot &gt; \\ <Module Name> \\ TIMEOUT**

dove *&lt; DebugRoot è &gt;* il percorso del Registro di sistema descritto nell'argomento Funzioni di output di [debug](debug-output-functions.md).

Se la chiave non esiste, il valore di timeout viene impostato per impostazione predefinita su INFINITE. È possibile usare la funzione [**DbgSetWaitTimeout per**](dbgsetwaittimeout.md) eseguire l'override della voce del Registro di sistema.



| Funzione                                                       | Descrizione                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [**DbgSetWaitTimeout**](dbgsetwaittimeout.md)                 | Imposta il valore di timeout del debug.                              |
| [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) | Attende la segnalazione di uno o di tutti gli oggetti specificati. |
| [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md)       | Attende che un oggetto diventi segnalato.                         |



 

 

 



