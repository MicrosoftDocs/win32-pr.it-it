---
title: Costanti di inserimento tocco
description: Questa sezione fornisce le specifiche di riferimento per le costanti touch injection.
ms.assetid: 52941DF1-88AF-452B-BF3E-838ADBDBC9B2
topic_type:
- apiref
api_name:
- MAX_TOUCH_COUNT
- TOUCH_FEEDBACK_DEFAULT
- TOUCH_FEEDBACK_INDIRECT
- TOUCH_FEEDBACK_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: d86af0d67c48218e8cb3f5909b647ff59d8b0cdddddef24057e02521a7f253ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451741"
---
# <a name="touch-injection-constants"></a>Costanti di inserimento tocco

Questa sezione fornisce le specifiche di riferimento per le [costanti touch injection.](touch-injection-portal.md)

| Costante/valore | Descrizione |
|---|---|
| **MAX_TOUCH_COUNT** 256                            | Specifica il numero massimo di contatti simultanei.<br/> |
| **TOUCH_FEEDBACK_DEFAULT** 0x1    | Specifica le visualizzazioni tocco predefinite.<br/>                |
| **TOUCH_FEEDBACK_INDIRECT** 0x2 | Specifica le visualizzazioni tocco indirette.<br/>               |
| **TOUCH_FEEDBACK_NONE** 0x3             | Non specifica visualizzazioni tocco.<br/>                     |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato | \[Windows 8 solo app desktop\]                                           |
| Server minimo supportato | \[Windows Server 2012 solo app desktop\]                                 |
| Intestazione                   | Winuser |

## <a name="see-also"></a>Vedi anche

[Informazioni di riferimento sul tocco injection](touch-injection-reference.md)
