---
title: Messaggio LVM_SETCOLUMNWIDTH (COMmctrl. h)
description: Modifica la larghezza di una colonna in modalità di visualizzazione report o la larghezza di tutte le colonne in modalità visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetColumnWidth di ListView.
ms.assetid: 309aebfb-9fed-4c77-acbb-ea905b32b0e2
keywords:
- Controlli di Windows Message LVM_SETCOLUMNWIDTH
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
ms.openlocfilehash: 529e989b3d66562acc7b6f91c3b3b06527235e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118998"
---
# <a name="lvm_setcolumnwidth-message"></a>\_Messaggio SETCOLUMNWIDTH LVM

Modifica la larghezza di una colonna in modalità di visualizzazione report o la larghezza di tutte le colonne in modalità visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetColumnWidth di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero di una colonna valida. Per la modalità di visualizzazione elenco, questo parametro deve essere impostato su zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Nuova larghezza della colonna in pixel. Per la modalità di visualizzazione report, sono supportati i valori speciali seguenti:



| Valore                                                                                                                                                                                           | Significato                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVSCW_AUTOSIZE"></span><span id="lvscw_autosize"></span><dl> <dt>**\_ridimensionamento automatico LVSCW**</dt> </dl>                                | Ridimensiona automaticamente la colonna.<br/>                                                                                                                                           |
| <span id="LVSCW_AUTOSIZE_USEHEADER"></span><span id="lvscw_autosize_useheader"></span><dl> <dt>**LVSCW \_ AUTOSIZE \_ USEHEADER**</dt> </dl> | Ridimensiona automaticamente la colonna per adattarla al testo dell'intestazione. Se si usa questo valore con l'ultima colonna, la larghezza viene impostata in modo da riempire la larghezza rimanente del controllo visualizzazione elenco.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Si supponga di disporre di un controllo di visualizzazione elenco a 2 colonne con una larghezza di 500 pixel. Se la larghezza della colonna zero è impostata su 200 pixel e si invia questo messaggio con *wParam* = 1 e *lParam* = LVSCW \_ AUTOSIZE \_ USEHEADER, la seconda colonna (e l'ultima) sarà 300 pixel di larghezza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





