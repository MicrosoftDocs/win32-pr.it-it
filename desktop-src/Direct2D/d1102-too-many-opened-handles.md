---
title: D1102 Troppi handle aperti
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: È stato trovato un numero elevato di interfacce non riasseedate. Attualmente sono presenti interfacce non assegnate allocate da questa DLL.
keywords:
- D1102 Troppi handle aperti Direct2D
topic_type:
- apiref
api_name:
- D1102 Too Many Opened Handles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2d59e110aece56a31af71e75e9a8eca0bb008961
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548686"
---
# <a name="d1102-too-many-opened-handles"></a>D1102: Troppi handle aperti

È stato trovato un numero elevato di interfacce non riasseedate. Attualmente questa DLL allocare un numero di interfacce \[  \] non ritirate.

## <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="number"></span><span id="NUMBER"></span>*Numero*
</dt> <dd>

Numero di interfacce non assegnate allocate da questa DLL.

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Livello di errore | Avviso |



 

## <a name="possible-causes"></a>Possibili cause

È stato creato un numero elevato di risorse. Anche se Direct2D non ha limiti superiori per il numero di risorse disponibili (ad eccezione della memoria), il livello di debug genererà questo messaggio informativo quando rileva 1001 oggetti live, 2001 oggetti live o 3001 oggetti live e così via, perché ciò potrebbe indicare una perdita nell'applicazione.

 

 




