---
description: Le funzioni seguenti vengono usate con i set di caratteri.
ms.assetid: 1799f5da-1391-4b6e-ac13-718017a77557
title: Funzioni Unicode e set di caratteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd26edd8931b1a63887816ca07698d779bd0d4d3decceb3b53faf5d499605612
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811712"
---
# <a name="unicode-and-character-set-functions"></a>Funzioni Unicode e set di caratteri

Le funzioni seguenti vengono usate con i set di caratteri.



| Funzione                                                       | Descrizione                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**GetTextCharset**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharset)                       | Recupera un identificatore del set di caratteri per il tipo di carattere attualmente selezionato in un contesto di dispositivo specificato.         |
| [**GetTextCharsetInfo**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharsetinfo)               | Recupera informazioni sul set di caratteri del tipo di carattere attualmente selezionato in un contesto di dispositivo specificato. |
| [**IsDBCSLeadByte**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte)                       | Determina se un carattere specificato è un byte iniziale per l'impostazione predefinita Windows tabella codici ANSI (CP \_ ACP).           |
| [**IsDBCSLeadByteEx**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyteex)                   | Determina se un carattere specificato è potenzialmente un byte iniziale.                                                       |
| [**IsTextUnicode**](/windows/desktop/api/Winbase/nf-winbase-istextunicode)                         | Determina se è probabile che un buffer contenga una forma di testo Unicode.                                                   |
| [**Multibytetowidechar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)             | Mappe una stringa di caratteri in una stringa UTF-16 (carattere wide).                                                          |
| [**TranslateCharsetInfo**](/windows/desktop/api/Wingdi/nf-wingdi-translatecharsetinfo)           | Converte le informazioni sul set di caratteri e imposta tutti i membri di una struttura di destinazione sui valori appropriati.           |
| [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)             | Mappe una stringa UTF-16 (carattere wide) in una nuova stringa di caratteri.                                                      |
| [**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))                       | Non usare.                                                                                                           |
| [**NlsDllCodePageTranslation**](/windows/desktop/api/Gb18030/nf-gb18030-nlsdllcodepagetranslation) | Non usare.                                                                                                           |
| [**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))                       | Non usare.                                                                                                           |



 

 

 
