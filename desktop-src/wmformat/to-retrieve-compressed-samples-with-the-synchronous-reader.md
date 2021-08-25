---
title: Per recuperare esempi compressi con il lettore sincrono
description: Per recuperare esempi compressi con il lettore sincrono
ms.assetid: 1f6da1aa-c26a-486a-bb44-cc4305c71979
keywords:
- Advanced Systems Format (ASF), recupero di esempi compressi
- ASF (Advanced Systems Format), recupero di esempi compressi
- Advanced Systems Format (ASF), lettori sincroni
- ASF (Advanced Systems Format), lettori sincroni
- Advanced Systems Format (ASF), esempi compressi
- ASF (Advanced Systems Format), esempi compressi
- lettori sincroni, recupero di esempi compressi
- lettori sincroni, esempi compressi
- esempi compressi, recupero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eeb2e3c7f1f6e00bd3f1c215a3b6783387fd3e19c268afe58862aa4b4d61889
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807461"
---
# <a name="to-retrieve-compressed-samples-with-the-synchronous-reader"></a>Per recuperare esempi compressi con il lettore sincrono

Analogamente al lettore asincrono, anche il lettore sincrono può recuperare esempi compressi. Gli esempi compressi devono essere usati quando si copiano flussi da un file a un altro.

L Windows Media Format SDK non fornisce metodi per decodificare i dati dopo che sono stati estratti da un file ASF. Se si ricevono esempi compressi e in un secondo momento si vuole decomprimerli, sarà necessario fornire il proprio codice a tale scopo. Un modo per aggirare questa limitazione è scrivere gli esempi compressi in un nuovo file ASF e quindi rilevarli in normali esempi non compressi.

Per ricevere esempi compressi con il lettore sincrono, chiamare [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) prima o durante la riproduzione. Passare true per *fCompressed*.

> [!Note]  
> I flussi di immagine non sono validi per il recapito di flussi compressi. Se si copia un flusso di immagini da un file a un altro, non funzionerà nel nuovo file. Per copiare un flusso di immagine da un file a un file, recuperare gli esempi del flusso di immagini in base al numero di output e includerli nel nuovo file come se fosse incluso un nuovo flusso di immagini.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file con il lettore sincrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




