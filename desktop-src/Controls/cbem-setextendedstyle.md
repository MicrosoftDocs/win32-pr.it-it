---
title: CBEM_SETEXTENDEDSTYLE messaggio (Commctrl.h)
description: Imposta gli stili estesi all'interno di un controllo ComboBoxEx.
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- CBEM_SETEXTENDEDSTYLE di controllo Windows messaggio
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
ms.openlocfilehash: efd1083e838d85f9cb659acb9a28b74a1d8605934be4c53fd72993e7470fad2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527971"
---
# <a name="cbem_setextendedstyle-message"></a>Messaggio CBEM \_ SETEXTENDEDSTYLE

Imposta gli stili estesi all'interno di un controllo ComboBoxEx.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore **DWORD** che indica quali stili in *lParam* devono essere interessati. Verranno modificati solo gli stili estesi in *wParam.* Se questo parametro è zero, tutti gli stili in *lParam* saranno interessati.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore **DWORD** che contiene gli stili estesi del controllo [ComboBoxEx](comboboxex-control-extended-styles.md) da impostare per il controllo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD** che contiene gli stili estesi usati in precedenza per il controllo.

## <a name="remarks"></a>Commenti

*wParam* consente di modificare uno o più stili estesi senza dover recuperare prima gli stili esistenti. Ad esempio, se si passa [**CBES \_ EX \_ NOEDITIMAGE**](comboboxex-control-extended-styles.md) per *wParam* e 0 per *lParam*, lo stile **CBES \_ EX \_ NOEDITIMAGE** verrà cancellato, ma tutti gli altri stili rimarranno invariati.

Se si tenta di impostare uno stile esteso per un controllo ComboBoxEx creato con lo stile [**SIMPLE di \_ CBS,**](combo-box-styles.md) è possibile che non venga ridisegnato correttamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





