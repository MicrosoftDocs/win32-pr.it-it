---
description: Questo articolo descrive in che modo Gestione filtri Graph individua un filtro di origine, dato un nome di file.
ms.assetid: bc0d5719-6325-40fe-8261-ad00b91f272c
title: Registrazione di un tipo di file personalizzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd2815748fafaff3e2d20d0de1ab5fa0bcc9dec62f4e65ffbdd8479fec434d99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697051"
---
# <a name="registering-a-custom-file-type"></a>Registrazione di un tipo di file personalizzato

Questo articolo descrive in che modo Gestione filtri Graph individua un filtro di origine, dato un nome di file. È possibile usare questo meccanismo per registrare tipi di file personalizzati. Dopo aver registrato il tipo di file, DirectShow carica automaticamente il filtro di origine corretto ogni volta che un'applicazione chiama [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) o [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).

-   [Overview](#overview)
-   [Protocolli](#protocols)
-   [Estensione](#file-extensions)
-   [Controlla byte](#check-bytes)
-   [Caricamento del filtro di origine](#loading-the-source-filter)
-   [Tipi di file personalizzati in Windows Media Player](#custom-file-types-in-windows-media-player)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Per individuare un filtro di origine da un determinato nome di file, Filter Graph Manager tenta di eseguire le operazioni seguenti, nell'ordine indicato:

1.  Corrisponde al protocollo, se presente.
2.  Trova la corrispondenza con l'estensione del file.
3.  Corrisponde ai modelli di byte all'interno del file, denominati *byte di controllo.*

## <a name="protocols"></a>Protocolli

I nomi di protocollo, ad esempio "ftp" o "http", vengono registrati nel

**HKEY \_ CLASSES \_ ROOT**

chiave , con la struttura seguente:


```C++
HKEY_CLASSES_ROOT
    <protocol>
        Source Filter = <Source filter CLSID>
        Extensions
            <.ext1> = <Source filter CLSID>
            <.ext2> = <Source filter CLSID>
```



Se il nome file o l'URL contiene i due punti (':'), Filter Graph Manager tenta di usare la parte prima di ':' come nome di protocollo. Ad esempio, se il nome è "myprot://myfile.ext", cerca una chiave del Registro di sistema denominata **myprot**. Se questa chiave esiste e contiene una sottochiave denominata "Extensions", Filter Graph Manager cerca all'interno di tale sottochiave le voci che corrispondono all'estensione di file. Il valore della chiave deve essere un GUID in formato stringa. ad esempio " {00000000-0000-0000-0000-000000000000} ". Se Filter Graph Manager non può corrispondere ad alcun elemento all'interno della sottochiave **Extensions,** cerca una sottochiave denominata **Source Filter,** che deve anche essere un GUID in formato stringa.

Se Gestione filtri Graph trova un GUID corrispondente, lo usa come CLSID del filtro di origine e tenta di caricare il filtro. Se non trova una corrispondenza, usa il filtro Origine file [(URL),](file-source--url--filter.md) che considera il nome del file come URL.

Esistono due eccezioni a questo algoritmo:

-   Per escludere le lettere dei driver, le stringhe a carattere singolo non sono considerate protocolli.
-   Se la stringa è "file:" o "file://", non viene considerata come protocollo.

## <a name="file-extensions"></a>Estensioni di file

Se il nome file non contiene alcun protocollo, Filter Graph Manager cerca nel Registro di sistema le voci con la chiave **HKEY \_ CLASSES ROOT Media \_ Type \\ \\ Extensions \\**.*ext* \\ , dove .*ext è* l'estensione del file. Se questa chiave esiste, il valore **Source Filter** contiene il CLSID del filtro di origine, in formato stringa. Facoltativamente, la chiave può avere valori per **Tipo** di supporto e **Sottotipo**, che forniscono i GUID del tipo principale e del sottotipo.

## <a name="check-bytes"></a>Controlla byte

Alcuni tipi di file possono essere identificati da modelli specifici di bit che si verificano in corrispondenza di offset di byte specifici nel file. Gestione filtri Graph cerca nel Registro di sistema le chiavi con il formato seguente:

**HKEY \_ CLASSES \_ ROOT \\ MediaType \\**{ major *type* } \\ { *subtype* }

dove *il tipo principale* e il *sottotipo* sono GUID che definiscono il tipo di supporto per il flusso di byte. Ogni chiave contiene una o più sottochiavi, in genere denominate 1, 2 e così via, che definiscono i byte di controllo. e una sottochiave denominata **Source Filter che** fornisce il CLSID del filtro di origine, in formato stringa. Le sottochiavi check-byte sono stringhe che contengono uno o più quad di numeri denominati:

*offset*, *cb*, *mask*, *val*

Per trovare la corrispondenza con il file, Il gestore Graph legge i byte cb, a partire dall'offset dei numeri di byte. Esegue quindi un'operazione AND bit per bit sul valore in mask. Se il risultato è uguale a val, il file corrisponde a tale quad. I valori mask e val sono specificati in formato esadecimale. Una voce vuota per mask viene considerata come una stringa di 1 di lunghezza cb. Un valore negativo per offset indica un offset dalla fine del file. Per trovare la corrispondenza con la chiave, il file deve corrispondere a tutti i quad in una delle sottochiavi.

Si supponga, ad esempio, che il Registro di sistema contenga le chiavi seguenti in **HKCR \\ Media Type**:


```C++
{e436eb83-524f-11ce-9f53-0020af0ba770}
    {7364696D-0000-0010-8000-00AA00389B71}
        0                    "0,4,,52494646,8,4,,524D4944"
        1                    "0,4,,4D546864"
        Source Filter        "{E436EBB5-524F-11CE-9F53-0020AF0BA770}"
```



La prima chiave corrisponde al tipo principale MEDIATYPE \_ Stream. Sottochiave seguente che corrisponde al sottotipo MEDIATYPE \_ Midi. Il valore della sottochiave Source Filter è CLSID AsyncReader, il CLSID del filtro di \_ [origine file (Async).](file-source--async--filter.md)

Ogni voce può avere più quadruple. tutti devono corrispondere. Nell'esempio seguente i primi 4 byte del file devono essere 0xAB, 0xCD, 0x12, 0x34; e gli ultimi 4 byte del file devono essere 0xAB, 0xAB, 0x00, 0xAB:


```C++
    0, 4, , ABCD1234,  -4, 4, , ABAB00AB 
```



Possono inoltre essere presenti più voci elencate in un singolo tipo di supporto. È sufficiente una corrispondenza con uno di essi. Questo schema consente un set di maschere alternative. ad esempio file wav che potrebbero avere o meno un'intestazione RIFF.

> [!Note]  
> Questo schema è simile a quello usato dalla [**funzione GetClassFile.**](/windows/win32/api/objbase/nf-objbase-getclassfile)

 

## <a name="loading-the-source-filter"></a>Caricamento del filtro di origine

Supponendo che Filter Graph Manager trovi un filtro di origine corrispondente per il file, aggiunge tale filtro al grafico, esegue una query sul filtro per l'interfaccia [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) e chiama [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load). Gli argomenti del metodo **Load sono** il nome del file e il tipo di supporto, come determinato dal Registro di sistema.

Se Gestione Graph non riesce a trovare alcun elemento dal Registro di sistema, per impostazione predefinita viene utilizzato il filtro Origine file asincrona. In tal caso, imposta il tipo di supporto su **MEDIATYPE \_ Stream**, **MEDIASUBTYPE \_ None**.

## <a name="custom-file-types-in-windows-media-player"></a>Tipi di file personalizzati in Windows Media Player

Windows Media Player usa un set aggiuntivo di voci del Registro di sistema. Per altre informazioni, vedere [File Name Extension Registry Impostazioni](../wmp/file-name-extension-registry-settings.md) in Windows Media Player SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura DirectShow filtri](writing-directshow-filters.md)
</dt> </dl>

 

 
