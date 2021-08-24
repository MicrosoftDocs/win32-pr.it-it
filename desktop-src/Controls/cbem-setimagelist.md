---
title: CBEM_SETIMAGELIST messaggio (Commctrl.h)
description: Imposta un elenco di immagini per un controllo ComboBoxEx.
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- CBEM_SETIMAGELIST di controllo Windows messaggio
topic_type:
- apiref
api_name:
- CBEM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd83336d27bf8e47900554a6f3c36d2d767e5e8ddd4b8680b50050d87da79bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699261"
---
# <a name="cbem_setimagelist-message"></a>Messaggio CBEM \_ SETIMAGELIST

Imposta un elenco di immagini per un controllo ComboBoxEx.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elenco di immagini da impostare per il controllo .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle all'elenco di immagini associato in precedenza al controllo oppure restituisce **NULL** se in precedenza non è stato impostato alcun elenco di immagini.

## <a name="remarks"></a>Commenti

> [!IMPORTANT]
> L'altezza delle immagini nell'elenco di immagini potrebbe modificare i requisiti di dimensione del controllo ComboBoxEx. È consigliabile ridimensionare il controllo dopo aver inviato questo messaggio per assicurarsi che venga visualizzato correttamente.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





