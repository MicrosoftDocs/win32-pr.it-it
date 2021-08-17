---
title: LVM_SETOUTLINECOLOR messaggio (Commctrl.h)
description: Imposta il colore del bordo di un controllo visualizzazione elenco se lo stile della finestra estesa LVS \_ EX \_ BORDERSELECT è impostato.
ms.assetid: c2b606fa-8d47-4192-94b7-d01c3cfdc514
keywords:
- LVM_SETOUTLINECOLOR di controllo Windows messaggio
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
ms.openlocfilehash: 5db9f5d53339ecec19fd6f06fcabd3a0471b1c3a569e8856571a98a99675a232
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119217391"
---
# <a name="lvm_setoutlinecolor-message"></a>Messaggio LVM \_ SETOUTLINECOLOR

Imposta il colore del bordo di un controllo visualizzazione elenco se lo stile della finestra estesa [**LVS \_ EX \_ BORDERSELECT**](extended-list-view-styles.md) è impostato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>**Struttura COLORREF** che specifica il colore per impostare il bordo.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **la struttura COLORREF** che contiene il colore del contorno.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per usare questo messaggio, è necessario fornire un manifesto che specifica Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





