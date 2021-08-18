---
title: Classi strutturali, astratte e ausiliarie
description: L'attributo objectClassCategory di un oggetto classSchema può avere un valore, come elencato nella tabella seguente, che indica se la classe è strutturale, astratta o ausiliaria.
ms.assetid: 5af740cb-b292-4d80-abe5-3e3d194758f3
ms.tgt_platform: multiple
keywords:
- Classi strutturali, astratte e ausiliarie AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393c08f5c26690d5b08b76dfea8ab4ff2833c94851a10ddcea2a69209279fbd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024709"
---
# <a name="structural-abstract-and-auxiliary-classes"></a>Classi strutturali, astratte e ausiliarie

**L'attributo objectClassCategory** di un oggetto **classSchema** può avere un valore, come elencato nella tabella seguente, che indica se la classe è strutturale, astratta o ausiliaria.



| Valore | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Classe strutturale, che è l'unico tipo di classe che può avere istanze in Active Directory Domain Services. Una classe strutturale può essere una sottoclasse di una classe astratta o strutturale. Una classe strutturale può includere un numero qualsiasi di classi ausiliarie nella relativa definizione.                                                                                                                                                                                                                                           |
| 2     | Classe astratta, ovvero un modello usato per derivare nuove classi astratte, ausiliarie e strutturali. Una classe astratta può essere solo una sottoclasse di una classe astratta. Non è possibile creare istanze di classi astratte in Active Directory Domain Services. Una classe astratta può includere un numero qualsiasi di classi ausiliarie nella relativa definizione.                                                                                                                                                                                   |
| 3     | Una classe ausiliaria, che può essere inclusa nella definizione di una classe strutturale, astratta o ausiliaria, nel qual caso i valori **mustContain**, **systemMustContain**, **mayContain** e **systemMayContain** della classe ausiliaria vengono aggiunti a quelli della classe. Una classe ausiliaria può essere una sottoclasse di una classe astratta o ausiliaria. Non è possibile creare un'istanza delle classi ausiliarie in Active Directory Domain Services. Una classe ausiliaria può includere un numero qualsiasi di classi ausiliarie nella relativa definizione. |



 

Non confondere **objectClassCategory** con una [categoria di oggetti](object-class-and-object-category.md).

 

 




