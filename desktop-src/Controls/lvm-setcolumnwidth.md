---
title: LVM_SETCOLUMNWIDTH messaggio (Commctrl.h)
description: Modifica la larghezza di una colonna in modalità di visualizzazione report o la larghezza di tutte le colonne in modalità visualizzazione elenco. Puoi inviare questo messaggio in modo esplicito o usare la \_ macro ListView SetColumnWidth.
ms.assetid: 309aebfb-9fed-4c77-acbb-ea905b32b0e2
keywords:
- LVM_SETCOLUMNWIDTH del messaggio Windows controlli
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a127706d6a47444ee59f1434478aadb5170f9ac7a919dca6fd6151de33486d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077291"
---
# <a name="lvm_setcolumnwidth-message"></a>Messaggio LVM \_ SETCOLUMNWIDTH

Modifica la larghezza di una colonna in modalità di visualizzazione report o la larghezza di tutte le colonne in modalità visualizzazione elenco. Puoi inviare questo messaggio in modo esplicito o usare la macro [**\_ ListView SetColumnWidth.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero di una colonna valida. Per la modalità di visualizzazione elenco, questo parametro deve essere impostato su zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Nuova larghezza della colonna, in pixel. Per la modalità di visualizzazione report sono supportati i valori speciali seguenti:



| Valore                                                                                                                                                                                           | Significato                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVSCW_AUTOSIZE"></span><span id="lvscw_autosize"></span><dl> <dt>**LVSCW \_ AUTOSIZE**</dt> </dl>                                | Ridimensiona automaticamente la colonna.<br/>                                                                                                                                           |
| <span id="LVSCW_AUTOSIZE_USEHEADER"></span><span id="lvscw_autosize_useheader"></span><dl> <dt>**LVSCW \_ AUTOSIZE \_ USEHEADER**</dt> </dl> | Ridimensiona automaticamente la colonna in base al testo dell'intestazione. Se si usa questo valore con l'ultima colonna, la larghezza viene impostata in modo da riempire la larghezza rimanente del controllo di visualizzazione elenco.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Si supponga di avere un controllo visualizzazione elenco a 2 colonne con una larghezza di 500 pixel. Se la larghezza della colonna zero è impostata su 200 pixel e si invia questo messaggio con *wParam* = 1 e *lParam* = LVSCW AUTOSIZE USEHEADER, la seconda (e l'ultima) colonna avrà una larghezza \_ di \_ 300 pixel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





