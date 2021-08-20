---
description: Il tipo di dati Language è una stringa di testo contenente uno o più ID di lingua numerica validi. Se sono presenti due o più ID lingua, devono essere separati da virgole.
ms.assetid: 547fc662-f055-421e-a621-eecdfa0b13f6
title: Linguaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b98e24ec0ad4d4b42dfcba02374792e10ea117db474a973eae06336a55834538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013129"
---
# <a name="language"></a>Linguaggio

Il tipo di dati Language è una stringa di testo contenente uno o più ID di lingua numerica validi. Se sono presenti due o più ID lingua, devono essere separati da virgole.

Il tipo di dati Language è un valore a 16 bit che rappresenta la combinazione di ID numerici primari e secondari. Il LANGID primario è costituito da bit da 0 a 9, mentre l'ID sottolinguaggio è compreso tra 10 e 15. Per un elenco di identificatori numerici della lingua primaria e secondaria, vedere l'argomento Language [Identifier Constants and Strings](../intl/language-identifier-constants-and-strings.md) (Costanti e stringhe degli identificatori di lingua).

Per gli ID lingua primaria, l'intervallo 0x200 a 0x3ff è definibile dall'utente. L'intervallo 0x000 da 0x1ff è riservato per l'uso da parte del sistema. Per gli ID di sottolinguaggio, l'0x20 da 0x3f è definibile dall'utente. L'intervallo 0x00 da 0x1f è riservato per l'uso da parte del sistema.

 

 
