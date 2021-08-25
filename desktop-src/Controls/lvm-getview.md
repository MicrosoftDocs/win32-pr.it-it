---
title: LVM_GETVIEW messaggio (Commctrl.h)
description: Recupera la visualizzazione corrente di un controllo visualizzazione elenco.
ms.assetid: dd63e726-3a7f-40e7-8d46-4680816c02a3
keywords:
- LVM_GETVIEW dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- LVM_GETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431b0a7b3fba9a45370c372347285489a56082c4a04396c273a45c4da41b05b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915511"
---
# <a name="lvm_getview-message"></a>Messaggio \_ LVM GETVIEW

Recupera la visualizzazione corrente di un controllo visualizzazione elenco.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD** che specifica la visualizzazione corrente.

## <a name="remarks"></a>Commenti

Di seguito sono riportati i valori per le visualizzazioni.

-   DETTAGLI DELLA \_ VISUALIZZAZIONE \_ LV
-   ICONA VISUALIZZAZIONE \_ \_ LV
-   ELENCO DI VISUALIZZAZIONE LV \_ \_
-   VISUALIZZAZIONE LV \_ \_ SMALLICON
-   RIQUADRO \_ VISUALIZZAZIONE LV \_

> [!Note]  
> Per usare questo messaggio, è necessario fornire un manifesto che specifica Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





