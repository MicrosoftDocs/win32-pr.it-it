---
description: Nei sistemi operativi a 64 bit Windows Installer possibile chiamare azioni personalizzate compilate per sistemi a 32 bit o 64 bit.
ms.assetid: fc370ab4-93f3-4e1e-9468-3454d4fee0be
title: Azioni personalizzate a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fcd804152abd010f985aab3b92c0de73a2744f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756260"
---
# <a name="64-bit-custom-actions"></a>Azioni personalizzate a 64 bit

Nei sistemi operativi a 64 bit Windows Installer possibile chiamare azioni personalizzate compilate per sistemi a 32 bit o 64 bit.

Un'azione personalizzata a 64 bit basata sugli [script](scripts.md) deve essere contrassegnata in modo esplicito come azione personalizzata a 64 bit aggiungendo il bit **msidbCustomActionType64BitScript** al tipo numerico azioni personalizzate nella colonna Type della [tabella CustomAction](customaction-table.md).



| Costante                             | Valore esadecimale | Decimal | Significato                                                           |
|--------------------------------------|-------------|---------|-------------------------------------------------------------------|
| **msidbCustomActionType64BitScript** | 0x0001000   | 4096    | Si tratta di un'azione personalizzata a 64 bit scritta negli [script](scripts.md). |



 

Le azioni personalizzate basate su [file eseguibili](executable-files.md) o [librerie a collegamento dinamico](dynamic-link-libraries.md) che sono state soddisfatte per i sistemi operativi a 64 bit non richiedono l'inclusione di questo bit aggiuntivo nella colonna Type della tabella CustomAction.

 

 



