---
title: Messaggio CCM_SETVERSION (COMmctrl. h)
description: Questo messaggio viene usato per informare il controllo che si prevede un comportamento associato a una particolare versione.
ms.assetid: f87b20bc-0139-4d0a-b38c-32c75743d6f6
keywords:
- Controlli di Windows Message CCM_SETVERSION
topic_type:
- apiref
api_name:
- CCM_SETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 349935173c41cd9c90a016ef3d2f3c77df8f159c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048526"
---
# <a name="ccm_setversion-message"></a>\_Messaggio della versione CCM

Questo messaggio viene usato per informare il controllo che si prevede un comportamento associato a una particolare versione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di versione.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la versione specificata nel messaggio precedente **della \_ versione CCM** . Se *wParam* è impostato su un valore maggiore della versione della dll corrente, restituisce-1.

## <a name="remarks"></a>Commenti

In alcuni casi, un controllo può comportarsi in modo diverso, a seconda della versione. Questo vale principalmente per i bug risolti nelle versioni successive. Il messaggio della **\_ versione CCM** consente di informare il controllo del comportamento previsto. È possibile determinare la versione specificata inviando un messaggio [**CCM \_ GetVersion**](ccm-getversion.md) . Per un esempio di come usare questo messaggio, vedere [Custom disegnato With List-View and Tree-View Controls](custom-draw.md).

Se ComCtl32.dll versione 6 è installata, indipendentemente dal valore impostato in *wParam*, il messaggio della versione **CCM \_** restituisce la versione 6.

> [!Note]  
> Questo messaggio consente di impostare solo il numero di versione per il controllo a cui viene inviato.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





