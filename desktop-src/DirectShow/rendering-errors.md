---
description: Errori di rendering
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Errori di rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e106a55363bf50e49a4966600662e26b03b53307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482236"
---
# <a name="rendering-errors"></a>Errori di rendering

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Microsoft® DirectShow® editing Services (DES) definisce diversi codici di errore utilizzati per registrare gli errori di rendering. Se il rendering di un progetto non viene eseguito correttamente, il motore di rendering chiama il metodo [**IAMErrorLog:: LogError**](iamerrorlog-logerror.md) . Nella tabella seguente sono riepilogati i parametri assegnati a **LogError**:

-   Il codice di errore è contenuto nel parametro *ErrorCode* .
-   La descrizione è contenuta nel parametro ErrorString.
-   La descrizione è contenuta nel parametro *ErrorString* .
-   Se sono presenti informazioni aggiuntive, il tipo **Variant** è contenuto nel membro **VT** della **variante** a cui punta *pExtraInfo*.

> [!Note]  
> I codici di errore descritti qui non sono valori **HRESULT** . Per un elenco di valori restituiti **HRESULT** specifici per des, vedere [codici di errore e di esito positivo](error-and-success-codes.md).

 



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
<td>Il nome file non esiste oppure DirectShow non riconosce l'estensione di file.</td>
<td>Nome file</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_BAD_SOURCE_NAME2</td>
<td>Il tipo di file non corrisponde all'estensione di file oppure il file è danneggiato.</td>
<td>Nome file</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_MISSING_SOURCE_NAME</td>
<td>Il nome file è obbligatorio, ma non è stato specificato.</td>
<td>nessuno</td>
<td>Non applicabile</td>
</tr>
<tr class="even">
<td>DEX_IDS_UNKNOWN_SOURCE</td>
<td>Impossibile analizzare l'origine dati fornita da questa origine.</td>
<td>nessuno</td>
<td>Non applicabile</td>
</tr>
<tr class="odd">
<td>DEX_IDS_INSTALL_PROBLEM</td>
<td>Errore imprevisto. Componente DirectShow non installato correttamente.</td>
<td>nessuno</td>
<td>Non applicabile</td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_SOURCE_NAMES</td>
<td>Il filtro di origine non accetta nomi di file.</td>
<td>nessuno</td>
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
<td>Il numero di flusso per questa origine non è valido.</td>
<td>Numero di flusso</td>
<td><strong>int</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_OUTOFMEMORY</td>
<td>Memoria insufficiente.</td>
<td>nessuno</td>
<td>Non applicabile</td>
</tr>
<tr class="even">
<td>DEX_IDS_DIBSEQ_NOTALLSAME</td>
<td>Una bitmap nella sequenza non è dello stesso tipo degli altri.</td>
<td>Nome bitmap</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_CLIPTOOSHORT</td>
<td>I tempi di supporto della clip non sono validi o la sequenza di bitmap (DIB) indipendente dal dispositivo è troppo corta.
<blockquote>
[!Note]<br />
Se si verificano altri errori di rendering, questo errore può verificarsi anche se i tempi dei supporti sono validi.
</blockquote>
<br/></td>
<td>nessuno</td>
<td>Non applicabile</td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_DXT</td>
<td>Identificatore di classe (CLSID) dell'effetto o della transizione non valido.</td>
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
<td>Questo effetto non è il tipo corretto o è danneggiato.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_NO_SUCH_PROPERTY</td>
<td>Questa proprietà non esiste nell'oggetto.</td>
<td>Nome proprietà</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="odd">
<td>DEX_IDS_ILLEGAL_PROPERTY_VAL</td>
<td>Valore non valido per questa proprietà.</td>
<td>Valore specificato</td>
<td><strong>VARIANTE</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_INVALID_XML</td>
<td>Errore di sintassi nel file XML.</td>
<td>Numero di riga</td>
<td>VT_I4 (Integer a 4 byte)</td>
</tr>
<tr class="odd">
<td>DEX_IDS_CANT_FIND_FILTER</td>
<td>Impossibile trovare il filtro specificato in XML per categoria e istanza.</td>
<td>Nome descrittivo (istanza)</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_DISK_WRITE_ERROR</td>
<td>Errore durante la scrittura del file XML su disco.</td>
<td>nessuno</td>
<td>Non applicabile</td>
</tr>
<tr class="odd">
<td>DEX_IDS_INVALID_AUDIO_FX</td>
<td>CLSID non è un filtro effetto audio DirectShow valido.</td>
<td>CLSID</td>
<td><strong>BSTR</strong></td>
</tr>
<tr class="even">
<td>DEX_IDS_CANT_FIND_COMPRESSOR</td>
<td>Non è possibile trovare un compressore per produrre il formato di compressione specificato.</td>
<td>nessuno</td>
<td>Non applicabile</td>
</tr>
</tbody>
</table>



 

Gli errori seguenti non dovrebbero mai verificarsi. Se si verifica uno di questi errori, inviare un report sui bug a Microsoft.



| Codice di errore                 | Descrizione                                 |
|----------------------------|---------------------------------------------|
| \_ \_ Analisi sequenza temporale ID Dex \_  | Errore imprevisto durante l'analisi della sequenza temporale.      |
| \_ \_ errore grafico ID \_ Dex     | Errore imprevisto durante la creazione del grafico del filtro. |
| \_errore di \_ griglia \_ ID Dex      | Errore imprevisto della griglia interna.    |
| \_errore dell' \_ interfaccia \_ ID Dex | Errore imprevisto durante il recupero di un'interfaccia.      |



 

 

 




