---
title: Messaggio LVM_SETOUTLINECOLOR (COMmctrl. h)
description: Imposta il colore del bordo di un controllo di visualizzazione elenco se \_ \_ è impostato lo stile della finestra estesa LVS ex BORDERSELECT.
ms.assetid: c2b606fa-8d47-4192-94b7-d01c3cfdc514
keywords:
- Controlli di Windows Message LVM_SETOUTLINECOLOR
topic_type:
- apiref
api_name:
- LVM_SETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 776cb13479e4d091d394941844691c117a4ebbef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873318"
---
# <a name="lvm_setoutlinecolor-message"></a>\_Messaggio SETOUTLINECOLOR LVM

Imposta il colore del bordo di un controllo di visualizzazione elenco se è impostato lo stile della finestra estesa [**LVS \_ ex \_ BORDERSELECT**](extended-list-view-styles.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Struttura **COLORREF** che specifica il colore per l'impostazione del bordo.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la struttura **COLORREF** che contiene il colore del contorno.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





