---
title: TB_CHANGEBITMAP messaggio (Commctrl.h)
description: Modifica la bitmap per un pulsante in una barra degli strumenti.
ms.assetid: 112b6f4e-6034-4e13-8b2f-b8411a351fbd
keywords:
- TB_CHANGEBITMAP di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_CHANGEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb75e4586960a68e68c52d01d19ad78a3b3c848dcfb7acbd495dffbe530770c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957940"
---
# <a name="tb_changebitmap-message"></a>TB \_ CHANGEBITMAP message

Modifica la bitmap per un pulsante in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore del comando del pulsante che deve ricevere una nuova bitmap.

</dd> <dt>

*lParam* 
</dt> <dd>

Indice in base zero di un'immagine nell'elenco di immagini della barra degli strumenti. Il sistema visualizza l'immagine specificata nel pulsante. Impostare questo parametro su I IMAGECALLBACK e la barra degli strumenti invierà la notifica \_ [**\_ TBN GETDISPINFO**](tbn-getdispinfo.md) per recuperare l'indice dell'immagine quando necessario.

[Versione 5.81.](common-control-versions.md) Impostare questo parametro su I \_ IMAGENONE per indicare che il pulsante non ha un'immagine. Il layout del pulsante non includerà alcuno spazio per una bitmap, ma solo testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





