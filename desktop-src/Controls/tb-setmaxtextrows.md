---
title: Messaggio TB_SETMAXTEXTROWS (COMmctrl. h)
description: Imposta il numero massimo di righe di testo visualizzate su un pulsante della barra degli strumenti.
ms.assetid: a14d74e8-cc21-482d-9bca-38dc7c0528ec
keywords:
- Controlli di Windows Message TB_SETMAXTEXTROWS
topic_type:
- apiref
api_name:
- TB_SETMAXTEXTROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0984c0b73280ec90c4e659d3bb3b4cc89cdcf4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963938"
---
# <a name="tb_setmaxtextrows-message"></a>TB \_ SETMAXTEXTROWS messaggio

Imposta il numero massimo di righe di testo visualizzate su un pulsante della barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero massimo di righe di testo che è possibile visualizzare.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Per fare in modo che il testo venga incapsulato, è necessario impostare la larghezza massima del pulsante inviando un messaggio [**\_ SETBUTTONWIDTH TB**](tb-setbuttonwidth.md) . Il testo viene incapsulato in corrispondenza di una parola break; le interruzioni di riga (" \\ n") nel testo vengono ignorate. Il testo nelle \_ barre degli strumenti dell'elenco TBSTYLE viene sempre visualizzato su una sola riga.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





