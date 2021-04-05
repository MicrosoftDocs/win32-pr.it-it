---
title: Messaggio TB_GETOBJECT (COMmctrl. h)
description: Recupera l'oggetto IDropTarget per un controllo Toolbar.
ms.assetid: b26394ea-6f0f-4084-956d-f9166cc54b76
keywords:
- Controlli di Windows Message TB_GETOBJECT
topic_type:
- apiref
api_name:
- TB_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce923feaec893e6f4304eb0b993de33dc1fe2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120687"
---
# <a name="tb_getobject-message"></a>TB- \_ messaggio GETobject

Recupera l'oggetto [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) per un controllo Toolbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore dell'interfaccia richiesta. Questo valore deve puntare all' **IID \_ IDropTarget**.

</dd> <dt>

*lParam* 
</dt> <dd>

Indirizzo che riceve il puntatore a interfaccia. Se si verifica un errore, in questo indirizzo viene inserito un puntatore **null** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** che indica l'esito positivo o negativo dell'operazione.

## <a name="remarks"></a>Commenti

Il [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) della barra degli strumenti viene usato dalla barra degli strumenti quando gli oggetti vengono trascinati su di esso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

