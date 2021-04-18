---
title: Risposta del lettore alle funzionalità ASF
description: Risposta del lettore alle funzionalità ASF
ms.assetid: 0cf800ca-63e8-47e2-a2fc-7ba6789fb4bb
keywords:
- Windows Media Format SDK, risposte del lettore alle funzionalità ASF
- ASF (Advanced Systems Format), risposte del lettore alle funzionalità
- ASF (formato avanzato dei sistemi), risposte del lettore alle funzionalità
- risposte del lettore alle funzionalità ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291752d2d011fbc8b0a3e5211c5d8926f94b1cbd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298231"
---
# <a name="reader-response-to-asf-features"></a>Risposta del lettore alle funzionalità ASF

La maggior parte delle funzionalità speciali dei file ASF può essere configurata nei file per interagire con le applicazioni di riproduzione personalizzate progettate per gestirle. Tuttavia, alcune funzionalità di includono il supporto incorporato nell'oggetto Reader.

L'oggetto Reader selezionerà automaticamente i flussi dai set che si escludono a vicenda in base alla velocità in bit. Questo caso speciale è noto come velocità in bit multipla (MBR). Il flusso selezionato dal lettore è basato sulla velocità in bit del flusso. Il numero del flusso e l'ordine in cui è stato aggiunto all'oggetto di esclusione reciproca sono irrilevanti per la selezione automatica. Se un file include più di un set di flussi che si escludono a vicenda per velocità in bit, il lettore selezionerà i flussi in base al calcolo del migliore uso della larghezza di banda disponibile.

L'esclusione reciproca basata sulla lingua viene impostata usando un'impostazione di output, prima della riproduzione. Se si combinano sia la lingua che l'esclusione reciproca basata sulla velocità in bit, è necessario raggruppare i flussi che si escludono reciprocamente basati sulla velocità in bit per lingua e quindi rendere i gruppi che si escludono a vicenda in base alla lingua. Il lettore controllerà innanzitutto la lingua e quindi determina la velocità in bit da usare.

La definizione delle priorità del flusso viene impostata tramite una matrice di record. I record nella matrice sono in ordine decrescente di priorità. L'ultimo flusso della matrice è il primo che verrà eliminato dal reader.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità file ASF**](asf-file-features.md)
</dt> <dt>

[**Esclusione reciproca**](mutual-exclusion.md)
</dt> <dt>

[**Assegnazione di priorità al flusso**](stream-prioritization.md)
</dt> </dl>

 

 




