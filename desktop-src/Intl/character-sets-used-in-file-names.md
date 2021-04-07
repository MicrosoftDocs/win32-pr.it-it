---
description: NTFS archivia i nomi di file in formato Unicode. Al contrario, i file system FAT12, FAT16 e FAT32 precedenti utilizzano il set di caratteri OEM. Per altre informazioni, vedere Tabelle codici.
ms.assetid: 4573dd3b-ad68-460c-bc0f-ff65d4b70860
title: Set di caratteri utilizzati nei nomi file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79394c92b2886f715299855aae27f15753dc86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882749"
---
# <a name="character-sets-used-in-file-names"></a>Set di caratteri utilizzati nei nomi file

NTFS archivia i nomi di file in formato Unicode. Al contrario, i file system FAT12, FAT16 e FAT32 precedenti utilizzano il set di caratteri OEM. Per altre informazioni, vedere [Tabelle codici](code-pages.md).

Le applicazioni non Unicode che creano file FAT talvolta devono usare le funzioni di conversione della libreria di runtime C standard per tradurre tra il set di caratteri della tabella codici di Windows e il set di caratteri della tabella codici OEM. Con le implementazioni Unicode delle funzioni file system, non è necessario eseguire tali traduzioni.

L'applicazione può usare tipi stringa generici, come descritto in [tipi di dati di Windows per le stringhe](windows-data-types-for-strings.md). L'applicazione può anche usare i prototipi di funzione generici usando le tecniche descritte in [convenzioni per i prototipi di funzione](conventions-for-function-prototypes.md). Per i tipi di stringa generici o per i prototipi di funzione generica, l'applicazione può usare un unico file di origine per compilare una versione Unicode o non Unicode. Per consentire questa operazione, l'applicazione fornisce macro per le funzioni che non vengono richiamate durante la compilazione per Unicode.

Nei file system NTFS e FAT, i caratteri speciali per il nome file sono:' \\ ','/',' .','?' è \* '. Nelle tabelle codici OEM questi caratteri speciali si trovano nell'intervallo di caratteri ASCII (da 0x00 a 0x7F). Gli equivalenti Unicode sono gli stessi valori in formato a 2 byte, 0x0000 tramite 0x007F.

> [!Caution]  
> I set di caratteri della tabella codici di Windows e della tabella codici OEM usati nei sistemi operativi in lingua giapponese contengono il simbolo Yen (¥) invece di una barra rovesciata ( \\ ). Il simbolo Yen è quindi un carattere non consentito per i file system NTFS e FAT. Quando si esegue il mapping di Unicode a una tabella codici in lingua giapponese, [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) e altre funzioni di conversione mappano sia la barra rovesciata (u + 005C) che il normale simbolo di yen Unicode (u + 00A5) a questo stesso carattere. Per motivi di sicurezza, le applicazioni non dovrebbero in genere consentire il carattere U + 00A5 in una stringa Unicode che potrebbe essere convertita per essere usata come nome file FAT. Per ulteriori informazioni, vedere [considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Unicode nell'API Windows](unicode-in-the-windows-api.md)
</dt> <dt>

[Considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md)
</dt> </dl>

 

 



