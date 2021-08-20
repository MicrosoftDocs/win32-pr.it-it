---
title: SB_SETICON messaggio (Commctrl.h)
description: Imposta l'icona per una parte in una barra di stato.
ms.assetid: d8528cd1-54d2-44ba-b0d6-29111f75616a
keywords:
- SB_SETICON di Windows messaggi
topic_type:
- apiref
api_name:
- SB_SETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e08b1c3b0ce1a453ca9050c20552a14169a594c8091708339b4a436f1fb1a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540071"
---
# <a name="sb_seticon-message"></a>Messaggio \_ SETICON SB

Imposta l'icona per una parte in una barra di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della parte che riceverà l'icona. Se questo parametro è -1, si presuppone che la barra di stato sia una semplice barra di stato.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'icona da impostare. Se questo valore è **NULL,** l'icona viene rimossa dalla parte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

La barra di stato non elimina l'icona. È responsabilità dell'applicazione chiamante tenere traccia delle icone ed eliminare le icone.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





