---
title: Messaggio LVM_GETOUTLINECOLOR (COMmctrl. h)
description: Recupera il colore del bordo di un controllo di visualizzazione elenco se \_ \_ è impostato lo stile della finestra estesa LVS ex BORDERSELECT.
ms.assetid: cc9d69d1-1470-4eaa-8d54-e31b796cf685
keywords:
- Controlli di Windows Message LVM_GETOUTLINECOLOR
topic_type:
- apiref
api_name:
- LVM_GETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489f21f2f6d4dcca2c79d92a13a85d7718a85693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874322"
---
# <a name="lvm_getoutlinecolor-message"></a>\_Messaggio GETOUTLINECOLOR LVM

Recupera il colore del bordo di un controllo di visualizzazione elenco se è impostato lo stile della finestra estesa [**LVS \_ ex \_ BORDERSELECT**](extended-list-view-styles.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce una struttura **COLORREF** che contiene il colore del bordo di un controllo di visualizzazione elenco.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





