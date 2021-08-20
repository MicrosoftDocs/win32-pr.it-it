---
description: I tipi di formato Integer dei dati configurabili possono essere utilizzati in campi di database di tipo text o integer. L'attributo msmConfigItemNonNullable è implicito in questo formato di dati e non deve essere impostato. Null non è mai un valore valido per questo tipo.
ms.assetid: 63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d
title: Tipi di formato Integer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cf5d4ad0d7ef9ba8adb1ddb919e284dbd2a10b2eafc7c43f72d6d0ee777f743
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805629"
---
# <a name="integer-format-types"></a>Tipi di formato Integer

I tipi di formato Integer dei dati configurabili possono essere utilizzati in campi di database di tipo text o integer. L'attributo msmConfigItemNonNullable è implicito in questo formato di dati e non deve essere impostato. Null non è mai un valore valido per questo tipo.

Esiste il tipo Integer Format seguente.

[Tipo Integer arbitrario](arbitrary-integer-type.md)

Gli elementi configurabili del tipo di formato Integer vengono usati in colonne di tipo text o integer e in generale possono essere sostituiti da qualsiasi numero intero positivo o negativo. Tuttavia, elementi configurabili specifici possono avere anche restrizioni semantiche di caratteristica. Ad esempio, un particolare elemento configurabile che deve essere un numero intero compreso tra 0 e 100 ha una restrizione semantica aggiuntiva. Tali restrizioni non vengono applicate da Mergemod.dll e pertanto gli autori di moduli devono essere preparati a gestire qualsiasi stringa che soddisfi il tipo integer specificato.

 

 



