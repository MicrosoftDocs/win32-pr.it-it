---
title: Messaggio TB_SETHOTITEM (COMmctrl. h)
description: Imposta l'elemento attivo in una barra degli strumenti.
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- Controlli di Windows Message TB_SETHOTITEM
topic_type:
- apiref
api_name:
- TB_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c477a445cb6aae78dd5d31e8d23b8ec3be8c61ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874209"
---
# <a name="tb_sethotitem-message"></a>TB \_ SETHOTITEM messaggio

Imposta l'elemento attivo in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento che verrà reso attivo. Se questo valore è-1, nessuno degli elementi sarà attivo.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento attivo precedente oppure-1 se non è presente alcun elemento attivo.

## <a name="remarks"></a>Commenti

Il comportamento di questo messaggio non è definito per le barre degli strumenti che non hanno lo stile [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





