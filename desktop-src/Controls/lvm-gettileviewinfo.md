---
title: LVM_GETTILEVIEWINFO messaggio (Commctrl.h)
description: Recupera informazioni su un controllo visualizzazione elenco nella visualizzazione affiancata.
ms.assetid: 114990c0-a150-49d8-80e7-b084c648ac34
keywords:
- LVM_GETTILEVIEWINFO di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_GETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6923f47e4a185ac036a3462a2691036573e8ddfedef9b5f9ab1327ce8204b85f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575691"
---
# <a name="lvm_gettileviewinfo-message"></a>Messaggio LVM \_ GETTILEVIEWINFO

Recupera informazioni su un controllo visualizzazione elenco nella visualizzazione affiancata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**una struttura LVTILEVIEWINFO**</a> che riceve le informazioni recuperate.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore restituito non usato.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per usare questo messaggio, è necessario fornire un manifesto che specifica Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





