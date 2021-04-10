---
title: Messaggio di EM_GETIMECOLOR (RichEdit. h)
description: Recupera il colore di composizione IME (Input Method Editor).
ms.assetid: 788ac56c-f2d8-4e9a-8829-b92dcd76e6de
keywords:
- Controlli di Windows Message EM_GETIMECOLOR
topic_type:
- apiref
api_name:
- EM_GETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8a19061651787ff94575f8bc64a69f06d445a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964578"
---
# <a name="em_getimecolor-message"></a>\_Messaggio GETIMECOLOR em

Recupera il colore di composizione IME (Input Method Editor).

> [!Note]  
> Questo messaggio è supportato solo nelle versioni in lingua asiatica di Microsoft Rich Edit 1,0. Non è supportata nelle versioni successive di Rich Edit.

 

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Matrice di quattro elementi di strutture [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) che riceve il colore di composizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.

Se l'operazione ha esito negativo, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





