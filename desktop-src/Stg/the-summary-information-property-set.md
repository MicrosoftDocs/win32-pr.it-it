---
title: Set di proprietà Summary Information
description: COM definisce un set di proprietà comuni standard per l'archiviazione di informazioni di riepilogo sui documenti.
ms.assetid: ceed6d66-7327-4781-a5dc-9058e671138a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54f942d0c7f6c7d1ebc37feda80d55420ea6c8aaf896f4df15df2a5b7e7c0ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886827"
---
# <a name="the-summary-information-property-set"></a>Set di proprietà Summary Information

COM definisce un set di proprietà comuni standard per l'archiviazione di informazioni di riepilogo sui documenti. Il set di proprietà Informazioni di riepilogo deve essere archiviato in un oggetto flusso. In altri parole, questo set di proprietà deve essere archiviato come set di proprietà semplice. Per altre informazioni, vedere [oggetti Archiviazione e Stream per un set di proprietà.](storage-vs--stream-for-a-property-set.md)

Ad esempio, per creare un set di proprietà ansi semplice, è necessario chiamare [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) per creare il set di proprietà, specificando **PROPSETFLAG \_ ANSI** (simple è il tipo predefinito di set di proprietà), quindi scrivere nel set con una chiamata a [**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Per leggere il set di proprietà, chiamare [**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple).

Tutti i set di proprietà condivise sono identificati da un flusso o da un nome di archiviazione con il prefisso \\ "005" (o 0x05) per mostrare che si tratta di un set di proprietà che può essere condiviso tra le applicazioni. Il set di proprietà Informazioni di riepilogo non fa eccezione. Il nome del flusso che contiene il set di proprietà Summary Information è: **" \\ 005SummaryInformation"**

Non è necessario conoscere il nome del flusso del set di proprietà quando vi si accede tramite i metodi [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) o [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) dell'interfaccia [**IPropertySetStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) in questo caso è necessario conoscere solo l'identificatore di formato (FMTID). FmTID per il set di proprietà Summary Information è: **F29F85E0-4FF9-1068-AB91-08002B27B3D9**

La dichiarazione per questo valore è disponibile nel file di intestazione **come FMTID \_ SummaryInformation.** Per altre informazioni, vedere FMTIDS in [Identificatori di formato dei set di proprietà predefiniti.](predefined-property-set-format-identifiers.md)

Nella tabella seguente sono elencati i nomi delle proprietà stringa per il set di proprietà Informazioni di riepilogo, insieme ai rispettivi identificatori di proprietà e indicatori del tipo di variabile (VT). I nomi non vengono in genere archiviati nel set di proprietà, ma vengono dedotto dal valore ID proprietà. Le voci property ID String mostrate di seguito corrispondono alle definizioni trovate nei file di intestazione.

| Nome | Stringa ID proprietà | ID proprietà | Tipo VT |
|------|--------------------|-------------|---------|
| Titolo | TITOLO \_ PIDSI | 0x00000002 | VT \_ LPSTR  |
| Oggetto | SOGGETTO \_ PIDSI | 0x00000003 | VT \_ LPSTR |
| Autore | AUTORE \_ PIDSI | 0x00000004 | VT \_ LPSTR |
| Parole chiave | PAROLE CHIAVE \_ PIDSI | 0x00000005 | VT \_ LPSTR |
| Commenti | COMMENTI \_ PIDSI | 0x00000006 | VT \_ LPSTR |
| Modello | MODELLO \_ PIDSI | 0x00000007 | VT \_ LPSTR |
| Autore ultimo salvataggio | PIDSI \_ LASTAUTHOR | 0x00000008 | VT \_ LPSTR |
| Revision Number | PIDSI \_ REVNUMBER | 0x00000009 | VT \_ LPSTR |
| Tempo di modifica totale | PIDSI \_ EDITTIME | 0x0000000a | VT \_ FILETIME (UTC) |
| Ultima stampa | PIDSI \_ LASTPRINTED | 0x0000000B | VT \_ FILETIME (UTC) |
| Crea ora/data (vedere la nota seguente) | PIDSI \_ CREATE \_ DTM | 0x0000000C | VT \_ FILETIME (UTC) |
| Data/ora ultimo salvataggio (vedere la nota seguente) | PIDSI \_ LASTSAVE \_ DTM | 0x0000000D | VT \_ FILETIME (UTC) |
| Numero di pagine | PIDSI \_ PAGECOUNT | 0x0000000E | VT \_ I4 |
| Numero di parole | PIDSI \_ WORDCOUNT | 0x0000000F | VT \_ I4 |
| Numero di caratteri | PIDSI \_ CHARCOUNT | 0x00000010 | VT \_ I4 |
| Anteprima | ANTEPRIMA \_ PIDSI | 0x00000011 | VT \_ CF |
| Nome dell'applicazione di creazione | PIDSI \_ APPNAME | 0x00000012 | VT \_ LPSTR |
| Sicurezza | SICUREZZA \_ PIDSI | 0x00000013 | VT \_ I4 |

> [!NOTE]
> Per **Create Time/Date** e **Last saved Time/Date**, alcuni metodi di trasferimento di file, ad esempio un download da un servizio BBS, non mantengono correttamente la versione file system di queste informazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Implementazione del set di proprietà Summary Information](implementing-the-summary-information-property-set.md)
</dt> </dl>

 

 




