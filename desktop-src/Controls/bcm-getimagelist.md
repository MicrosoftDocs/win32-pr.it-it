---
title: Messaggio BCM_GETIMAGELIST (COMmctrl. h)
description: Ottiene la \_ struttura ImageList del pulsante che descrive l'elenco di immagini assegnato a un controllo Button. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Button Getimagine.
ms.assetid: 79383758-53d4-4955-b472-befd338cbec6
keywords:
- Controlli di Windows Message BCM_GETIMAGELIST
topic_type:
- apiref
api_name:
- BCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0c28e997e23d6df63150fe2283d04be1a8c0d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476996"
---
# <a name="bcm_getimagelist-message"></a>\_Messaggio GETimagine BCM

Ottiene la [**struttura \_ ImageList del pulsante**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) che descrive l'elenco di immagini assegnato a un controllo Button. È possibile inviare questo messaggio in modo esplicito o usare la macro [**Button \_ getimagine**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) .

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

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





