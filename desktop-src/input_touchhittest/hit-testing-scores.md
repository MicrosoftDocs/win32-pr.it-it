---
title: Punteggi di hit testing tocco
description: Le costanti seguenti identificano i punteggi di hit test possibili per un oggetto, rispetto ad altri oggetti che intersecano l'area di contatto tocco.
ms.assetid: EACDE6DB-ADBD-4F0C-8C31-7321AB6A73EA
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_PROXIMITY_CLOSEST
- TOUCH_HIT_TESTING_PROXIMITY_FARTHEST
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 18b321272637f4e6931bdc9115e64f8b0553e90e94d8013147ca7a577bad1eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758013"
---
# <a name="touch-hit-testing-scores"></a>Punteggi di hit testing tocco

Le costanti seguenti identificano i punteggi di hit test possibili per un oggetto, rispetto ad altri oggetti che intersecano l'area di contatto tocco.

| Costante/valore | Descrizione |
|---|---|
| **TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0      | L'oggetto è la destinazione più probabile.<br/>  |
| **TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF | L'oggetto è la destinazione meno probabile.<br/> |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | Winuser |
