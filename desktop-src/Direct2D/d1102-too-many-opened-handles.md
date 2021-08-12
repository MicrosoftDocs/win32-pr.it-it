---
title: D1102 Troppi handle aperti
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: È stato trovato un numero elevato di interfacce non inedito. Attualmente sono presenti interfacce inedito allocate da questa DLL.
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
ms.openlocfilehash: baaa4c46850919aed50897583bfa68c9003bcf496ad884c68cfb57d3e8a90147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666352"
---
# <a name="d1102-too-many-opened-handles"></a>D1102: troppi handle aperti

È stato trovato un numero elevato di interfacce non inedito. Attualmente sono presenti numero di interfacce non assegnate \[  \] allocate da questa DLL.

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

È stato creato un numero elevato di risorse. Anche se Direct2D non ha limiti superiori al numero di risorse disponibili (ad eccezione della memoria), il livello di debug segnala questo messaggio informativo quando rileva 1001 oggetti live, 2001 oggetti live o 3001 oggetti live e così via, perché ciò potrebbe indicare una perdita nell'applicazione.

 

 




