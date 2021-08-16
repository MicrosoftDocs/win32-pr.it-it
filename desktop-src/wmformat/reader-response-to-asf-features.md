---
title: Risposta del lettore alle funzionalità di Asf
description: Risposta del lettore alle funzionalità di Asf
ms.assetid: 0cf800ca-63e8-47e2-a2fc-7ba6789fb4bb
keywords:
- Windows Media Format SDK, risposte del lettore alle funzionalità di ASF
- Advanced Systems Format (ASF), risposte del lettore alle funzionalità
- ASF (Advanced Systems Format), risposte del lettore alle funzionalità
- risposte del lettore alle funzionalità di Asf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8b8b64649388af6186155009f2a47b0f2b2c96cc42645e64dbb04f3054d7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084498"
---
# <a name="reader-response-to-asf-features"></a>Risposta del lettore alle funzionalità di Asf

La maggior parte delle funzionalità speciali dei file ASF può essere impostata nei file per interagire con applicazioni di riproduzione personalizzate progettate per gestirle. Tuttavia, alcune delle funzionalità hanno il supporto predefinito nell'oggetto reader.

L'oggetto lettore selezionerà automaticamente i flussi dei set che si escludono a vicenda in base alla velocità in bit. Questo caso speciale viene definito MBR (Multiple Bit Rate). Il flusso selezionato dal lettore è basato sulla velocità in bit del flusso. Il numero di flusso e l'ordine in cui è stato aggiunto all'oggetto di esclusione reciproca non sono rilevanti per la selezione automatica. Se un file include più di un set di flussi che si escludono a vicenda in base alla velocità in bit, il lettore selezionerà i flussi in base al calcolo dell'uso ottimale della larghezza di banda disponibile.

L'esclusione reciproca basata sulla lingua viene impostata usando un'impostazione di output, prima della riproduzione. Se si combinano sia l'esclusione reciproca basata sul linguaggio sia l'esclusione reciproca basata sulla velocità in bit, è necessario raggruppare i flussi che si escludono a vicenda in base alla frequenza di bit in base al linguaggio e quindi fare in modo che i gruppi si escludono a vicenda in base al linguaggio. Il lettore controlla prima la lingua e quindi determina la velocità in bit da usare.

La priorità del flusso viene impostata usando una matrice di record. I record nella matrice sono in ordine di priorità decrescente. L'ultimo flusso nella matrice è il primo che verrà eliminato dal lettore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità dei file ASF**](asf-file-features.md)
</dt> <dt>

[**Esclusione reciproca**](mutual-exclusion.md)
</dt> <dt>

[**Priorità del flusso**](stream-prioritization.md)
</dt> </dl>

 

 




