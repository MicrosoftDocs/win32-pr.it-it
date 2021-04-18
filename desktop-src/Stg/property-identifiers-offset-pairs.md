---
title: Coppie di identificatori di proprietà/offset
description: In seguito al conteggio delle proprietà, il valore del set di proprietà è una matrice di coppie di identificatori di proprietà/coppie di offset.
ms.assetid: 341608a1-3ab1-4fa9-ab9a-4124c63c78a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b55ed20aef2c76dc97fcb3f4acfe981b9800308
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298973"
---
# <a name="property-identifiersoffset-pairs"></a>Coppie di identificatori di proprietà/offset

In seguito al conteggio delle proprietà, il valore del set di proprietà è una matrice di coppie di identificatori di proprietà/coppie di offset. Gli identificatori di proprietà sono valori a 32 bit che identificano in modo univoco una proprietà all'interno di una sezione. Le coppie di offset indicano la distanza tra l'inizio della sezione e l'inizio della coppia tipo/valore della proprietà. Poiché gli offset sono relativi alla sezione, le sezioni possono essere copiate come una matrice di byte.

Gli identificatori di proprietà non sono ordinati in base a un ordine particolare. Le proprietà possono essere omesse dal set di proprietà archiviato; i lettori non devono basarsi su un ordine o un intervallo specifico di identificatori di proprietà.

 

 




