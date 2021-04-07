---
description: Questo attributo specifica se i file di backup di rollback sono inclusi nei costi visualizzati dal controllo VolumeCostList.
ms.assetid: a3ed4d8a-170b-4708-afc2-03d2a5b665a3
title: Attributo di controllo ControlShowRollbackCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7947777a356933ab74051163b6b9b023736dbb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883941"
---
# <a name="controlshowrollbackcost-control-attribute"></a>Attributo di controllo ControlShowRollbackCost

Questo attributo specifica se i file di backup di rollback sono inclusi nei costi visualizzati dal [controllo VolumeCostList](volumecostlist-control.md).

Se questo bit è impostato e la proprietà [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = P, i file di backup di rollback sono inclusi nel costo visualizzato dal [controllo VolumeCostList](volumecostlist-control.md).

Se questo bit non è impostato e la proprietà [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = P, i file di backup di rollback non sono inclusi nei costi visualizzati dal [controllo VolumeCostList](volumecostlist-control.md).

## <a name="valid-controls"></a>Controlli validi

[VolumeCostList](volumecostlist-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                         |
|---------|-------------|----------------------------------|
| 4194304 | 0x00400000  | **msidbControlShowRollbackCost** |



 

## <a name="remarks"></a>Commenti

Questo attributo di controllo viene ignorato se [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D o F.

Se [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F, viene incluso il costo del rollback, ovvero i file di backup.

Se [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D o la proprietà [**DisableRollback**](-disablerollback.md) = 1, il costo del rollback non include i file di backup.

 

 



