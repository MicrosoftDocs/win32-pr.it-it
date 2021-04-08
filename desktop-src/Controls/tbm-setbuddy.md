---
title: Messaggio TBM_SETBUDDY (COMmctrl. h)
description: Assegna una finestra come finestra di Buddy per un controllo TrackBar. Le finestre del contatto TrackBar vengono visualizzate automaticamente in un percorso relativo all'orientamento del controllo (orizzontale o verticale).
ms.assetid: ab35911f-bf81-47f3-98aa-0901aa877dea
keywords:
- Controlli di Windows Message TBM_SETBUDDY
topic_type:
- apiref
api_name:
- TBM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab33e53117933390d7a34ec75a49724003255108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048064"
---
# <a name="tbm_setbuddy-message"></a>\_Messaggio SEBUDDY TBM

Assegna una finestra come finestra di Buddy per un controllo TrackBar. Le finestre del contatto TrackBar vengono visualizzate automaticamente in un percorso relativo all'orientamento del controllo (orizzontale o verticale).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che specifica la posizione in cui visualizzare la finestra di Buddy. I valori validi sono i seguenti:



| Valore                                                                                                                                | Significato                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>**TRUE**</dt> </dl>    | L'oggetto Buddy verrà visualizzato a sinistra del controllo TrackBar se il controllo TrackBar usa lo [**stile \_ orizzontalmente di TBS**](trackbar-control-styles.md) . Se il controllo TrackBar usa lo stile di [**TBS \_ Vert**](trackbar-control-styles.md) , il contatto viene visualizzato sopra il controllo TrackBar.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>**FALSE**</dt> </dl> | L'oggetto Buddy verrà visualizzato a destra del controllo TrackBar se il controllo TrackBar usa lo [**stile \_ orizzontalmente di TBS**](trackbar-control-styles.md) . Se il controllo TrackBar utilizza lo stile di [**TBS \_ Vert**](trackbar-control-styles.md) , l'oggetto Buddy viene visualizzato sotto il controllo TrackBar.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la finestra che verrà impostata come Buddy del controllo TrackBar.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle alla finestra precedentemente assegnata al controllo in tale posizione.

## <a name="remarks"></a>Commenti

> [!Note]  
> I controlli TrackBar supportano fino a due finestre di contatto. Questa operazione può essere utile quando è necessario visualizzare testo o immagini a ogni estremità del controllo.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





