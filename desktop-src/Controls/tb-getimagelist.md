---
title: Messaggio TB_GETIMAGELIST (COMmctrl. h)
description: Recupera l'elenco di immagini utilizzato da un controllo Toolbar per visualizzare i pulsanti nello stato predefinito. Un controllo toolbar utilizza questo elenco immagini per visualizzare i pulsanti quando non sono attivi o disabilitati.
ms.assetid: 21edde99-019b-495c-a38b-4d686e124f8e
keywords:
- Controlli di Windows Message TB_GETIMAGELIST
topic_type:
- apiref
api_name:
- TB_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a56b8b847bd212e703d3b512b255cf1693abf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740274"
---
# <a name="tb_getimagelist-message"></a>TB \_ messaggio GETimagine

Recupera l'elenco di immagini utilizzato da un controllo Toolbar per visualizzare i pulsanti nello stato predefinito. Un controllo toolbar utilizza questo elenco immagini per visualizzare i pulsanti quando non sono attivi o disabilitati.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per l'elenco di immagini oppure **null** se non è impostato alcun elenco di immagini.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





