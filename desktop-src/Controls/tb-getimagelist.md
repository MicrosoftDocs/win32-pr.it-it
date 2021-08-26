---
title: TB_GETIMAGELIST messaggio (Commctrl.h)
description: Recupera l'elenco di immagini utilizzato da un controllo barra degli strumenti per visualizzare i pulsanti nello stato predefinito. Un controllo barra degli strumenti usa questo elenco di immagini per visualizzare i pulsanti quando non sono attiva o disabilitati.
ms.assetid: 21edde99-019b-495c-a38b-4d686e124f8e
keywords:
- TB_GETIMAGELIST di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dee13a7099a1781722b1d2cb6028fe2bc8e22bc712992283148e72a628269a98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918841"
---
# <a name="tb_getimagelist-message"></a>TB \_ GETIMAGELIST message

Recupera l'elenco di immagini utilizzato da un controllo barra degli strumenti per visualizzare i pulsanti nello stato predefinito. Un controllo barra degli strumenti usa questo elenco di immagini per visualizzare i pulsanti quando non sono attiva o disabilitati.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per l'elenco di immagini oppure **NULL se** non è impostato alcun elenco di immagini.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





