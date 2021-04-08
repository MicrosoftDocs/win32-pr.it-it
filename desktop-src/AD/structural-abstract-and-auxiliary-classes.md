---
title: Classi strutturali, astratte e ausiliarie
description: L'attributo objectClassCategory di un oggetto classSchema può avere un valore, come elencato nella tabella seguente, che indica se la classe è strutturale, astratta o ausiliaria.
ms.assetid: 5af740cb-b292-4d80-abe5-3e3d194758f3
ms.tgt_platform: multiple
keywords:
- Classi strutturali, astratte e ausiliarie AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561bc836794b45b6c028fe8da772b0b38d0936a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044090"
---
# <a name="structural-abstract-and-auxiliary-classes"></a>Classi strutturali, astratte e ausiliarie

L'attributo **objectClassCategory** di un oggetto **classSchema** può avere un valore, come elencato nella tabella seguente, che indica se la classe è strutturale, astratta o ausiliaria.



| Valore | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Classe strutturale, che è l'unico tipo di classe in cui possono essere presenti istanze in Active Directory Domain Services. Una classe strutturale può essere una sottoclasse di una classe astratta o strutturale. Una classe strutturale può includere un numero qualsiasi di classi ausiliarie nella relativa definizione.                                                                                                                                                                                                                                           |
| 2     | Una classe astratta, ovvero un modello usato per derivare nuove classi astratte, ausiliarie e strutturali. Una classe astratta può essere solo una sottoclasse di una classe astratta. Impossibile creare un'istanza delle classi astratte in Active Directory Domain Services. Una classe astratta può includere un numero qualsiasi di classi ausiliarie nella relativa definizione.                                                                                                                                                                                   |
| 3     | Una classe ausiliaria, che può essere inclusa nella definizione di una classe strutturale, astratta o ausiliaria, nel qual caso i valori **mustContain**, **systemMustContain**, **mayContain** e **systemMayContain** della classe ausiliaria vengono aggiunti a quelli della classe. Una classe ausiliaria può essere una sottoclasse di una classe astratta o ausiliaria. Non è possibile creare un'istanza delle classi ausiliarie in Active Directory Domain Services. Una classe ausiliaria può includere un numero qualsiasi di classi ausiliarie nella relativa definizione. |



 

Non confondere **objectClassCategory** con una [categoria di oggetti](object-class-and-object-category.md).

 

 




