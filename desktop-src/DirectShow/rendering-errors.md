---
description: Errori di rendering
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Errori di rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e5af72ccf7ca76b2d4899178757282f1879c06052d2db2f3e1d929ddeef0f53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050611"
---
# <a name="rendering-errors"></a>Errori di rendering

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Microsoft® DirectShow® Editing Services (DES) definisce vari codici di errore usati per registrare gli errori di rendering. Se il rendering di un progetto non viene eseguito correttamente, il motore di rendering chiama il [**metodo IAMErrorLog::LogError.**](iamerrorlog-logerror.md) Nella tabella seguente sono riepilogati i parametri forniti a **LogError**:

-   Il codice di errore è contenuto nel *parametro ErrorCode.*
-   La descrizione è contenuta nel parametro ErrorString.
-   La descrizione è contenuta nel *parametro ErrorString.*
-   Se sono presenti informazioni aggiuntive, il **tipo VARIANT** è contenuto nel membro **vt** dell'elemento **VARIANT** a cui *punta pExtraInfo*.

> [!Note]  
> I codici di errore descritti qui non sono **valori HRESULT.** Per un elenco dei **valori restituiti HRESULT** specifici di DES, vedere [Codici di errore e di esito positivo](error-and-success-codes.md).

 



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Codice di errore</th>
<th>Descrizione</th>
<th>Informazioni aggiuntive</th>
<th>Tipo variant</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DEX_IDS_BAD_SOURCE_NAME</td>
<td>Il nome del file non esiste o DirectShow non riconosce l'estensione del file.</td>
<td>Nome file</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_BAD_SOURCE_NAME2</td>
<td>Il tipo di file non corrisponde all'estensione di file o il file è danneggiato.</td>
<td>Nome file</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_MISSING_SOURCE_NAME</td>
<td>Il nome file era obbligatorio, ma non è stato specificato.</td>
<td>Nessuno</td>
<td>Non applicabile</td>
</tr>
<tr class="even">
<td>DEX_IDS_UNKNOWN_SOURCE</td>
<td>Impossibile analizzare l'origine dati fornita da questa origine.</td>
<td>Nessuno</td>
<td>Non applicabile</td>
</tr>
<tr class="odd">
<td>DEX_IDS_INSTALL_PROBLEM</td>
<td>Errore imprevisto. Alcuni DirectShow componente non sono installati correttamente.</td>
<td>Nessuno</td>
<td>Non applicabile</td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_SOURCE_NAMES</td>
<td>Il filtro di origine non accetta nomi di file.</td>
<td>Nessuno</td>
<td>Non applicabile</td>
</tr>
<tr class="odd">
<td>DEX_IDS_BAD_MEDIATYPE</td>
<td>Il tipo di supporto del gruppo non è supportato.</td>
<td>Numero gruppo</td>
<td><strong>int</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_STREAM_NUMBER</td>
<td>Numero di flusso non valido per questa origine.</td>
<td>Numero di flusso</td>
<td><strong>int</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_OUTOFMEMORY</td>
<td>Memoria insufficiente.</td>
<td>Nessuno</td>
<td>Non applicabile</td>
</tr>
<tr class="even">
<td>DEX_IDS_DIBSEQ_NOTALLSAME</td>
<td>Una bitmap nella sequenza non era dello stesso tipo delle altre.</td>
<td>Nome bitmap</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_CLIPTOOSHORT</td>
<td>I tempi multimediali del clip non sono validi o la sequenza DIB (Device-Independent Bitmap) è troppo breve.
<blockquote>
[!Note]<br />
Se si verificano altri errori di rendering, questo errore potrebbe verificarsi anche se i tempi dei supporti sono validi.
</blockquote>
<br/></td>
<td>Nessuno</td>
<td>Non applicabile</td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_DXT</td>
<td>L'identificatore di classe (CLSID) dell'effetto o della transizione non è valido.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_INVALID_DEFAULT_DXT</td>
<td>Il CLSID dell'effetto o della transizione predefinita non è valido.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_3D</td>
<td>La versione di DirectX non supporta le transizioni tridimensionali.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_BROKEN_DXT</td>
<td>Questo effetto non è del tipo giusto o è interrotto.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_SUCH_PROPERTY</td>
<td>Questa proprietà non esiste nell'oggetto .</td>
<td>Nome proprietà</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_ILLEGAL_PROPERTY_VAL</td>
<td>Valore non valido per questa proprietà.</td>
<td>Valore specificato</td>
<td><strong>Variante</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_XML</td>
<td>Errore di sintassi nel file XML.</td>
<td>Numero di riga</td>
<td>VT_I4 (intero a 4 byte)</td>
</tr>
<tr class="odd">
<td>DEX_IDS_CANT_FIND_FILTER</td>
<td>Impossibile trovare il filtro specificato in XML in base alla categoria e all'istanza.</td>
<td>Nome descrittivo (istanza)</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_DISK_WRITE_ERROR</td>
<td>Errore durante la scrittura del file XML su disco.</td>
<td>Nessuno</td>
<td>Non applicabile</td>
</tr>
<tr class="odd">
<td>DEX_IDS_INVALID_AUDIO_FX</td>
<td>CLSID non è un filtro DirectShow effetto audio valido.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_CANT_FIND_COMPRESSOR</td>
<td>Impossibile trovare un file per produrre il formato di compressione specificato.</td>
<td>Nessuno</td>
<td>Non applicabile</td>
</tr>
</tbody>
</table>



 

Gli errori seguenti non dovrebbero mai verificarsi. Se si verifica uno di questi errori, inviare una segnalazione di bug a Microsoft.



| Codice di errore                 | Descrizione                                 |
|----------------------------|---------------------------------------------|
| ANALISI SEQUENZA TEMPORALE ID DEX \_ \_ \_  | Errore imprevisto durante l'analisi della sequenza temporale.      |
| ERRORE DEL \_ GRAFO DEGLI ID DEX \_ \_     | Errore imprevisto durante la compilazione del grafico dei filtri. |
| ERRORE DELLA GRIGLIA DEGLI ID DEX \_ \_ \_      | Errore imprevisto con la griglia interna.    |
| ERRORE \_ DELL'INTERFACCIA IDS \_ \_ DEX | Errore imprevisto durante il recupero di un'interfaccia.      |



 

 

 




