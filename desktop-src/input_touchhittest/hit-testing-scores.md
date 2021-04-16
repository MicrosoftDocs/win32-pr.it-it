---
title: Punteggi hit testing tocco
description: Le costanti seguenti identificano i possibili punteggi di hit test per un oggetto, rispetto ad altri oggetti che intersecano l'area di contatto tocco.
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
ms.openlocfilehash: f6590e7d56c1c9d92f0ff20524b6e4222d8655b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517619"
---
# <a name="touch-hit-testing-scores"></a>Punteggi hit testing tocco

Le costanti seguenti identificano i possibili punteggi di hit test per un oggetto, rispetto ad altri oggetti che intersecano l'area di contatto tocco.

| Costante/valore | Descrizione |
|---|---|
| **TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0      | L'oggetto è la destinazione più probabile.<br/>  |
| **TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF | L'oggetto è la destinazione meno probabile.<br/> |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | Winuser. h |
