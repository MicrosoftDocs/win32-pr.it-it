---
title: Messaggio LVM_SETICONSPACING (COMmctrl. h)
description: Imposta la spaziatura tra le icone nei controlli visualizzazione elenco con lo \_ stile dell'icona LVS. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetIconSpacing di ListView.
ms.assetid: 2dd3d9df-5b0d-445e-9201-d766fa218f90
keywords:
- Controlli di Windows Message LVM_SETICONSPACING
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
ms.openlocfilehash: 972435190ec21bb50db90640a589cef1e394318c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873321"
---
# <a name="lvm_seticonspacing-message"></a>\_Messaggio SETICONSPACING LVM

Imposta la spaziatura tra le icone nei controlli visualizzazione elenco con lo stile dell' [**\_ icona LVS**](list-view-window-styles.md) . È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetIconSpacing di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la distanza in pixel da impostare tra le icone sull'asse x. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la distanza in pixel da impostare tra le icone sull'asse y. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **DWORD** che contiene la distanza precedente dell'asse x nella parola bassa e la distanza dell'asse y precedente nella parola alta.

## <a name="remarks"></a>Commenti

I valori per *lParam* sono relativi all'angolo superiore sinistro di una bitmap icona. Pertanto, per impostare la spaziatura tra le icone che non si sovrappongono, i valori *lParam* devono includere le dimensioni dell'icona, più la quantità di spazio vuoto che si desidera tra le icone. I valori che non includono la larghezza dell'icona provocheranno sovrapposizioni.

Quando si definisce la spaziatura delle icone, è necessario che i valori *lParam* siano impostati su 4 o più grandi. I valori più piccoli non restituiranno il layout desiderato. Per reimpostare le icone sulla spaziatura predefinita, impostare i valori *lParam* su-1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

