---
title: EM_SETEDITSTYLE messaggio (Richedit.h)
description: Imposta i flag di stile di modifica correnti per un controllo Rich Edit.
ms.assetid: e48de6b3-0fd2-4791-9863-a6dcdafa3642
keywords:
- EM_SETEDITSTYLE dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06789b1d1fedfc76af205ac46aac7d3ea4bb882f2460676df96cd018d5a216b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048591"
---
# <a name="em_seteditstyle-message"></a>Messaggio EM \_ SETEDITSTYLE

Imposta i flag di stile di modifica correnti per un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica uno o più flag di stile di modifica. Per un elenco dei valori possibili, vedere [**EM \_ GETEDITSTYLE**](em-geteditstyle.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Maschera costituita da uno o più valori *wParam.* Verranno impostati o cancellati solo i valori specificati in questa maschera. In questo modo è possibile impostare o cancellare un singolo flag senza leggere gli stati del flag corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è lo stato dei flag di stile di modifica dopo che il controllo Rich Edit ha tentato di implementare le modifiche dello stile di modifica. I flag di stile di modifica sono un set di flag che indicano lo stile di modifica corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Componente ridistribuibile<br/>          | Rich Edit 3.0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ GETEDITSTYLE**](em-geteditstyle.md)
</dt> </dl>

 

 





