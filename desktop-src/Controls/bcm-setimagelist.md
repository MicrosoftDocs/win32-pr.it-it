---
title: Messaggio BCM_SETIMAGELIST (COMmctrl. h)
description: Assegna un elenco di immagini a un controllo Button. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Button.
ms.assetid: 805d2d9b-3e8f-4323-abaf-0dd5765cd740
keywords:
- Controlli di Windows Message BCM_SETIMAGELIST
topic_type:
- apiref
api_name:
- BCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bdf29735958f3c40af544bca4b946458df8431
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048266"
---
# <a name="bcm_setimagelist-message"></a>\_Messaggio SUBimage di BCM

Assegna un elenco di immagini a un controllo Button. È possibile inviare questo messaggio in modo esplicito o [**usare \_ la macro Button**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura del [**pulsante \_ ImageList**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) che contiene informazioni sull'elenco di immagini.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, restituisce **true**. In caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

L'elenco di immagini a cui si fa riferimento nel membro **himl** della struttura [**\_ ImageList del pulsante**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) deve contenere una singola immagine da usare per tutti gli Stati o singole immagini per ogni stato. Gli Stati seguenti sono definiti in vssym32. h.

``` syntax
enum PUSHBUTTONSTATES {
    PBS_NORMAL = 1,
    PBS_HOT = 2,
    PBS_PRESSED = 3,
    PBS_DISABLED = 4,
    PBS_DEFAULTED = 5,
    PBS_STYLUSHOT = 6,
};
```

Si noti che PBS \_ STYLUSHOT viene utilizzato solo nei computer tablet.

Ogni valore è un indice dell'immagine appropriata nell'elenco immagini. Se è presente una sola immagine, viene usata per tutti gli Stati. Se l'elenco di immagini contiene più di un'immagine, ogni indice corrisponde a uno stato del pulsante. Se non viene specificata un'immagine per ogni stato, non viene disegnato alcun elemento per tali Stati senza immagini.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





