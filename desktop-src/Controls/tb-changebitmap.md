---
title: Messaggio TB_CHANGEBITMAP (COMmctrl. h)
description: Modifica la bitmap per un pulsante in una barra degli strumenti.
ms.assetid: 112b6f4e-6034-4e13-8b2f-b8411a351fbd
keywords:
- Controlli di Windows Message TB_CHANGEBITMAP
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
ms.openlocfilehash: 1367a2a1b4e35d6f52bf1e7a0be42f1e75daa7ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874682"
---
# <a name="tb_changebitmap-message"></a>TB \_ CHANGEBITMAP messaggio

Modifica la bitmap per un pulsante in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore di comando del pulsante che deve ricevere una nuova bitmap.

</dd> <dt>

*lParam* 
</dt> <dd>

Indice in base zero di un'immagine nell'elenco di immagini della barra degli strumenti. Il sistema Visualizza l'immagine specificata nel pulsante. Impostare questo parametro su I \_ IMAGECALLBACK e la barra degli strumenti invierà la notifica [**TBN \_ GETDISPINFO**](tbn-getdispinfo.md) per recuperare l'indice dell'immagine quando necessario.

[Versione 5,81](common-control-versions.md). Impostare questo parametro su I \_ IMAGENONE per indicare che il pulsante non dispone di un'immagine. Il layout del pulsante non includerà alcuno spazio per una bitmap, ma solo per il testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





