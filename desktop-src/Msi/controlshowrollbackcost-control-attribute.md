---
description: Questo attributo specifica se i file di backup di rollback vengono inclusi nei costi visualizzati dal controllo VolumeCostList.
ms.assetid: a3ed4d8a-170b-4708-afc2-03d2a5b665a3
title: Attributo controlShowRollbackCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a888df328062a81637b36dc3fcfbe178d6e49bd4aee01c65b2d2e3524fb321
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379926"
---
# <a name="controlshowrollbackcost-control-attribute"></a>Attributo controlShowRollbackCost

Questo attributo specifica se i file di backup di rollback vengono inclusi nei costi visualizzati dal [controllo VolumeCostList](volumecostlist-control.md).

Se questo bit è impostato e [**la proprietà PROMPTROLLBACKCOST**](promptrollbackcost.md) è impostata su P, i file di backup di rollback vengono inclusi nel costo visualizzato dal [controllo VolumeCostList](volumecostlist-control.md).

Se questo bit non è impostato e la proprietà [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = P, i file di backup di rollback non vengono inclusi nel costo visualizzato dal [controllo VolumeCostList](volumecostlist-control.md).

## <a name="valid-controls"></a>Controlli validi

[VolumeCostList](volumecostlist-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                         |
|---------|-------------|----------------------------------|
| 4194304 | 0x00400000  | **msidbControlShowRollbackCost** |



 

## <a name="remarks"></a>Commenti

Questo attributo di controllo viene ignorato [**se PROMPTROLLBACKCOST**](promptrollbackcost.md) = D o F.

Se [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F, il costo del rollback include i file di backup.

Se [**la proprietà PROMPTROLLBACKCOST**](promptrollbackcost.md) = D o [**DISABLEROLLBACK**](-disablerollback.md) = 1, il costo del rollback non include i file di backup.

 

 



