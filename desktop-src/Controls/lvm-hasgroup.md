---
title: Messaggio LVM_HASGROUP (COMmctrl. h)
description: Determina se il controllo di visualizzazione elenco dispone di un gruppo specificato.
ms.assetid: 0b8a9208-5221-4f66-8b26-7de55afe485f
keywords:
- Controlli di Windows Message LVM_HASGROUP
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
ms.openlocfilehash: bb05fed8466188aa0025d2128ce64ad7f1512c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478502"
---
# <a name="lvm_hasgroup-message"></a>\_Messaggio HASGROUP LVM

Determina se il controllo di visualizzazione elenco dispone di un gruppo specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>ID del gruppo.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere **null**.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se il controllo elenco-visualizzazione dispone del gruppo specificato o **false** in caso contrario.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





