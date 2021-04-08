---
title: Messaggio LVM_ENABLEGROUPVIEW (COMmctrl. h)
description: Abilita o Disabilita se gli elementi in un controllo visualizzazione elenco vengono visualizzati come gruppo.
ms.assetid: 783a5e23-d1cb-4523-a6d2-b2cf93fa7f62
keywords:
- Controlli di Windows Message LVM_ENABLEGROUPVIEW
topic_type:
- apiref
api_name:
- LVM_ENABLEGROUPVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d546e1236fa4f0800c0353810beb5b427ba4fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047868"
---
# <a name="lvm_enablegroupview-message"></a>\_Messaggio ENABLEGROUPVIEW LVM

Abilita o Disabilita se gli elementi in un controllo visualizzazione elenco vengono visualizzati come gruppo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>**Bool** che indica se abilitare un controllo visualizzazione elenco per raggruppare gli elementi visualizzati. Utilizzare **true** per abilitare il raggruppamento, **false** per disabilitarlo. </dd> <dt>

*lParam* 
</dt> <dd>Deve essere **null**.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti.



| Codice restituito                                                                       | Descrizione                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>  | La possibilità di visualizzare elementi della visualizzazione elenco come gruppo è già abilitata o disabilitata.<br/> |
| <dl> <dt>**1**</dt> </dl>  | Lo stato del controllo è stato modificato correttamente.<br/>                                |
| <dl> <dt>**-1**</dt> </dl> | Operazione non riuscita.<br/>                                                             |



 

## <a name="remarks"></a>Commenti

**LVM \_ ENABLEGROUPVIEW** non è supportato nello stile [**\_ OWNERDATA di LVS**](list-view-window-styles.md) .

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





