---
description: La tabella dei file master (MFT) archivia le informazioni necessarie per recuperare i file da una partizione NTFS.
ms.assetid: 673fb4d0-7b6f-44fe-bfd6-1962e14ccdf5
title: Tabella file master (note per gli sviluppatori)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded28a9655c6d3cbba21449b15bd70cf5a24b17e3864dc1b525cb5f6e4e32fca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955750"
---
# <a name="master-file-table"></a>Tabella file master

\[Questo documento si applica solo alla versione 3 dei volumi NTFS.\]

La tabella dei file master (MFT) archivia le informazioni necessarie per recuperare i file da una partizione NTFS.

Un file può avere uno o più record MFT e può contenere uno o più attributi. In NTFS, un riferimento al file è il riferimento al segmento MFT del record del file di base. Per altre informazioni, vedere [**MFT \_ SEGMENT \_ REFERENCE**](mft-segment-reference.md).

L'MFT contiene segmenti di record di file. i primi 16 sono riservati a file speciali, ad esempio:

-   0: MFT ($Mft)
-   5: directory radice ( \\ )
-   6: file di allocazione cluster di volumi ($Bitmap)
-   8: file del cluster non valido ($BadClus)

Ogni segmento di record di file inizia con un'intestazione di segmento di record di file. Per altre informazioni, vedere [**FILE \_ RECORD SEGMENT \_ \_ HEADER**](file-record-segment-header.md). Ogni segmento di record di file è seguito da uno o più attributi. Ogni attributo inizia con un'intestazione di record dell'attributo. Per altre informazioni, vedere [**ATTRIBUTE \_ RECORD \_ HEADER**](attribute-record-header.md). Il record dell'attributo include il tipo di attributo (ad esempio $DATA o $BITMAP), un nome facoltativo e il valore dell'attributo. Il flusso di dati utente è un attributo, così come tutti i flussi. L'elenco di attributi viene terminato con 0xFFFFFFFF ($END).

Di seguito sono riportati alcuni attributi di esempio.

-   Il $Mft file contiene un attributo $DATA senza nome che è la sequenza di segmenti di record MFT, nell'ordine indicato.
-   Il $Mft file contiene un attributo $BITMAP nome che indica quali record MFT sono in uso.
-   Il $Bitmap file contiene un attributo $DATA che indica quali cluster sono in uso.
-   Il $BadClus file contiene un $DATA denominato $BAD che contiene una voce che corrisponde a ogni cluster non valido.

Quando non è disponibile più spazio per l'archiviazione degli attributi nel segmento di record di file, vengono allocati e inseriti segmenti di record di file aggiuntivi nel primo segmento di record di file (o di base) in un attributo denominato elenco di attributi. L'elenco di attributi indica dove è possibile trovare ogni attributo associato al file. Sono inclusi tutti gli attributi nel record del file di base, ad eccezione dell'elenco di attributi stesso. Per altre informazioni, vedere [**ATTRIBUTE \_ LIST \_ ENTRY**](attribute-list-entry.md).

Le strutture correlate all'MFT includono quanto segue:

-   [**VOCE \_ \_ DELL'ELENCO ATTRIBUTI**](attribute-list-entry.md)
-   [**INTESTAZIONE \_ RECORD \_ ATTRIBUTO**](attribute-record-header.md)
-   [**NOME \_ FILE**](file-name.md)
-   [**INTESTAZIONE \_ SEGMENTO RECORD \_ \_ FILE**](file-record-segment-header.md)
-   [**INFORMAZIONI DI RIFERIMENTO SUL \_ SEGMENTO \_ MFT**](mft-segment-reference.md)
-   [**INTESTAZIONE \_ MULTI \_ SETTORE**](multi-sector-header.md)
-   [**INFORMAZIONI \_ STANDARD**](standard-information.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento tecniche su NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))
</dt> </dl>

 

 
