---
description: Guida di riferimento al file con estensione AVI
ms.assetid: 2d8cf5be-1252-4b58-89b1-f5c53ea17d0e
title: Guida di riferimento al file con estensione AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f28a7254ac9eb927381e313603ffd2bd0d050c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482548"
---
# <a name="avi-riff-file-reference"></a>Guida di riferimento al file con estensione AVI

Il formato di file di Microsoft AVI è una specifica del file RIFF usata con le applicazioni che acquisiscono, modificano e riproducono sequenze audio-video. In generale, i file AVI contengono più flussi di tipi diversi di dati. La maggior parte delle sequenze AVI USA flussi audio e video. Una variante semplice per una sequenza AVI usa dati video e non richiede un flusso audio.

Questa sezione non descrive le estensioni di formato file AVI di OpenDML. Per ulteriori informazioni su queste estensioni, vedere *OPENDML AVI file format Extensions*, pubblicato dal sottocomitato del formato di file OpenDML AVI M-JPEG.

## <a name="fourccs"></a>FourCC

Un FOURCC (codice a quattro caratteri) è un Unsigned Integer a 32 bit creato concatenando quattro caratteri ASCII. Ad esempio, il FOURCC "abcd" viene rappresentato in un sistema di Little-Endian come 0x64636261. FourCC può contenere caratteri di spazio, quindi "ABC" è un FOURCC valido. Il formato di file AVI usa i codici FOURCC per identificare i tipi di flusso, i blocchi di dati, le voci di indice e altre informazioni.

## <a name="riff-file-format"></a>Formato file RIFF

Il formato del file AVI è basato sul formato di documento RIFF (Resource Interchange File Format). Un file RIFF è costituito da un'intestazione RIFF seguita da zero o più *elenchi* e *blocchi*.

-   L'intestazione RIFF ha il formato seguente:

    `'RIFF' fileSize fileType (data)`

    dove ' RIFF ' è il codice FOURCC ' RIFF ' letterale, `fileSize` è un valore a 4 byte che fornisce la dimensione dei dati nel file e `fileType` è un FourCC che identifica il tipo di file specifico. Il valore di `fileSize` include le dimensioni di `fileType` fourcc più le dimensioni dei dati seguenti, ma non include le dimensioni del FourCC ' riff ' o la dimensione di `fileSize` . I dati dei file sono costituiti da blocchi ed elenchi, in qualsiasi ordine.

-   Un blocco ha il formato seguente:

    `ckID ckSize ckData`

    dove `ckID` è un FourCC che identifica i dati contenuti nel blocco, `ckSize` è un valore a 4 byte che fornisce la dimensione dei dati in `ckData` e `ckData` è pari a zero o più byte di dati. I dati vengono sempre riempiti al confine di **parola** più vicino. `ckSize` indica la dimensione dei dati validi nel blocco. non include la spaziatura interna, la dimensione `ckID` o la dimensione di `ckSize` .

-   Un elenco ha il formato seguente:

    `'LIST' listSize listType listData`

    dove "LIST" è il valore letterale FOURCC code "LIST", `listSize` è un valore a 4 byte che assegna la dimensione dell'elenco, `listType` è un codice FourCC ed è `listData` costituito da blocchi o elenchi, in qualsiasi ordine. Il valore di `listSize` include le dimensioni di `listType` più le dimensioni di `listData` ; non include il FourCC ' List ' o la dimensione di `listSize` .

Il resto di questa sezione usa la notazione seguente per descrivere i blocchi RIFF:

`ckID ( ckData )`

dove le dimensioni del blocco sono implicite. Utilizzando questa notazione, un elenco può essere rappresentato come:

`'LIST' ( listType ( listData ) )`

Gli elementi facoltativi sono racchiusi tra parentesi quadre: `[ optional element ]`

## <a name="avi-riff-form"></a>Formato AVI RIFF

I file AVI sono identificati da FOURCC ' AVI ' nell'intestazione RIFF. Tutti i file AVI includono due blocchi elenco obbligatori, che definiscono rispettivamente il formato dei flussi e i dati di flusso. Un file AVI può includere anche un blocco dell'indice, che fornisce la posizione dei blocchi di dati all'interno del file. Un file AVI con questi componenti ha il formato seguente:


```C++
RIFF ('AVI '
      LIST ('hdrl' ... )
      LIST ('movi' ... )
      ['idx1' (<AVI Index>) ]
     )
```



L'elenco ' hdrl ' definisce il formato dei dati ed è il primo blocco di elenco richiesto. L'elenco ' movi ' contiene i dati per la sequenza AVI ed è il secondo blocco elenco obbligatorio. L'elenco ' IDX1' contiene l'indice. I file AVI devono contenere questi tre componenti nella sequenza corretta.

> [!Note]  
> Le estensioni OpenDML definiscono un altro tipo di indice, identificato da FOURCC ' indx '.

 

Gli elenchi ' hdrl ' è movi ' usano i sottoblocchi per i dati. Nell'esempio seguente viene illustrato il formato AVI RIFF espanso con i blocchi necessari per completare gli elenchi:


```C++
RIFF ('AVI '
      LIST ('hdrl'
            'avih'(<Main AVI Header>)
            LIST ('strl'
                  'strh'(<Stream header>)
                  'strf'(<Stream format>)
                  [ 'strd'(<Additional header data>) ]
                  [ 'strn'(<Stream name>) ]
                  ...
                 )
             ...
           )
      LIST ('movi'
            {SubChunk | LIST ('rec '
                              SubChunk1
                              SubChunk2
                              ...
                             )
               ...
            }
            ...
           )
      ['idx1' (<AVI Index>) ]
     )
```



