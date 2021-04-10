---
title: Messaggio TB_GETBITMAPFLAGS (COMmctrl. h)
description: Recupera i flag che descrivono il tipo di bitmap da utilizzare.
ms.assetid: 64a66fe6-1446-424c-a0c6-388da6a7b081
keywords:
- Controlli di Windows Message TB_GETBITMAPFLAGS
topic_type:
- apiref
api_name:
- TB_GETBITMAPFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e21b5b14fa57d6e454c997cbd0e80ac5716d230e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121719"
---
# <a name="tb_getbitmapflags-message"></a>TB \_ GETBITMAPFLAGS messaggio

Recupera i flag che descrivono il tipo di bitmap da utilizzare.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **DWORD** che descrive il tipo di bitmap da usare. Se il valore restituito è \_ impostato su TBBF large flag, le applicazioni devono usare bitmap di grandi dimensioni (24 x 24). in caso contrario, le applicazioni devono usare bitmap di piccole dimensioni (16 x 16). Tutti gli altri bit sono riservati.

## <a name="remarks"></a>Commenti

Il valore restituito da **TB \_ GETBITMAPFLAGS** è solo consultivo. Il controllo Toolbar consiglia le bitmap di grandi dimensioni o piccole in base al fatto che l'utente abbia scelto caratteri di grandi dimensioni o piccoli.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





