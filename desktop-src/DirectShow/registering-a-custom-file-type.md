---
description: In questo articolo viene descritto il modo in cui il gestore del grafico dei filtri individua un filtro di origine, dato un nome file.
ms.assetid: bc0d5719-6325-40fe-8261-ad00b91f272c
title: Registrazione di un tipo di file personalizzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e98c01555497ac628fff452f464c826475edbb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303900"
---
# <a name="registering-a-custom-file-type"></a>Registrazione di un tipo di file personalizzato

In questo articolo viene descritto il modo in cui il gestore del grafico dei filtri individua un filtro di origine, dato un nome file. È possibile utilizzare questo meccanismo per registrare i tipi di file personalizzati. Una volta registrato il tipo di file, DirectShow caricherà automaticamente il filtro di origine corretto ogni volta che un'applicazione chiama [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) o [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).

-   [Overview](#overview)
-   [Protocolli](#protocols)
-   [Estensioni di file](#file-extensions)
-   [Byte di controllo](#check-bytes)
-   [Caricamento del filtro di origine](#loading-the-source-filter)
-   [Tipi di file personalizzati in Windows Media Player](#custom-file-types-in-windows-media-player)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Per individuare un filtro di origine da un nome file specificato, il gestore del grafico del filtro tenta di eseguire le operazioni seguenti, nell'ordine indicato:

1.  Trovare la corrispondenza con il protocollo, se disponibile.
2.  Corrisponde all'estensione del file.
3.  Corrisponde ai modelli di byte all'interno del file, detti *Check bytes*.

## <a name="protocols"></a>Protocolli

I nomi di protocollo, ad esempio "FTP" o "http", sono registrati nel

**\_radice delle classi HKEY \_**

chiave, con la struttura seguente:


```C++
HKEY_CLASSES_ROOT
    <protocol>
        Source Filter = <Source filter CLSID>
        Extensions
            <.ext1> = <Source filter CLSID>
            <.ext2> = <Source filter CLSID>
```



Se il nome file o l'URL contiene i due punti (':'), il gestore del grafico del filtro tenta di utilizzare la parte prima di ':' come nome di protocollo. Se, ad esempio, il nome è "myprot://myfile.ext", viene eseguita la ricerca di una chiave del registro di sistema denominata **prot**. Se questa chiave esiste e contiene una sottochiave denominata "Extensions", il gestore del grafo dei filtri Cerca le voci che corrispondono all'estensione di file nella sottochiave. Il valore della chiave deve essere un GUID in formato stringa. ad esempio, " {00000000-0000-0000-0000-000000000000} ". Se il gestore del grafo del filtro non può corrispondere ad alcun elemento all'interno della sottochiave **Extensions** , Cerca una sottochiave denominata **Filter di origine**, che deve essere anche un GUID in formato stringa.

Se il gestore del grafo del filtro trova un GUID corrispondente, lo utilizza come CLSID del filtro di origine e tenta di caricare il filtro. Se non trova una corrispondenza, usa il filtro di [origine file (URL)](file-source--url--filter.md) , che considera il nome del file come un URL.

Questo algoritmo presenta due eccezioni:

-   Per escludere le lettere di driver, le stringhe a carattere singolo non vengono considerate protocolli.
-   Se la stringa è "file:" o "file://", non viene considerata come un protocollo.

## <a name="file-extensions"></a>Estensioni di file

Se non è presente alcun protocollo nel nome del file, il gestore del grafico dei filtri Cerca nel registro di sistema le voci con le principali **\_ \_ \\ \\ estensioni \\ del tipo di supporto radice delle classi HKEY**.*EXT* \\ , dove.*EXT* è l'estensione di file. Se questa chiave esiste, il **filtro di origine** del valore contiene il CLSID del filtro di origine, in formato stringa. Facoltativamente, la chiave può avere valori per il **tipo di supporto** e il **sottotipo**, che assegnano al tipo principale e ai GUID del sottotipo.

## <a name="check-bytes"></a>Byte di controllo

Alcuni tipi di file possono essere identificati da modelli specifici di bit che si verificano in offset di byte specifici nel file. Filter Graph Manager cerca le chiavi nel registro di sistema con il formato seguente:

**HKEY \_ Classi \_ radice \\ mediaType \\**{ *tipo principale* } \\ { *sottotipo* }

dove il *tipo principale* e il *sottotipo* sono GUID che definiscono il tipo di supporto per il flusso di byte. Ogni chiave contiene una o più sottochiavi, in genere denominate 1, 2 e così via, che definiscono i byte di controllo; e una sottochiave denominata **filtro di origine** che fornisce il CLSID del filtro di origine, in formato stringa. Le sottochiavi di byte di controllo sono stringhe che contengono uno o più quad di numeri chiamati:

*offset*, *CB*, *mask*, *Val*

Per trovare la corrispondenza con il file, il gestore del grafo del filtro legge i byte CB, a partire dall'offset del numero di byte. Esegue quindi un operatore and bit per bit sul valore in mask. Se il risultato è uguale a Val, il file corrisponde a tale quad. I valori mask e Val sono specificati in esadecimale. Una voce vuota per la maschera viene considerata come una stringa di 1s di lunghezza CB. Un valore negativo per offset indica un offset dalla fine del file. Per trovare la corrispondenza con la chiave, il file deve corrispondere a tutti i quad in una qualsiasi delle sottochiavi.

Si supponga, ad esempio, che il registro di sistema contenga le chiavi seguenti in **HKCR \\ Media Type**:


```C++
{e436eb83-524f-11ce-9f53-0020af0ba770}
    {7364696D-0000-0010-8000-00AA00389B71}
        0                    "0,4,,52494646,8,4,,524D4944"
        1                    "0,4,,4D546864"
        Source Filter        "{E436EBB5-524F-11CE-9F53-0020AF0BA770}"
```



La prima chiave corrisponde al tipo principale flusso MEDIATYPE \_ . Sottochiave seguente che corrisponde al sottotipo MEDIATYPE \_ MIDI. Il valore della sottochiave del filtro di origine è CLSID \_ AsyncReader, il CLSID del filtro di [origine file (Async)](file-source--async--filter.md) .

Ogni voce può avere più quadruple; tutte devono corrispondere. Nell'esempio seguente, i primi 4 byte del file devono essere 0xAB, 0xCD, 0x12, 0x34; e gli ultimi 4 byte del file devono essere 0xAB, 0xAB, 0x00, 0xAB:


```C++
    0, 4, , ABCD1234,  -4, 4, , ABAB00AB 
```



Inoltre, possono essere presenti più voci in un unico tipo di supporto. È sufficiente una corrispondenza con uno di essi. Questo schema consente un set di maschere alternative. ad esempio, i file con estensione wav che possono o non possono avere un'intestazione RIFF.

> [!Note]  
> Questo schema è simile a quello usato dalla funzione [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile) .

 

## <a name="loading-the-source-filter"></a>Caricamento del filtro di origine

Supponendo che Filter Graph Manager trovi un filtro di origine corrispondente per il file, aggiunge tale filtro al grafo, esegue una query sul filtro per l'interfaccia [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) e chiama [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load). Gli argomenti per il metodo **Load** sono il nome del file e il tipo di supporto, come determinato dal registro di sistema.

Se il gestore del grafo del filtro non riesce a trovare nulla dal registro di sistema, per impostazione predefinita viene usato il filtro di origine file asincrono. In tal caso, imposta il tipo di supporto su **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ None**.

## <a name="custom-file-types-in-windows-media-player"></a>Tipi di file personalizzati in Windows Media Player

Windows Media Player utilizza un set aggiuntivo di voci del registro di sistema. Per ulteriori informazioni, vedere [impostazioni del registro di sistema](../wmp/file-name-extension-registry-settings.md) per l'estensione di file in Windows Media Player SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di filtri DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 
