---
title: LVM_SETICONSPACING messaggio (Commctrl.h)
description: Imposta la spaziatura tra le icone nei controlli visualizzazione elenco con lo stile \_ LVS ICON. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro ListView SetIconSpacing.
ms.assetid: 2dd3d9df-5b0d-445e-9201-d766fa218f90
keywords:
- LVM_SETICONSPACING dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- LVM_SETICONSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5897b0ca6aec7763cc24a0ea538f336e7a2f737f2ddc0e7cb52a2145e570db47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019178"
---
# <a name="lvm_seticonspacing-message"></a>Messaggio LVM \_ SETICONSPACING

Imposta la spaziatura tra le icone nei controlli visualizzazione elenco con lo [**stile \_ LVS ICON.**](list-view-window-styles.md) È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ ListView SetIconSpacing.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la distanza, in pixel, da impostare tra le icone sull'asse x. La [**parola chiave HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la distanza, in pixel, da impostare tra le icone sull'asse y. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD** che contiene la distanza precedente dell'asse x nella parola bassa e la distanza dell'asse y precedente nella parola alta.

## <a name="remarks"></a>Commenti

I valori *per lParam* sono relativi all'angolo superiore sinistro di una bitmap dell'icona. Pertanto, per impostare la spaziatura tra le icone che non si sovrappongono, i valori *lParam* devono includere le dimensioni dell'icona, oltre alla quantità di spazio vuoto desiderato tra le icone. I valori che non includono la larghezza dell'icona comportano sovrapposizioni.

Quando si definisce la spaziatura delle icone, i *valori lParam* devono essere impostati su 4 o su un valore maggiore. I valori più piccoli non producono il layout desiderato. Per ripristinare la spaziatura predefinita delle icone, impostare *i valori lParam* su -1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

