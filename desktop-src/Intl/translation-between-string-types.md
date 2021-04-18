---
description: Le funzioni elencate nella tabella seguente consentono di convertire le stringhe di caratteri da un tipo stringa a un altro.
ms.assetid: 26802339-6291-4767-b468-68a9e8e95774
title: Conversione tra tipi di stringa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877721f2d8ce3852011786e487598e3fd068c9eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312852"
---
# <a name="translation-between-string-types"></a>Conversione tra tipi di stringa

Le funzioni elencate nella tabella seguente consentono di convertire le stringhe di caratteri da un tipo stringa a un altro.



| Funzione                                           | Descrizione                                             |
|----------------------------------------------------|---------------------------------------------------------|
| [**Della funzione FoldString**](/windows/win32/api/stringapiset/nf-stringapiset-foldstringw)                   | Converte una stringa di caratteri in un'altra.             |
| [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                 | Esegue il mapping di una stringa di caratteri in base alle impostazioni locali.                      |
| [**Tounicode**](/windows/win32/api/winuser/nf-winuser-tounicode)              | Converte un codice di chiave virtuale in un carattere Unicode. |
| [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) | Esegue il mapping di una stringa multibyte a una stringa Unicode.            |
| [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) | Esegue il mapping di una stringa Unicode a una stringa multibyte.            |



 

Le funzioni [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) e [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) sono particolarmente utili per le applicazioni che supportano più tipi di stringa. ANSI C definisce anche le funzioni di conversione **wcstombs** e **mbstowcs**, ma possono solo eseguire la conversione da e verso il set di caratteri supportato dalla libreria C standard.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Unicode nell'API Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
