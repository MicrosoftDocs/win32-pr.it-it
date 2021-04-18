---
description: Indicizzatore ASF
ms.assetid: 3f95b0ac-d70f-4bc2-8524-c7de1df34afa
title: Indicizzatore ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c729b547339149ee578a90283c570ec8460b0c57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305524"
---
# <a name="asf-indexer"></a>Indicizzatore ASF

L' *indicizzatore* ASF è un componente di livello WMContainer che viene usato per leggere o scrivere oggetti index in un file di formato Advanced Systems (ASF). Per informazioni sulla struttura di un file ASF, vedere la pagina relativa alla [struttura dei file ASF](asf-file-structure.md).

Un'applicazione può utilizzare l'indicizzatore per eseguire la ricerca in base all'ora di presentazione o per generare nuove voci di indice per un file ASF. L'indicizzatore ASF implementa l'interfaccia [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo di indice</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Indice basato sul tempo di presentazione</td>
<td>Fornisce l'indicizzazione basata sul tempo di presentazione per i flussi audio e video nei blocchi di indice per rendere l'indicizzazione più efficiente dello spazio. Ogni blocco di indice fa riferimento a voci di indice che contengono un offset di byte. <br/> L'offset è la posizione del pacchetto di dati cercato, relativo all'inizio dell'oggetto dati ASF.<br/> GUID_NULL deve essere utilizzato come tipo GUID per l'identificatore dell'indice. Per ulteriori informazioni, vedere <a href="using-the-indexer-to-write-a-new-index.md">uso dell'indicizzatore per scrivere un nuovo indice</a>.<br/></td>
</tr>
<tr class="even">
<td>Indice timecode</td>
<td>Semplifica la ricerca in base al timecode nei flussi che contengono metadati del timecode. I timecode sono conformi a un formato SMPTE (<em>ore: minuti: secondi: frame</em>). Ogni blocco di indice fa riferimento a voci di indice che contengono un offset di byte. <br/> L'offset è la posizione del pacchetto di dati cercato, relativo all'inizio dell'oggetto dati ASF.<br/>
<blockquote>
[!Note]<br />
Gli oggetti indice del codice temporale non sono attualmente supportati.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>Indice basato su frame</td>
<td>Fornisce l'indicizzazione basata su frame per i flussi video. Gli indici nell'indice basato su frame sono in termini di numeri di frame, con il primo frame per un flusso nel file ASF corrispondente alla voce 0 nell'oggetto indice basato su frame. Ogni blocco di indice fa riferimento a voci di indice che contengono un offset di byte.<br/>
<blockquote>
[!Note]<br />
Gli oggetti indice basati su frame non sono attualmente supportati.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

In questa sezione vengono trattati gli argomenti seguenti.



| Argomento                                                                                | Descrizione                                                                                                                      |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Creazione e configurazione dell'indicizzatore](indexer-creation-and-configuration.md)         | Come creare un oggetto indicizzatore e configurarlo per la lettura di un indice esistente o per la scrittura di un nuovo oggetto indice ASF per un file. |
| [Uso dell'indicizzatore per la ricerca in un file](using-the-indexer-to-seek.md)                 | Come utilizzare l'indicizzatore per la ricerca all'interno di un file ASF.                                                                               |
| [Uso dell'indicizzatore per scrivere un nuovo indice](using-the-indexer-to-write-a-new-index.md) | Come utilizzare l'indicizzatore per generare voci di indice e scrivere un nuovo oggetto index per un file ASF.                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Componenti ASF WMContainer](wmcontainer-asf-components.md)
</dt> <dt>

[Supporto ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




