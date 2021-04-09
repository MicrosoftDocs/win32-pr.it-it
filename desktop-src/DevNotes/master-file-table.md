---
description: La tabella file master (MFT) archivia le informazioni necessarie per recuperare i file da una partizione NTFS.
ms.assetid: 673fb4d0-7b6f-44fe-bfd6-1962e14ccdf5
title: Tabella file master (note per gli sviluppatori)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae8656a44b6dadd7d4ff601ddc64623935f5881
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965919"
---
# <a name="master-file-table"></a>Tabella file master

\[Questo documento si applica solo alla versione 3 dei volumi NTFS.\]

La tabella file master (MFT) archivia le informazioni necessarie per recuperare i file da una partizione NTFS.

Un file può avere uno o più record MFT e può contenere uno o più attributi. In NTFS un riferimento al file è il riferimento del segmento MFT del record del file di base. Per altre informazioni, vedere [**\_ \_ riferimento al segmento MFT**](mft-segment-reference.md).

Il file MFT contiene segmenti di record di file; i primi 16 di questi elementi sono riservati per i file speciali, ad esempio:

-   0: MFT ($Mft)
-   5: directory radice ( \\ )
-   6: file di allocazione cluster del volume ($Bitmap)
-   8: file del cluster non valido ($BadClus)

Ogni segmento di record di file inizia con un'intestazione di segmento di record di file. Per altre informazioni, vedere [**\_ intestazione del \_ segmento \_ di record di file**](file-record-segment-header.md). Ogni segmento di record di file è seguito da uno o più attributi. Ogni attributo inizia con un'intestazione di record di attributo. Per altre informazioni, vedere [**\_ \_ header record attribute**](attribute-record-header.md). Il record di attributo include il tipo di attributo, ad esempio $DATA o $BITMAP, un nome facoltativo e il valore dell'attributo. Il flusso di dati utente è un attributo, così come tutti i flussi. L'elenco di attributi viene terminato con 0xFFFFFFFF ($END).

Di seguito sono riportati alcuni attributi di esempio.

-   Il file di $Mft contiene un attributo $DATA senza nome che corrisponde alla sequenza dei segmenti di record MFT, in ordine.
-   Il file di $Mft contiene un attributo $BITMAP senza nome che indica quali record MFT sono in uso.
-   Il file di $Bitmap contiene un attributo $DATA senza nome che indica i cluster in uso.
-   Il file di $BadClus contiene un attributo $DATA denominato $BAD contenente una voce corrispondente a ogni cluster non valido.

Quando non è più disponibile spazio per l'archiviazione degli attributi nel segmento di record di file, i segmenti di record di file aggiuntivi vengono allocati e inseriti nel primo segmento di record di file (o base) in un attributo denominato elenco attributi. L'elenco di attributi indica dove è possibile trovare ogni attributo associato al file. Sono inclusi tutti gli attributi nel record del file di base, ad eccezione dell'elenco di attributi. Per ulteriori informazioni, vedere [**\_ \_ voce elenco attributi**](attribute-list-entry.md).

Le strutture correlate a MFT includono quanto segue:

-   [**\_voce elenco \_ attributi**](attribute-list-entry.md)
-   [**\_intestazione record \_ attributo**](attribute-record-header.md)
-   [**\_nome file**](file-name.md)
-   [**\_ \_ intestazione segmento record \_ file**](file-record-segment-header.md)
-   [**\_riferimento al segmento MFT \_**](mft-segment-reference.md)
-   [**\_intestazione multisettore \_**](multi-sector-header.md)
-   [**\_informazioni standard**](standard-information.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento tecnico per NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))
</dt> </dl>

 

 
