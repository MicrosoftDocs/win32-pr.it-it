---
description: Le funzioni elencate nella tabella seguente traducono le stringhe di caratteri da un tipo stringa a un altro.
ms.assetid: 26802339-6291-4767-b468-68a9e8e95774
title: Conversione tra tipi di stringa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b62ae39307e92c203441ea8ddb9dc61b394a02622e3c86a8949b59539588585
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631921"
---
# <a name="translation-between-string-types"></a>Conversione tra tipi di stringa

Le funzioni elencate nella tabella seguente traducono le stringhe di caratteri da un tipo stringa a un altro.



| Funzione                                           | Descrizione                                             |
|----------------------------------------------------|---------------------------------------------------------|
| [**FoldString**](/windows/win32/api/stringapiset/nf-stringapiset-foldstringw)                   | Converte una stringa di caratteri in un'altra.             |
| [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                 | Mappe una stringa di caratteri in base alle impostazioni locali.                      |
| [**ToUnicode**](/windows/win32/api/winuser/nf-winuser-tounicode)              | Converte un codice di chiave virtuale in un carattere Unicode. |
| [**Multibytetowidechar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) | Mappe una stringa multibyte in una stringa Unicode.            |
| [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) | Mappe una stringa Unicode in una stringa multibyte.            |



 

Le [**funzioni WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) e [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) sono particolarmente utili per le applicazioni che supportano diversi tipi di stringa. ANSI C definisce anche le funzioni di conversione **wcstombs** e **mbstowcs**, ma possono solo eseguire la conversione da e verso il set di caratteri supportato dalla libreria C standard.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Unicode nell'API Windows](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
