---
title: TB_GETBITMAPFLAGS messaggio (Commctrl.h)
description: Recupera i flag che descrivono il tipo di bitmap da utilizzare.
ms.assetid: 64a66fe6-1446-424c-a0c6-388da6a7b081
keywords:
- TB_GETBITMAPFLAGS controlli di Windows messaggio
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
ms.openlocfilehash: 97b9bce2f6e9bf862b10b162bf9172c0144d15c07328b61cbdb79bcf05c759e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670029"
---
# <a name="tb_getbitmapflags-message"></a>TB \_ GETBITMAPFLAGS message

Recupera i flag che descrivono il tipo di bitmap da utilizzare.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD** che descrive il tipo di bitmap da utilizzare. Se per questo valore restituito è impostato il flag LARGE di TBBF, le applicazioni devono usare bitmap di grandi dimensioni (24 x 24). In caso contrario, le applicazioni devono usare bitmap di piccole dimensioni \_ (16 x 16). Tutti gli altri bit sono riservati.

## <a name="remarks"></a>Commenti

Il valore restituito **da TB \_ GETBITMAPFLAGS** è solo un avviso. Il controllo barra degli strumenti consiglia bitmap di grandi o piccole dimensioni a seconda che l'utente abbia scelto tipi di carattere di piccole o grandi dimensioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





