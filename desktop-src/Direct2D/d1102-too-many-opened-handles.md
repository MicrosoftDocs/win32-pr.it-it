---
title: D1102 troppi handle aperti
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: È stato trovato un numero elevato di interfacce non rilasciate. Attualmente sono presenti interfacce non rilasciate allocate da questa DLL.
keywords:
- D1102 troppi handle aperti Direct2D
topic_type:
- apiref
api_name:
- D1102 Too Many Opened Handles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: e3c12c2e2a7b47535e830c6ed65a828a16672bbf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718052"
---
# <a name="d1102-too-many-opened-handles"></a>D1102: troppi handle aperti

È stato trovato un numero elevato di interfacce non rilasciate. Attualmente sono presenti \[ *numero* \] di interfacce non rilasciate allocate da questa dll.

## <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="number"></span><span id="NUMBER"></span>*numero*
</dt> <dd>

Numero di interfacce non rilasciate allocate da questa DLL.

</dd> </dl> 

|             |         |
|-------------|---------|
| Livello di errore | Avviso |



 

## <a name="possible-causes"></a>Possibili cause

È stato creato un numero elevato di risorse. Sebbene Direct2D non abbia un limite superiore per il numero di risorse disponibili (ad eccezione della memoria), il livello di debug emette questo messaggio informativo quando rileva 1001 oggetti attivi, 2001 oggetti attivi o 3001 oggetti attivi, perché questo potrebbe indicare una perdita nell'applicazione.

 

 




