---
description: Errori di rendering
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Errori di rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31d49c5fbb82457282decdaa07152e75db6bc3e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482587"
---
# <a name="rendering-errors"></a>Errori di rendering

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Microsoft® DirectShow® Editing Services (DES) definisce vari codici di errore usati per registrare gli errori di rendering. Se il rendering di un progetto non viene eseguito correttamente, il motore di rendering chiama il [**metodo IAMErrorLog::LogError.**](iamerrorlog-logerror.md) Nella tabella seguente sono riepilogati i parametri forniti a **LogError**:

-   Il codice di errore è contenuto nel *parametro ErrorCode.*
-   La descrizione è contenuta nel parametro ErrorString.
-   La descrizione è contenuta nel *parametro ErrorString.*
-   Se sono presenti informazioni aggiuntive, il **tipo VARIANT** è contenuto nel membro **vt** dell'elemento **VARIANT** a cui *punta pExtraInfo*.

> [!Note]  
> I codici di errore descritti qui non sono **valori HRESULT.** Per un elenco dei **valori restituiti HRESULT** specifici di DES, vedere [Codici di errore e di esito positivo](error-and-success-codes.md).

 




| Codice di errore | Descrizione | Informazioni aggiuntive | Tipo variant | 
|------------|-------------|-------------------|--------------|
| DEX_IDS_BAD_SOURCE_NAME | Il nome file non esiste o DirectShow non riconosce l'estensione del file. | Nome file | <strong>BSTR</strong> | 
| DEX_IDS_BAD_SOURCE_NAME2 | Il tipo di file non corrisponde all'estensione di file o il file è danneggiato. | Nome file | <strong>BSTR</strong> | 
| DEX_IDS_MISSING_SOURCE_NAME | Il nome file era obbligatorio, ma non è stato specificato. | Nessuno | Non applicabile | 
| DEX_IDS_UNKNOWN_SOURCE | Impossibile analizzare l'origine dati fornita da questa origine. | Nessuno | Non applicabile | 
| DEX_IDS_INSTALL_PROBLEM | Errore imprevisto. Alcuni DirectShow componente non sono installati correttamente. | Nessuno | Non applicabile | 
| DEX_IDS_NO_SOURCE_NAMES | Il filtro di origine non accetta nomi di file. | Nessuno | Non applicabile | 
| DEX_IDS_BAD_MEDIATYPE | Il tipo di supporto del gruppo non è supportato. | Numero gruppo | <strong>int</strong> | 
| DEX_IDS_STREAM_NUMBER | Numero di flusso non valido per questa origine. | Numero di flusso | <strong>int</strong> | 
| DEX_IDS_OUTOFMEMORY | Memoria insufficiente. | Nessuno | Non applicabile | 
| DEX_IDS_DIBSEQ_NOTALLSAME | Una bitmap nella sequenza non era dello stesso tipo delle altre. | Nome bitmap | <strong>BSTR</strong> | 
| DEX_IDS_CLIPTOOSHORT | I tempi multimediali del clip non sono validi o la sequenza DIB (Device-Independent Bitmap) è troppo breve.<blockquote>[!Note]<br />Se si verificano altri errori di rendering, questo errore potrebbe verificarsi anche se i tempi dei supporti sono validi.</blockquote><br /> | Nessuno | Non applicabile | 
| DEX_IDS_INVALID_DXT | L'identificatore di classe (CLSID) dell'effetto o della transizione non è valido. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_INVALID_DEFAULT_DXT | Il CLSID dell'effetto o della transizione predefinita non è valido. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_NO_3D | La versione di DirectX non supporta le transizioni tridimensionali. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_BROKEN_DXT | Questo effetto non è del tipo giusto o viene interrotto. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_NO_SUCH_PROPERTY | Questa proprietà non esiste nell'oggetto . | Nome proprietà | <strong>BSTR</strong> | 
| DEX_IDS_ILLEGAL_PROPERTY_VAL | Valore non valido per questa proprietà. | Valore specificato | <strong>VARIANTE</strong> | 
| DEX_IDS_INVALID_XML | Errore di sintassi nel file XML. | Numero di riga | VT_I4 (intero a 4 byte) | 
| DEX_IDS_CANT_FIND_FILTER | Impossibile trovare il filtro specificato in XML in base alla categoria e all'istanza. | Nome descrittivo (istanza) | <strong>BSTR</strong> | 
| DEX_IDS_DISK_WRITE_ERROR | Errore durante la scrittura del file XML su disco. | Nessuno | Non applicabile | 
| DEX_IDS_INVALID_AUDIO_FX | CLSID non valido DirectShow filtro effetto audio. | CLSID | <strong>BSTR</strong> | 
| DEX_IDS_CANT_FIND_COMPRESSOR | Impossibile trovare un file per produrre il formato di compressione specificato. | Nessuno | Non applicabile | 




 

Gli errori seguenti non devono mai verificarsi. Se si verifica uno di questi errori, inviare una segnalazione di bug a Microsoft.



| Codice di errore                 | Descrizione                                 |
|----------------------------|---------------------------------------------|
| ANALISI SEQUENZA TEMPORALE ID DEX \_ \_ \_  | Errore imprevisto durante l'analisi della sequenza temporale.      |
| ERRORE DEL \_ GRAFO DEGLI ID DEX \_ \_     | Errore imprevisto durante la compilazione del grafico dei filtri. |
| ERRORE DELLA GRIGLIA DEGLI ID DEX \_ \_ \_      | Errore imprevisto con la griglia interna.    |
| ERRORE \_ DELL'INTERFACCIA IDS \_ \_ DEX | Errore imprevisto durante il recupero di un'interfaccia.      |



 

 

 




