---
title: LVM_HASGROUP messaggio (Commctrl.h)
description: Determina se il controllo visualizzazione elenco ha un gruppo specificato.
ms.assetid: 0b8a9208-5221-4f66-8b26-7de55afe485f
keywords:
- LVM_HASGROUP controlli Windows messaggio
topic_type:
- apiref
api_name:
- LVM_HASGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a9dcfadf3e7a07a5f814f5421ed97d26faff6a5ac4c36ce97b9faea77c6a152
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293741"
---
# <a name="lvm_hasgroup-message"></a>Messaggio \_ LVM HASGROUP

Determina se il controllo visualizzazione elenco ha un gruppo specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>ID del gruppo.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere **NULL.**</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se il controllo visualizzazione elenco ha il gruppo specificato oppure FALSE in caso **contrario.**

## <a name="remarks"></a>Commenti

> [!Note]  
> Per usare questo messaggio, è necessario fornire un manifesto che specifica Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





