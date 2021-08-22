---
description: NTFS archivia i nomi di file in Unicode. Al contrario, i file system FAT12, FAT16 e FAT32 meno recenti usano il set di caratteri OEM. Per altre informazioni, vedere Tabelle codici.
ms.assetid: 4573dd3b-ad68-460c-bc0f-ff65d4b70860
title: Set di caratteri usati nei nomi di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dad9033b3ea723de757c59a73fc62c91a56da286ca74ca7444f31db42ff539f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107381"
---
# <a name="character-sets-used-in-file-names"></a>Set di caratteri usati nei nomi di file

NTFS archivia i nomi di file in Unicode. Al contrario, i file system FAT12, FAT16 e FAT32 meno recenti usano il set di caratteri OEM. Per altre informazioni, vedere [Tabelle codici](code-pages.md).

Le applicazioni non Unicode che creano file FAT talvolta devono usare le funzioni di conversione standard della libreria di runtime C per eseguire la conversione tra il set di caratteri della tabella codici Windows e il set di caratteri della tabella codici OEM. Con le implementazioni Unicode delle file system, non è necessario eseguire tali traduzioni.

L'applicazione può usare tipi stringa generici, come descritto in Windows [tipi di dati per le stringhe](windows-data-types-for-strings.md). L'applicazione può anche usare prototipi di funzione generici usando le tecniche descritte in [Convenzioni per i prototipi di funzione](conventions-for-function-prototypes.md). Per i tipi di stringa generici o i prototipi di funzione generici, l'applicazione può usare un singolo file di origine per compilare una versione Unicode o non Unicode. A tale scopo, l'applicazione fornisce macro per le funzioni che non vengono richiamate durante la compilazione per Unicode.

Nei file system NTFS e FAT, i caratteri speciali del nome file sono: \\ '', '/', '.', '?' e \* ''. Nelle code pages OEM questi caratteri speciali sono nell'intervallo di caratteri ASCII (da 0x00 a 0x7F). Gli equivalenti Unicode sono gli stessi valori in formato a 2 byte, 0x0000 a 0x007F.

> [!Caution]  
> Windows tabella codici e i set di caratteri della tabella codici OEM usati nei sistemi operativi in lingua giapponese contengono il simbolo Di dollaro (¥) anziché una barra rovesciata ( \\ ). Di conseguenza, il simbolo Dello yen è un carattere non consentito per i file system NTFS e FAT. Quando si esegue il mapping di Unicode a una tabella codici in lingua giapponese, [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) e altre funzioni di conversione eseguano il mapping di entrambe le barre rovesciate (U+005C) e del normale simbolo Unicode Unicode (U+00A5) allo stesso carattere. Per motivi di sicurezza, le applicazioni non devono in genere consentire il carattere U+00A5 in una stringa Unicode che potrebbe essere convertita per l'uso come nome di file FAT. Per altre informazioni, vedere [Considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Unicode nell'API Windows](unicode-in-the-windows-api.md)
</dt> <dt>

[Considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md)
</dt> </dl>

 

 



