---
title: Uso del manifesto di trasferimento
description: La Pubblicazione guidata sul Web e l'Ordinamento guidato stampa online usano il manifesto di trasferimento per comunicare i dettagli del trasferimento dei dati tra il computer client e il sito del server.
ms.assetid: b7bb541c-3bf4-4aab-ac70-c006517e772e
keywords:
- Pubblicazione guidata sul Web, trasferimento del manifesto
- Ordinamento guidato stampa online, manifesto di trasferimento
- manifesto di trasferimento
- manifest
- window.external, manifesto di trasferimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d7f4ea3f9cd392f4b0bab50e1e558613fc7485d4f44a27472cd48ad898b3ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555851"
---
# <a name="using-the-transfer-manifest"></a>Uso del manifesto di trasferimento

La Pubblicazione guidata sul Web e l'Ordinamento guidato stampa online usano il manifesto di trasferimento per comunicare i dettagli del trasferimento dei dati tra il computer client e il sito del server.

## <a name="the-purpose-of-the-transfer-manifest"></a>Scopo del manifesto di trasferimento

Il manifesto di trasferimento descrive i file coinvolti nel trasferimento, inclusi dettagli quali la gerarchia di destinazione e i metadati del file. Lo script lato server può modificare il manifesto rimuovendo i file non appropriati dall'elenco e aggiungendo informazioni su come e dove devono essere trasferiti i file.

Il manifesto viene esposto come proprietà **window.external.Property("TransferManifest")**, un documento XML Document Object Model (DOM). Per altre informazioni sul DOM XML, vedere la documentazione MSDN per [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).

L'organizzazione di primo livello del manifesto di trasferimento è la seguente:


```
<transfermanifest>
    <filelist/>
    <folderlist/>
    <uploadinfo/>
</transfermanifest>
```



La pagina HTML lato server può usare i nodi nel manifesto per ottenere determinate informazioni sui file da copiare e quindi modificare di conseguenza l'interfaccia utente del servizio. Ad esempio, un sito di stampa di foto potrebbe usare le informazioni per visualizzare le anteprime delle immagini scelte, mentre un sito di archiviazione potrebbe usare le informazioni per garantire che sia disponibile spazio di archiviazione sufficiente per l'utente. Per informazioni complete sui nodi e sugli attributi del manifesto di trasferimento, vedere [Trasferisci schema manifesto](/windows/desktop/shell/interfaces).

Lo schema del manifesto di trasferimento viene scritto come modello aperto in modo che gli elementi non definiti in modo specifico nello schema vengano visualizzati nel manifesto di trasferimento. Pertanto, un sito del provider potrebbe aggiungere elementi proprietari per il proprio uso senza disturbare la validità del manifesto. Lo schema viene definito anche in modo che l'ordine degli elementi non sia limitato.

> [!Note]  
> Il manifesto viene ri-creato ogni volta che viene scelto un nuovo provider in modo che il provider abbia la possibilità di archiviare le informazioni sul sito nel manifesto.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasferire lo schema del manifesto](/windows/desktop/shell/interfaces)
</dt> </dl>

 

 