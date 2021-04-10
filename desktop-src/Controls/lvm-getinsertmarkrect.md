---
title: Messaggio LVM_GETINSERTMARKRECT (COMmctrl. h)
description: Recupera il rettangolo che delimita il punto di inserimento.
ms.assetid: 7b10229c-73ab-426c-8a8a-71258a33e248
keywords:
- Controlli di Windows Message LVM_GETINSERTMARKRECT
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd85bfb94f6425d2666372fd141b531fcb238643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964745"
---
# <a name="lvm_getinsertmarkrect-message"></a>\_Messaggio GETINSERTMARKRECT LVM

Recupera il rettangolo che delimita il punto di inserimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Non utilizzato; deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Puntatore a una struttura <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> che contiene le coordinate di un rettangolo che delimita il punto di inserimento.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti.



| Codice restituito                                                                      | Descrizione                          |
|----------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**0**</dt> </dl> | Nessun punto di inserimento trovato.<br/> |
| <dl> <dt>**1**</dt> </dl> | Trovato punto di inserimento.<br/>    |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

