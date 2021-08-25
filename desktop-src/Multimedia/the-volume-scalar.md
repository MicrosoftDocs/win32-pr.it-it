---
title: Scalare del volume
description: Scalare del volume
ms.assetid: a9fe2c35-9109-4697-9ffa-a31debbe72c8
keywords:
- MIDI (Musical Instrument Digital Interface), scalare di volumi
- MIDI (Musical Instrument Digital Interface),volume scalare
- MIDI Mapper, scalare di volumi
- scalare di volumi
- Mapper MIDI, regolazione dei livelli di output
- regolazione dei livelli di output
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7710e8e3ceb8079f04ac97bfcce8c91c6c74aa60452c220166e358a87939848
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804947"
---
# <a name="the-volume-scalar"></a>Scalare del volume

Lo scopo dello scalare di volume è consentire modifiche tra i livelli di output relativi di patch diverse in un sintetizzatore. Ad esempio, se la patch per bassi in un sintetizzatore è troppo alta rispetto alla patch del piano, è possibile modificare la mappa di configurazione per ridimensionare il volume dei bassi o aumentare il volume del piano.

Lo scalare di volume specifica un valore percentuale per la modifica di tutti i messaggi del controller del volume principale MIDI che seguono un messaggio di modifica del programma associato. Ad esempio, se il valore scalare del volume è 50%, MIDI Mapper modifica i messaggi del controller midi principale del volume, come illustrato nella figura seguente.

![immagine midi mapper](images/mmap-a04.gif)

 

 




