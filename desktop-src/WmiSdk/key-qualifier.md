---
description: Il qualificatore Key indica se la proprietà fa parte dell'handle dello spazio dei nomi.
ms.assetid: 838d295f-e812-4e46-99a4-d2714a0ae8dc
ms.tgt_platform: multiple
title: Qualificatore di chiave
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
ms.openlocfilehash: 9ae5525aa85ab744e7e6824bb6079511a3611643d53594503e70c8e587f363cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555891"
---
# <a name="key-qualifier"></a>Qualificatore di chiave

Il **qualificatore Key** indica se la proprietà fa parte dell'handle dello spazio dei nomi. Se più proprietà hanno il **qualificatore Key,** tutte queste proprietà formano collettivamente la chiave (una chiave composta). Quando vengono riunite, le proprietà chiave devono fornire un riferimento univoco per ogni istanza della classe. Se questo qualificatore viene inserito in una proprietà, è consentito solo il valore **TRUE.**

È possibile usare qualsiasi tipo di proprietà, ad eccezione dei seguenti:

-   Matrici
-   Numeri reali e a virgola mobile
-   Oggetti incorporati
-   Caratteri inferiori a ASCII 32 (ovvero spazi vuoti)
-   Le stringhe di caratteri **di tipo char16** o le stringhe di caratteri definite come chiavi devono contenere valori maggiori di U+0020. Ciò è dovuto al fatto che WMI usa i valori chiave nei percorsi degli oggetti e non è possibile utilizzare caratteri non stampabili in un percorso oggetto.

Quando una classe padre specifica una chiave, tutte le classi derivate dalla classe padre ereditano tale chiave. Le classi derivate non possono modificare la chiave ereditata né definire una nuova proprietà della chiave. Tuttavia, quando si deriva una sottoclasse da una classe astratta senza una chiave, è possibile introdurre una chiave nella sottoclasse.

Tutte le classi che definiscono più di un'istanza devono specificare una chiave. Poiché le classi astratte non definiscono istanze, non è necessario specificare chiavi. Poiché le classi singleton definiscono una sola istanza, non possono specificare chiavi.

Le chiavi vengono scritte una sola volta al momento della creazione dell'istanza dell'oggetto e non devono essere modificate in un secondo momento. Non ha senso applicare un valore predefinito a una proprietà qualificata con chiave.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



 

 




