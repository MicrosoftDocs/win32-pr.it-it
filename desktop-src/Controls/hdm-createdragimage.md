---
title: Messaggio HDM_CREATEDRAGIMAGE (COMmctrl. h)
description: Crea una versione semi-trasparente dell'immagine di un elemento da utilizzare come immagine di trascinamento. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro CreateDragImage dell'intestazione.
ms.assetid: 1b9dc515-d327-4634-a424-cc15a32f0f7c
keywords:
- Controlli di Windows Message HDM_CREATEDRAGIMAGE
topic_type:
- apiref
api_name:
- HDM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9e801ad9771205b5f2e6df8e37bb0a0ad7f0bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048522"
---
# <a name="hdm_createdragimage-message"></a>\_Messaggio HDM CREATEDRAGIMAGE

Crea una versione semi-trasparente dell'immagine di un elemento da utilizzare come immagine di trascinamento. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ CreateDragImage dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento all'interno del controllo intestazione. L'immagine assegnata a questo elemento rappresenta la base per l'immagine trasparente.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un handle a un elenco di immagini che contiene la nuova immagine come unico elemento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





