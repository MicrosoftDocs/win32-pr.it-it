---
description: I tipi di formato integer dei dati configurabili possono essere utilizzati nei campi di database di tipo text o Integer. L'attributo msmConfigItemNonNullable è implicito in questo formato dati e non è necessario impostarlo. Null non è mai un valore valido per questo tipo.
ms.assetid: 63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d
title: Tipi di formato Integer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184ef6380f25474a9e2ad07be7a4eb6d00706aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757034"
---
# <a name="integer-format-types"></a>Tipi di formato Integer

I tipi di formato integer dei dati configurabili possono essere utilizzati nei campi di database di tipo text o Integer. L'attributo msmConfigItemNonNullable è implicito in questo formato dati e non è necessario impostarlo. Null non è mai un valore valido per questo tipo.

Il tipo di formato integer seguente esiste.

[Tipo Integer arbitrario](arbitrary-integer-type.md)

Gli elementi configurabili del tipo di formato integer vengono utilizzati in colonne di tipo text o Integer e in generale potrebbero essere sostituiti da qualsiasi numero intero positivo o negativo. Tuttavia, particolari elementi configurabili possono anche avere restrizioni semantiche caratteristiche. Un particolare elemento configurabile, ad esempio, deve essere un numero intero compreso tra 0 e 100 e una restrizione semantica aggiuntiva. Tali restrizioni non vengono applicate da Mergemod.dll e pertanto gli autori dei moduli devono essere preparati a gestire qualsiasi stringa che soddisfi il tipo di formato integer specificato.

 

 



