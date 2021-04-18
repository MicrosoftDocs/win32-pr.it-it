---
title: Messaggio CBEM_SETEXTENDEDSTYLE (COMmctrl. h)
description: Imposta gli stili estesi in un controllo ComboBoxEx.
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- Controlli di Windows Message CBEM_SETEXTENDEDSTYLE
topic_type:
- apiref
api_name:
- CBEM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a60518d2f6130c2c89e379125308fc2e647c6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302524"
---
# <a name="cbem_setextendedstyle-message"></a>\_Messaggio CBEM SETEXTENDEDSTYLE

Imposta gli stili estesi in un controllo ComboBoxEx.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore **DWORD** che indica quali stili in *lParam* devono essere interessati. Solo gli stili estesi in *wParam* verranno modificati. Se questo parametro è zero, saranno interessati tutti gli stili in *lParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Valore **DWORD** che contiene gli [stili estesi del controllo ComboBoxEx](comboboxex-control-extended-styles.md) da impostare per il controllo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **DWORD** che contiene gli stili estesi usati in precedenza per il controllo.

## <a name="remarks"></a>Commenti

*wParam* consente di modificare uno o più stili estesi senza dover prima recuperare gli stili esistenti. Se ad esempio si passa [**CBES \_ ex \_ NOEDITIMAGE**](comboboxex-control-extended-styles.md) per *wParam* e 0 per *lParam*, lo stile **CBES \_ ex \_ NOEDITIMAGE** verrà cancellato, ma tutti gli altri stili rimarranno invariati.

Se si tenta di impostare uno stile esteso per un controllo ComboBoxEx creato con lo [**stile \_ semplice CBS**](combo-box-styles.md) , è possibile che non venga ridisegnato correttamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





