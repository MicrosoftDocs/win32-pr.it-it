---
description: I tipi di formato testo dei dati configurabili possono essere stringhe di testo di qualsiasi lunghezza. I valori Null incorporati non sono consentiti.
ms.assetid: 71b89f87-43ba-41cd-a969-765d45da4ba4
title: Tipi di formato testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a77ef5e6948320deba8df992e2cf9447cbda82d6a20fc4329f97e761f425164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626331"
---
# <a name="text-format-types"></a>Tipi di formato testo

I tipi di formato testo dei dati configurabili possono essere stringhe di testo di qualsiasi lunghezza. I valori Null incorporati non sono consentiti.

Esistono i tipi di formato testo seguenti:

[Testo arbitrario](arbitrary-text-type.md)

[Rtf](rtf-type.md)

[Formattato](formatted-type.md)

[Enumerazione](enum-type.md)

[Tipo di identificatore](identifier-type.md)

Gli elementi configurabili del tipo di formato testo vengono usati nei campi di database non binari e in generale possono essere sostituiti da qualsiasi stringa di qualsiasi lunghezza. Tuttavia, anche particolari elementi configurabili hanno restrizioni semantiche. Ad esempio, un elemento configurabile che deve essere una chiave esterna in una tabella specifica ha restrizioni semantiche aggiuntive. Queste restrizioni semantiche non vengono applicate da Mergemod.dll e pertanto gli autori di moduli devono essere preparati a gestire qualsiasi stringa che soddisfi il tipo di formato testo specificato.

 

 



