---
description: impostazioni locali \_ ILANGUAGE
ms.assetid: 8f80a941-8ba6-4a0d-92fa-77230fe0a9d1
title: LOCALE_ILANGUAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b68ccd270319fa00cd2e983b5f9159d454f160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305633"
---
# <a name="locale_ilanguage"></a>impostazioni locali \_ ILANGUAGE

[Identificatore di lingua](language-identifiers.md) con un valore esadecimale. Ad esempio, l'inglese (Stati Uniti) ha il valore 0409, che indica l'esadecimale 0x0409 ed è equivalente a 1033 Decimal. Il numero massimo di caratteri consentiti per questa stringa è cinque, incluso un carattere di terminazione null.

**Windows Vista e versioni successive:** L'uso di questa costante può causare la restituzione di un identificatore delle impostazioni locali non valido per [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) . Quando si chiama questa funzione, l'applicazione deve usare la costante [ \_ sName delle impostazioni locali](locale-sname.md) .

 

 



