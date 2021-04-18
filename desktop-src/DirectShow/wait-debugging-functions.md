---
description: Funzioni di debug di attesa
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Funzioni di debug di attesa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d2f9f8d40e6b9676426254f0b9165b546dec7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308946"
---
# <a name="wait-debugging-functions"></a>Funzioni di debug di attesa

Microsoft DirectShow fornisce diverse funzioni per il debug di attese infinite.

Nelle compilazioni al dettaglio, le funzioni [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) e [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) funzionano come le controparti API Windows, **WaitForMultipleObjects** e **WaitForSingleObject**, con intervalli di timeout infiniti.

Nelle build di debug queste funzioni usano un valore di timeout globale. Se il timeout scade, la funzione attiva un'asserzione. La seguente chiave del registro di sistema specifica il valore di timeout, in millisecondi:

**\_ \_ \\ <DebugRoot> \\ <Module Name> \\ timeout computer locale HKEY**

dove *<DebugRoot>* è il percorso del registro di sistema descritto nell'argomento [funzioni di output di debug](debug-output-functions.md).

Se la chiave non esiste, per impostazione predefinita il valore di timeout è infinito. È possibile usare la funzione [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) per eseguire l'override della voce del registro di sistema.



| Funzione                                                       | Descrizione                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [**DbgSetWaitTimeout**](dbgsetwaittimeout.md)                 | Imposta il valore di timeout del debug.                              |
| [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) | Attende la segnalazione di qualsiasi (o tutti) degli oggetti specificati. |
| [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md)       | Attende che un oggetto venga segnalato.                         |



 

 

 



