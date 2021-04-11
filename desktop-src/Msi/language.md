---
description: Il tipo di dati Language è una stringa di testo contenente uno o più ID di lingua numerici validi. Se sono presenti due o più ID lingua, devono essere separati da virgole.
ms.assetid: 547fc662-f055-421e-a621-eecdfa0b13f6
title: Linguaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87cb8b88dc3a693eee6890276adb67ad359e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226124"
---
# <a name="language"></a>Linguaggio

Il tipo di dati Language è una stringa di testo contenente uno o più ID di lingua numerici validi. Se sono presenti due o più ID lingua, devono essere separati da virgole.

Il tipo di dati Language è un valore a 16 bit costituito dalla combinazione di ID numerici primari e sottolinguaggi. Il LANGID primario include i bit da 0 a 9 mentre l'ID del sottolingua è BITS da 10 a 15. Per un elenco degli identificatori numerici primari e secondari, vedere l'argomento relativo alle [costanti e alle stringhe dell'identificatore di lingua](../intl/language-identifier-constants-and-strings.md) .

Per gli ID della lingua primaria, l'intervallo da 0x200 a 0x3FF è definibile dall'utente. L'intervallo da 0x000 a 0x1FF è riservato per l'utilizzo da parte del sistema. Per gli ID del linguaggio secondario, l'intervallo da 0x20 a 0x3F è definibile dall'utente. L'intervallo da 0x00 a 0x1F è riservato per l'utilizzo da parte del sistema.

 

 
