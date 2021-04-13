---
title: Messaggio di EM_SETEDITSTYLE (RichEdit. h)
description: Imposta i flag di stile di modifica correnti per un controllo Rich Edit.
ms.assetid: e48de6b3-0fd2-4791-9863-a6dcdafa3642
keywords:
- Controlli di Windows Message EM_SETEDITSTYLE
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
ms.openlocfilehash: 14c7b7e1d3990a00fb6931ed39bbd28aa6f8c2ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518670"
---
# <a name="em_seteditstyle-message"></a>\_Messaggio SETEDITSTYLE em

Imposta i flag di stile di modifica correnti per un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica uno o più flag di stile di modifica. Per un elenco di valori possibili, vedere [**em \_ geteditname**](em-geteditstyle.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Maschera costituita da uno o più valori *wParam* . Verranno impostati o cancellati solo i valori specificati in questa maschera. In questo modo è possibile impostare o cancellare un flag singolo senza leggere gli Stati del flag corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è lo stato dei flag di stile di modifica dopo che il controllo Rich Edit ha tentato di implementare le modifiche dello stile di modifica. I flag di stile di modifica sono un set di flag che indicano lo stile di modifica corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Componente ridistribuibile<br/>          | Modifica avanzata 3,0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_geteditin em**](em-geteditstyle.md)
</dt> </dl>

 

 





