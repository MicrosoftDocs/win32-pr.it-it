---
title: Esclusione reciproca
description: Esclusione reciproca
ms.assetid: 3a3f6763-a241-4bbd-a6e8-62041b05622d
keywords:
- Windows Media Format SDK, esclusione reciproca
- Formato di sistemi avanzati (ASF), esclusione reciproca
- ASF (formato avanzato dei sistemi), esclusione reciproca
- Windows Media Format SDK, l'esclusione reciproca MBR
- ASF (Advanced Systems Format), esclusione reciproca MBR
- ASF (formato avanzato dei sistemi), esclusione reciproca MBR
- Windows Media Format SDK, frequenza a più bit (MBR)
- ASF (Advanced Systems Format), velocità in bit multipla (MBR)
- ASF (formato avanzato dei sistemi), velocità in bit multipla (MBR)
- esclusione reciproca, informazioni
- velocità in bit multipla (MBR), esclusione reciproca
- MBR (frequenza a più bit), esclusione reciproca
- esclusione reciproca, velocità in bit
- esclusione reciproca, lingua
- esclusione reciproca, presentazione
- esclusione reciproca, sconosciuta
- esclusione reciproca, funzionalità
- esclusione reciproca, funzionalità avanzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd00bf5bcb544d2541a6bc5465171fe9bacc1b9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856889"
---
# <a name="mutual-exclusion"></a>Esclusione reciproca

Ogni file ASF contiene uno o più flussi, ognuno dei quali contiene dati multimediali digitali. In circostanze normali, ogni flusso è associato a un singolo output. Durante la riproduzione, l'oggetto Reader recapita esempi per ogni output. Pertanto, per impostazione predefinita, ogni flusso in un file ASF viene recapitato dal lettore durante la riproduzione.

Esistono situazioni in cui non si desidera che ogni flusso venga recapitato al client. Se, ad esempio, si crea un file video con cinque flussi audio, uno per ogni cinque lingue, è necessario recapitarne solo uno alla volta. L'esclusione reciproca è una funzionalità di Windows Media Format SDK che consente di specificare un numero di flussi che si escludono a vicenda che equivalgono allo stesso output.

L'esclusione reciproca viene definita nel profilo utilizzato per creare un file. È possibile configurare l'esclusione reciproca in un profilo utilizzando oggetti di esclusione reciproca. Si aggiungono i flussi uno alla volta all'oggetto di esclusione reciproca, si imposta il tipo e si include l'oggetto nel profilo.

Windows Media Format SDK riconosce quattro tipi di esclusione reciproca:

-   Velocità in bit
-   Linguaggio
-   Presentazione
-   Sconosciuto

## <a name="mutual-exclusion-by-bit-rate"></a>Esclusione reciproca per velocità in bit

L'esclusione reciproca della velocità in bit è un tipo speciale di esclusione reciproca ed è più comunemente indicata come esclusione reciproca a più bit (MBR). Un'esclusione reciproca MBR contiene un numero di flussi che provengono tutti dallo stesso input, ma sono codificati a velocità in bit diverse. Quando si riproduce un file con MBR, il lettore determina il flusso migliore da usare in base alla larghezza di banda disponibile.

Windows Media Format SDK supporta MBR per flussi audio e video. L'SDK supporta anche un tipo speciale di video MBR denominato più dimensioni video MBR. Questo è analogo al normale video MBR, tranne per il fatto che i singoli flussi possono avere dimensioni di frame differenti. Ad esempio, è possibile che siano presenti alcuni flussi alla dimensione del video predefinita 320 x 240 e altre con velocità in bit superiori e 640 x 480 di dimensioni del video.

## <a name="mutual-exclusion-by-language"></a>Esclusione reciproca per lingua

L'esclusione reciproca basata sulla lingua è progettata per essere usata con contenuto (in genere audio) registrato in più lingue. Un'esclusione reciproca basata sul linguaggio include diversi flussi originati da input univoci. Ogni input è lo stesso contenuto, ma in una lingua diversa.

Per l'esclusione reciproca in base al linguaggio, l'applicazione di lettura deve includere la logica per selezionare la lingua appropriata. Se si scrive un'applicazione per riprodurre file ASF e si desidera supportare i file con esclusione reciproca basata sulla lingua, è necessario selezionare il flusso appropriato prima di iniziare la riproduzione.

## <a name="mutual-exclusion-by-presentation"></a>Esclusione reciproca per presentazione

Viene fornita l'esclusione reciproca basata sulla presentazione per supportare flussi video contenenti lo stesso contenuto codificato con proporzioni diverse. Viene in genere usato quando si fornisce video in una versione letterbox (proporzioni 16:9) e formattato per le schermate televisive (proporzioni 4:3).

La selezione di una presentazione per la riproduzione è spesso determinata dall'utente. Se si scrive un'applicazione per riprodurre file ASF e si desidera supportare i file con esclusione reciproca basata sulla presentazione, è necessario presentare all'utente la possibilità di selezionare un tipo di presentazione per la visualizzazione.

## <a name="unknown-mutual-exclusion"></a>Esclusione reciproca sconosciuta

Puoi creare un'esclusione reciproca in base ai criteri che preferisci. Tutti i tipi di esclusione reciproca personalizzata devono essere creati usando il tipo sconosciuto.

## <a name="advanced-mutual-exclusion-features"></a>Funzionalità avanzate di esclusione reciproca

È anche possibile usare l'esclusione reciproca per assegnare flussi a gruppi che si escludono reciprocamente tra loro. Ad esempio, potrebbe essere necessario disporre di flussi audio in più lingue e assegnare un flusso video diverso a ognuno di essi. Si usa l'esclusione reciproca per raggruppare ogni flusso audio con il flusso video corrispondente e rendere tutti i gruppi che si escludono a vicenda.

Il Reader seleziona automaticamente i flussi per tutte le esclusioni reciproche. Per tutti i tipi di esclusione reciproca tranne MBR ed esclusione reciproca basata sulla lingua, il Reader seleziona sempre il flusso predefinito, ovvero il primo flusso aggiunto all'oggetto di esclusione reciproca nel profilo. Per MBR, il lettore seleziona il flusso che meglio si adatta alla larghezza di banda disponibile al momento della riproduzione. Se non si vuole usare il flusso predefinito, è possibile impostare la selezione del flusso su manuale prima di iniziare la lettura di un file.

La selezione del flusso manuale si applica all'intero file. Le difficoltà possono verificarsi quando si hanno esclusioni reciproche di tipi diversi nello stesso file. Un file può includere, ad esempio, l'esclusione reciproca basata sulla velocità in bit e l'esclusione reciproca personalizzata. Per selezionare un flusso diverso da quello predefinito nell'esclusione reciproca personalizzata, è necessario usare la selezione del flusso manuale. Se si usa la selezione del flusso manuale, tuttavia, il lettore non selezionerà automaticamente il flusso a più velocità in bit. È necessario pianificare questa eventualità nell'applicazione se si prevede di supportare più tipi di esclusione reciproca in un singolo file. Ciò significa in genere creare routine di selezione dei flussi personalizzati per i tipi di esclusione reciproca normalmente automatici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità file ASF**](asf-file-features.md)
</dt> <dt>

[**Uso dell'esclusione reciproca**](using-mutual-exclusion.md)
</dt> </dl>

 

 




