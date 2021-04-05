---
title: Utilizzo del manifesto di trasferimento
description: La pubblicazione guidata sul Web e l'ordinamento guidato stampa online utilizzano il manifesto di trasferimento per comunicare i dettagli del trasferimento dei dati tra il computer client e il sito del server.
ms.assetid: b7bb541c-3bf4-4aab-ac70-c006517e772e
keywords:
- Pubblicazione guidata sul Web, trasferimento manifesto
- Procedura guidata per l'ordine di stampa online, trasferimento manifesto
- trasferire il manifesto
- manifest
- finestra. External, trasferimento manifesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fa7b3a35a6f06e2939b6c25f82d12c2b98a7f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872502"
---
# <a name="using-the-transfer-manifest"></a>Utilizzo del manifesto di trasferimento

La pubblicazione guidata sul Web e l'ordinamento guidato stampa online utilizzano il manifesto di trasferimento per comunicare i dettagli del trasferimento dei dati tra il computer client e il sito del server.

## <a name="the-purpose-of-the-transfer-manifest"></a>Scopo del manifesto di trasferimento

Il manifesto di trasferimento descrive i file che coinvolgono il trasferimento, inclusi i dettagli, ad esempio la gerarchia di destinazione e i metadati del file. Lo script lato server può modificare il manifesto rimuovendo i file non appropriati dall'elenco e aggiungendo le informazioni su come e dove trasferire i file.

Il manifesto viene esposto come finestra proprietà **. External. Property ("TransferManifest")**, un documento XML Document Object Model (Dom). Per ulteriori informazioni sul modello DOM XML, vedere la documentazione MSDN relativa a [IXMLDOMDocument/DOMDocument](/previous-versions/windows/desktop/ms756987(v=vs.85)).

L'organizzazione di primo livello del manifesto di trasferimento è la seguente:


```
<transfermanifest>
    <filelist/>
    <folderlist/>
    <uploadinfo/>
</transfermanifest>
```



La pagina HTML sul lato server può utilizzare i nodi del manifesto per ottenere determinate informazioni sui file da copiare e quindi modificare di conseguenza l'interfaccia utente del servizio. Ad esempio, un sito di stampa di foto può utilizzare le informazioni per visualizzare le anteprime delle immagini scelte, mentre un sito di archiviazione può utilizzare le informazioni per assicurarsi che sia disponibile spazio di archiviazione sufficiente per tale utente. Per informazioni complete sugli attributi e sui nodi del manifesto di trasferimento, vedere [Transfer manifest schema](/windows/desktop/shell/interfaces).

Lo schema del manifesto di trasferimento viene scritto come modello aperto in modo che gli elementi non definiti specificamente nello schema siano visualizzati nel manifesto di trasferimento. Pertanto, un sito del provider può aggiungere elementi proprietari per il proprio utilizzo senza compromettere la validità del manifesto. Lo schema viene definito anche in modo che l'ordine degli elementi non sia limitato.

> [!Note]  
> Il manifesto viene ricreato ogni volta che viene scelto un nuovo provider, in modo che il provider abbia la possibilità di archiviare le informazioni sul sito nel manifesto.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasferimento dello schema del manifesto](/windows/desktop/shell/interfaces)
</dt> </dl>

 

 