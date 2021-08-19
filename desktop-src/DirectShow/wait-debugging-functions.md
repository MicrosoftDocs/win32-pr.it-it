---
description: Funzioni di debug in attesa
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Funzioni di debug in attesa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f8f1de3d19ce7408625a5ab42f230d23ce401728e9fa7cf060edae62e19fcfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049201"
---
# <a name="wait-debugging-functions"></a>Funzioni di debug in attesa

Microsoft DirectShow fornisce diverse funzioni per il debug di attese infinite.

Nelle build di vendita al dettaglio, le funzioni [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) e [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) funzionano come le controparti dell'API Windows, **WaitForMultipleObjects** e **WaitForSingleObject**, con intervalli di timeout infiniti.

Nelle build di debug queste funzioni usano un valore di timeout globale. Se il timeout scade, la funzione attiva un'asserzione. La chiave del Registro di sistema seguente specifica il valore di timeout, espresso in millisecondi:

**TIMEOUT DEL COMPUTER LOCALE HKEY \_ \_ \\ <DebugRoot> \\ <Module Name> \\**

dove *<DebugRoot>* è il percorso del Registro di sistema descritto nell'argomento Funzioni di output di [debug](debug-output-functions.md).

Se la chiave non esiste, il valore di timeout viene impostato per impostazione predefinita su INFINITE. È possibile usare la funzione [**DbgSetWaitTimeout per**](dbgsetwaittimeout.md) eseguire l'override della voce del Registro di sistema.



| Funzione                                                       | Descrizione                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [**DbgSetWaitTimeout**](dbgsetwaittimeout.md)                 | Imposta il valore di timeout del debug.                              |
| [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) | Attende la segnalazione di uno o tutti gli oggetti specificati. |
| [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md)       | Attende che un oggetto diventi segnalato.                         |



 

 

 



