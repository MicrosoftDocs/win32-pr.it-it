---
title: Messaggio LVM_GETTILEVIEWINFO (COMmctrl. h)
description: Recupera le informazioni su un controllo visualizzazione elenco nella visualizzazione affiancata.
ms.assetid: 114990c0-a150-49d8-80e7-b084c648ac34
keywords:
- Controlli di Windows Message LVM_GETTILEVIEWINFO
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
ms.openlocfilehash: bfe1f34da560d539a9ae12cc7a065b2bf37bc3c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742983"
---
# <a name="lvm_gettileviewinfo-message"></a>\_Messaggio GETTILEVIEWINFO LVM

Recupera le informazioni su un controllo visualizzazione elenco nella visualizzazione affiancata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a una struttura <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> che riceve le informazioni recuperate.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore restituito non utilizzato.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





