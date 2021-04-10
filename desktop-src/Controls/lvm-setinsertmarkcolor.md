---
title: Messaggio LVM_SETINSERTMARKCOLOR (COMmctrl. h)
description: Imposta il colore del punto di inserimento.
ms.assetid: dce2c266-672b-4682-ba23-51d9a8e1102b
keywords:
- Controlli di Windows Message LVM_SETINSERTMARKCOLOR
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260d21d083e2c70d8e82a27628e42596bd1b37eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963761"
---
# <a name="lvm_setinsertmarkcolor-message"></a>\_Messaggio SETINSERTMARKCOLOR LVM

Imposta il colore del punto di inserimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Struttura **COLORREF** che specifica il colore per impostare il punto di inserimento.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la struttura **COLORREF** impostata sul colore precedente.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





