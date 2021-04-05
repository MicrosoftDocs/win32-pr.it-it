---
title: Voci di sistema per compresser, decompressori e renderer
description: Voci di sistema per compresser, decompressori e renderer
ms.assetid: b27bbd5b-a218-49bb-b179-b24ce39869a1
keywords:
- Video per Windows (VFW), voci di sistema compressore
- VFW (video per Windows), voci di sistema compressore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46d9c6fd8974511698bcb687c580e68be3757ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713300"
---
# <a name="system-entries-for-compressors-decompressors-and-renderers"></a>Voci di sistema per compresser, decompressori e renderer

Il sistema usa le voci nel registro di sistema per trovare i driver VCM. Queste voci sono costituite da codici a 2 4 caratteri separati da un punto. Il primo codice di quattro caratteri viene definito dal sistema e può essere uno dei seguenti:



| Codice a quattro caratteri | Descrizione                               |
|---------------------|-------------------------------------------|
| VIDC              | Identifica i comprimeri e i decompressori. |
| VIDS              | Identifica i renderer del flusso video.        |
| TXTS              | Identifica i renderer del flusso di testo.         |
| "AUDS"              | Identifica i gestori del flusso audio.         |



 

I renderer personalizzati possono definire i propri codici a quattro caratteri.

Il secondo codice a quattro caratteri viene definito dal driver. In genere, il secondo codice a quattro caratteri corrisponde al tipo di dati che il driver è in grado di gestire.

Quando si apre un driver VCM, un'applicazione specifica il tipo di driver e il tipo di gestore di dati necessari. In genere, queste informazioni provengono dall'intestazione del flusso. Il sistema tenta di aprire il gestore di dati specificato; in caso contrario, il sistema esegue una ricerca nel registro di sistema di un driver con il gestore obbligatorio.

Quando si esegue la ricerca del driver, il sistema tenta di trovare una corrispondenza tra i codici di quattro caratteri specificati per il tipo di driver e il gestore di dati con quelli specificati nella voce del driver. Se, ad esempio, in un'applicazione viene specificato il compressore MSSQ, il sistema cerca nel registro di sistema la voce di driver VIDC. MSSQ. Se non riesce a trovare una corrispondenza, apre ogni driver corrispondente al tipo di driver e ne individua uno in grado di gestire il tipo di dati specificato dall'applicazione. Nell'esempio precedente, se il sistema non è stato in grado di trovare VIDC. MSSQ, apre tutti i driver con il codice a quattro caratteri "VIDC" e ne individua uno in grado di gestire i dati.

 

 




