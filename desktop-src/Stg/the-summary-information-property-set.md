---
title: Set di proprietà delle informazioni di riepilogo
description: COM definisce un set di proprietà comuni standard per archiviare le informazioni di riepilogo sui documenti.
ms.assetid: ceed6d66-7327-4781-a5dc-9058e671138a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb318daba7e0ad03ff176853877fe416ddeda799
ms.sourcegitcommit: fc240ac77d4c40a9f3a27714d7b852abbd234774
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/12/2019
ms.locfileid: "104397034"
---
# <a name="the-summary-information-property-set"></a>Set di proprietà delle informazioni di riepilogo

COM definisce un set di proprietà comuni standard per archiviare le informazioni di riepilogo sui documenti. Il set di proprietà informazioni di riepilogo deve essere archiviato in un oggetto flusso. Questo set di proprietà deve essere archiviato come un semplice set di proprietà. Per altre informazioni, vedere [oggetti di archiviazione e di flusso per un set di proprietà](storage-vs--stream-for-a-property-set.md).

Ad esempio, per creare un set di proprietà semplice ANSI, è necessario chiamare [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) per creare il set di proprietà, specificando **PROPSETFLAG \_ ANSI** (Simple è il tipo predefinito del set di proprietà), quindi scrivere in tale set con una chiamata a [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Per leggere il set di proprietà, è necessario chiamare [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple).

Tutti i set di proprietà condivisi sono identificati da un flusso o da un nome di archiviazione con prefisso " \\ 005" (o 0x05) per indicare che si tratta di un set di proprietà che può essere condiviso tra le applicazioni. Il set di proprietà informazioni di riepilogo non è un'eccezione. Il nome del flusso che contiene il set di proprietà informazioni di riepilogo è: **" \\ 005SummaryInformation"**

Non è necessario che conosca il nome del flusso della proprietà impostata quando viene eseguito l'accesso tramite i metodi [**create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) o [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) dell'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) . in questo caso è necessario conoscere solo l'identificatore di formato (FMTID). Il FMTID per il set di proprietà informazioni di riepilogo è: **F29F85E0-4FF9-1068-AB91-08002B27B3D9**

La dichiarazione per questo valore è disponibile nel file di intestazione come **fmtid \_ SummaryInformation**. Per ulteriori informazioni, vedere FMTIDS negli [identificatori di formato di set di proprietà predefiniti](predefined-property-set-format-identifiers.md).

Nella tabella seguente sono elencati i nomi delle proprietà di stringa per il set di proprietà informazioni di riepilogo, insieme ai rispettivi identificatori di proprietà e gli indicatori di tipo di variabile (VT). I nomi non vengono in genere archiviati nel set di proprietà, ma vengono dedotti dal valore ID della proprietà. Le voci di stringa ID proprietà indicate di seguito corrispondono alle definizioni trovate nei file di intestazione.

| Nome | Stringa ID proprietà | ID proprietà | Tipo di VT |
|------|--------------------|-------------|---------|
| Titolo | \_titolo PIDSI | 0x00000002 | \_LPSTR VT  |
| Oggetto | \_oggetto PIDSI | 0x00000003 | \_LPSTR VT |
| Autore | autore di PIDSI \_ | 0x00000004 | \_LPSTR VT |
| Parole chiave | \_parole chiave PIDSI | 0x00000005 | \_LPSTR VT |
| Commenti | \_Commenti PIDSI | 0x00000006 | \_LPSTR VT |
| Modello | \_modello PIDSI | 0x00000007 | \_LPSTR VT |
| Autore ultimo salvataggio | \_LASTAUTHOR PIDSI | 0x00000008 | \_LPSTR VT |
| Revision Number | \_REVNUMBER PIDSI | 0x00000009 | \_LPSTR VT |
| Tempo di modifica totale | \_EDITTIME PIDSI | 0x0000000A | FILETIME VT \_ (UTC) |
| Ultima stampa | \_LASTPRINTED PIDSI | 0x0000000B | FILETIME VT \_ (UTC) |
| Data/ora di creazione (vedere la nota sotto) | PIDSI \_ creare \_ DTM | 0x0000000C | FILETIME VT \_ (UTC) |
| Data/ora dell'ultimo salvataggio (vedere la nota di seguito) | PIDSI \_ LASTSAVE \_ DTM | 0x0000000D | FILETIME VT \_ (UTC) |
| Numero di pagine | \_PageCount PIDSI | 0x0000000E | VT \_ I4 |
| Numero di parole | \_WORDCOUNT PIDSI | 0x0000000F | VT \_ I4 |
| Numero di caratteri | \_charCount PIDSI | 0x00000010 | VT \_ I4 |
| Anteprima | \_Anteprima PIDSI | 0x00000011 | VT \_ CF |
| Nome della creazione dell'applicazione | PIDSI \_ appname | 0x00000012 | \_LPSTR VT |
| Sicurezza | \_sicurezza PIDSI | 0x00000013 | VT \_ I4 |

> [!NOTE]
> Per **la** **data e l'ora dell'ultimo salvataggio**, alcuni metodi di trasferimento di file, ad esempio un download da una BBS, non mantengono la versione file System delle informazioni corrette.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Implementazione del set di proprietà informazioni di riepilogo](implementing-the-summary-information-property-set.md)
</dt> </dl>

 

 