## <a name="avi-main-header"></a>Intestazione principale AVI

L'elenco ' hdrl ' inizia con l'intestazione AVI principale, che è contenuta in un blocco ' AVIH '. L'intestazione principale contiene informazioni globali per l'intero file AVI, ad esempio il numero di flussi all'interno del file e la larghezza e l'altezza della sequenza AVI. Il blocco principale dell'intestazione è costituito da una struttura [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) .

## <a name="avi-stream-headers"></a>Intestazioni del flusso AVI

Uno o più elenchi ' STRl ' seguono l'intestazione principale. Per ogni flusso di dati è necessario un elenco ' STRl '. Ogni elenco ' STRl ' contiene informazioni su un flusso nel file e deve contenere un blocco di intestazione del flusso (' Strh ') e un blocco di formato del flusso (' strF '). Inoltre, un elenco ' STRl ' potrebbe contenere un blocco di dati di intestazione del flusso (' Strd ') e un blocco del nome del flusso (' STRN ').

Il blocco di intestazione del flusso (' Strh ') è costituito da una struttura [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) .

Un blocco di formato del flusso (' strF ') deve seguire il blocco dell'intestazione del flusso. Il blocco formato flusso descrive il formato dei dati nel flusso. I dati contenuti in questo blocco dipendono dal tipo di flusso. Per i flussi video, le informazioni sono una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , incluse le informazioni sulla tavolozza, se appropriato. Per i flussi audio, le informazioni sono una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

Se il blocco di dati dell'intestazione del flusso (' Strd ') è presente, segue il blocco del formato del flusso. Il formato e il contenuto di questo blocco sono definiti dal driver del codec. In genere, i driver utilizzano queste informazioni per la configurazione. Le applicazioni che leggono e scrivono file AVI non devono interpretare queste informazioni; il trasferimento è semplice da e verso il driver come blocco di memoria.

Il blocco facoltativo ' STRN ' contiene una stringa di testo con terminazione null che descrive il flusso.

Le intestazioni del flusso nell'elenco "hdrl" sono associate ai dati del flusso nell'elenco "movi" in base all'ordine dei blocchi "STRl". Il primo blocco ' STRl ' si applica al flusso 0, il secondo si applica al flusso 1 e così via.

## <a name="stream-data-movi-list"></a>Dati di flusso (elenco ' movi ')

Le informazioni di intestazione sono un elenco ' movi ' che contiene i dati effettivi nei flussi, ovvero i fotogrammi video e gli esempi audio. I blocchi di dati possono trovarsi direttamente nell'elenco ' movi ' oppure possono essere raggruppati all'interno degli elenchi ' REC '. Il raggruppamento ' REC ' implica che i blocchi raggruppati devono essere letti dal disco in una sola volta ed è destinato a file con interfoliazione per la riproduzione da CD-ROM.

Il FOURCC che identifica ogni blocco di dati è costituito da un numero di flusso a due cifre seguito da un codice di due caratteri che definisce il tipo di informazioni nel blocco.



| Codice a due caratteri | Descrizione              |
|--------------------|--------------------------|
| db                 | Fotogramma video non compresso |
| dc                 | Fotogramma video compresso   |
| pc                 | Modifica tavolozza           |
| WB                 | Dati audio               |



 

Se, ad esempio, il flusso 0 contiene audio, i blocchi di dati per quel flusso avranno il FOURCC ' 00wb '. Se Stream 1 contiene video, i blocchi di dati per quel flusso avranno FOURCC ' 01dB ' o ' 01DC '. I blocchi di dati video possono anche definire nuove voci della tavolozza per aggiornare la tavolozza durante una sequenza AVI. Ogni tavolozza-Modifica blocco (' xxpc ') contiene una struttura [**AVIPALCHANGE**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) . Se un flusso contiene modifiche della tavolozza, impostare il flag **AVISF \_ video \_ PALCHANGES** nel membro **dwFlags** della struttura [**AVISTREAMHEADER**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) per quel flusso.

I flussi di testo possono utilizzare codici arbitrari di due caratteri.

## <a name="avi-index-entries"></a>Voci di indice AVI

<dl> <dt>

<span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>Indice AVI 1,0
</dt> <dd>

Un blocco index (' IDX1') facoltativo può seguire l'elenco ' movi '. L'indice contiene un elenco dei blocchi di dati e la relativa posizione nel file. È costituito da una struttura [**AVIOLDINDEX**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) con le voci per ogni blocco di dati, inclusi i blocchi "REC". Se il file contiene un indice, impostare il flag **AVIF \_ HASINDEX** nel membro **dwFlags** della struttura [**AVIMAINHEADER**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) .

</dd> <dt>

<span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>Indice AVI 2,0
</dt> <dd>

Un indice AVI 2,0 può essere visualizzato come singolo blocco. In alternativa, i segmenti di indice possono essere interfogliati all'interno del blocco ' movi '. Se i segmenti di indice vengono posizionati nel blocco ' movi ', un indice Super contiene un indice dei segmenti di indice. La struttura [**AVIMETAINDEX**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex) è la struttura di base per i segmenti di indice e per l'indice con privilegi avanzati. Per altre informazioni, vedere le *estensioni di formato file AVI di OpenDML*, pubblicate dal sottocomitato formato file OpenDML AVI M-JPEG. Questa risorsa potrebbe non essere disponibile in alcune lingue e paesi.

</dd> </dl>

## <a name="other-data-chunks"></a>Altri blocchi di dati

I dati possono essere allineati in un file AVI inserendo i blocchi ' JUNK ' in base alle esigenze. Le applicazioni devono ignorare il contenuto di un blocco "JUNK".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato file AVI](avi-file-format.md)
</dt> </dl>

 

 
