---
title: Per recuperare esempi compressi con il lettore sincrono
description: Per recuperare esempi compressi con il lettore sincrono
ms.assetid: 1f6da1aa-c26a-486a-bb44-cc4305c71979
keywords:
- Formato di sistemi avanzati (ASF), recupero di esempi compressi
- ASF (formato avanzato dei sistemi), recupero di esempi compressi
- ASF (Advanced Systems Format), lettori sincroni
- ASF (formato avanzato dei sistemi), lettori sincroni
- ASF (Advanced Systems Format), esempi compressi
- ASF (Advanced Systems Format), esempi compressi
- lettori sincroni, recupero di esempi compressi
- lettori sincroni, esempi compressi
- esempi compressi, recupero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f0051fc14a14500b2c6e69c5e32f7ec0c39a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117367"
---
# <a name="to-retrieve-compressed-samples-with-the-synchronous-reader"></a>Per recuperare esempi compressi con il lettore sincrono

Analogamente al Reader asincrono, il lettore sincrono può recuperare anche esempi compressi. Gli esempi compressi devono essere usati per la copia di flussi da un file a un altro.

Windows Media Format SDK non fornisce alcun metodo per la decodifica dei dati dopo che è stato Estratto da un file ASF. Se si ricevono esempi compressi e successivamente si desidera decomprimerli, sarà necessario fornire il proprio codice a tale scopo. Per aggirare questa limitazione, è possibile scrivere gli esempi compressi in un nuovo file ASF e quindi leggerli nuovamente in campioni normali non compressi.

Per ricevere esempi compressi con il lettore sincrono, chiamare [**IWMSyncReader:: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) prima o durante la riproduzione. Passare true per *fCompressed*.

> [!Note]  
> I flussi di immagini non sono validi per il recapito di flussi compressi. Se si copia un flusso di immagini da un file a un altro, non funzionerà nel nuovo file. Per copiare un flusso di immagini da un file a un altro, recuperare gli esempi di flusso dell'immagine in base al numero di output e includerli nel nuovo file come se fosse incluso un nuovo flusso di immagine.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file con il lettore sincrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




