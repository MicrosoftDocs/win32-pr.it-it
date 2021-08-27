---
description: LINGUA \_ DELLE IMPOSTAZIONI LOCALI
ms.assetid: 8f80a941-8ba6-4a0d-92fa-77230fe0a9d1
title: LOCALE_ILANGUAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3159fe26ce1af7291c5990a07297e7513144b5187b55c00086bf46e452ef188c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106651"
---
# <a name="locale_ilanguage"></a>LINGUA \_ DELLE IMPOSTAZIONI LOCALI

[Identificatore di](language-identifiers.md) lingua con valore esadecimale. Ad esempio, inglese (Stati Uniti) ha il valore 0409, che indica 0x0409 esadecimale e equivale a 1033 decimale. Il numero massimo di caratteri consentiti per questa stringa è cinque, incluso un carattere Null di terminazione.

**Windows Vista e versioni successive:** L'uso di questa costante può causare la restituzione di un identificatore delle impostazioni locali non valido da parte di [**GetLocaleInfo.**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) L'applicazione deve usare la [costante \_ LOCALE SNAME](locale-sname.md) quando chiama questa funzione.

 

 



