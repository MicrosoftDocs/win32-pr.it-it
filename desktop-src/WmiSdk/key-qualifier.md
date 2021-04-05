---
description: Il qualificatore chiave indica se la proprietà fa parte dell'handle dello spazio dei nomi.
ms.assetid: 838d295f-e812-4e46-99a4-d2714a0ae8dc
ms.tgt_platform: multiple
title: Qualificatore chiave
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Key
api_type:
- NA
api_location: ''
ms.openlocfilehash: affc9f4be594723700a65c9c92f8ae37ffead265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758324"
---
# <a name="key-qualifier"></a>Qualificatore chiave

Il qualificatore **chiave** indica se la proprietà fa parte dell'handle dello spazio dei nomi. Se più di una proprietà dispone del qualificatore **chiave** , tutte queste proprietà costituiscono collettivamente la chiave (una chiave composta). Quando vengono rilevate insieme, le proprietà chiave devono fornire un riferimento univoco per ogni istanza della classe. Se questo qualificatore viene inserito in una proprietà, è consentito solo il valore **true** .

È possibile utilizzare qualsiasi tipo di proprietà, ad eccezione di quanto segue:

-   Matrici
-   Numeri reali e a virgola mobile
-   Oggetti incorporati
-   Caratteri inferiori a ASCII 32 (ovvero spazi vuoti)
-   Le stringhe di caratteri di tipo **Char16** o stringhe di caratteri definite come chiavi devono contenere valori maggiori di U + 0020. Questo perché WMI usa i valori di chiave nei percorsi degli oggetti e non è possibile usare caratteri non stampabili in un percorso dell'oggetto.

Quando una classe padre specifica una chiave, tutte le classi derivate dalla classe padre ereditano tale chiave. Le classi derivate non possono modificare la chiave ereditata o definire una nuova proprietà della chiave. Tuttavia, quando si deriva una sottoclasse da una classe astratta senza una chiave, è possibile introdurre una chiave nella sottoclasse.

Tutte le classi che definiscono più istanze devono specificare una chiave. Poiché le classi astratte non definiscono alcuna istanza, non è necessario specificare chiavi. Poiché le classi singleton definiscono solo un'istanza, non possono specificare chiavi.

Le chiavi vengono scritte una volta alla creazione dell'istanza dell'oggetto e non devono essere modificate in un secondo momento. Non ha senso applicare un valore predefinito a una proprietà con chiave qualificata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



 

 




