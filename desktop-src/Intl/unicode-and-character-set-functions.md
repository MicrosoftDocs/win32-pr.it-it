---
description: Le funzioni seguenti vengono utilizzate con i set di caratteri.
ms.assetid: 1799f5da-1391-4b6e-ac13-718017a77557
title: Funzioni del set di caratteri e Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6996139d8a9bb426c21a460ac2bcb1358e6c8e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058075"
---
# <a name="unicode-and-character-set-functions"></a>Funzioni del set di caratteri e Unicode

Le funzioni seguenti vengono utilizzate con i set di caratteri.



| Funzione                                                       | Descrizione                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**GetTextCharset**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharset)                       | Recupera un identificatore del set di caratteri per il tipo di carattere attualmente selezionato in un contesto di dispositivo specificato.         |
| [**GetTextCharsetInfo**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharsetinfo)               | Recupera le informazioni sul set di caratteri del tipo di carattere attualmente selezionato in un contesto di dispositivo specificato. |
| [**IsDBCSLeadByte**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte)                       | Determina se un carattere specificato è un byte di apertura per la tabella codici ANSI di Windows predefinita del sistema (CP \_ ACP).           |
| [**IsDBCSLeadByteEx**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyteex)                   | Determina se un carattere specificato è potenzialmente un byte di apertura.                                                       |
| [**IsTextUnicode**](/windows/desktop/api/Winbase/nf-winbase-istextunicode)                         | Determina se un buffer può contenere un formato di testo Unicode.                                                   |
| [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)             | Esegue il mapping di una stringa di caratteri a una stringa UTF-16 (carattere wide).                                                          |
| [**TranslateCharsetInfo**](/windows/desktop/api/Wingdi/nf-wingdi-translatecharsetinfo)           | Converte le informazioni sul set di caratteri e imposta tutti i membri di una struttura di destinazione sui valori appropriati.           |
| [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)             | Esegue il mapping di una stringa UTF-16 (carattere wide) a una nuova stringa di caratteri.                                                      |
| [**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))                       | Non usare.                                                                                                           |
| [**NlsDllCodePageTranslation**](/windows/desktop/api/Gb18030/nf-gb18030-nlsdllcodepagetranslation) | Non usare.                                                                                                           |
| [**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))                       | Non usare.                                                                                                           |



 

 

 
