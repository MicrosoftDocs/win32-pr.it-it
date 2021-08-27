---
title: LVM_SETCALLBACKMASK messaggio (Commctrl.h)
description: Modifica la maschera di callback per un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro ListView SetCallbackMask.
ms.assetid: d7828bab-9897-408c-99ca-fad42b431be8
keywords:
- LVM_SETCALLBACKMASK dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- LVM_SETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79e33b106eb0c59f83e40b9f170dd017fcdda412072ed51a26572fcf368f5215
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088851"
---
# <a name="lvm_setcallbackmask-message"></a>Messaggio LVM \_ SETCALLBACKMASK

Modifica la maschera di callback per un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView SetCallbackMask.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore della maschera di callback. I bit della maschera indicano gli stati dell'elemento o le immagini per cui l'applicazione archivia i dati dello stato corrente. Questo valore può essere qualsiasi combinazione delle costanti seguenti:



| Valore                                                                                                                                                                           | Significato                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ CUT**</dt> </dl>                                  | L'elemento è contrassegnato per un'operazione taglia e incolla.<br/>                                       |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | L'elemento è evidenziato come destinazione di trascinamento della selezione.<br/>                                      |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS \_ INCENTRATO**</dt> </dl>                      | L'elemento ha lo stato attivo.<br/>                                                                 |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ SELEZIONATO**</dt> </dl>                   | L'elemento è selezionato. <br/>                                                                  |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**MASCHERA DI SOVRAPPOSIZIONE LVIS \_**</dt> </dl>          | L'applicazione archivia l'indice dell'elenco immagini dell'immagine di sovrimpressione corrente per ogni elemento.<br/> |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | L'applicazione archivia l'indice dell'elenco immagini dell'immagine di stato corrente per ogni elemento. <br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

La *maschera di callback* di un controllo visualizzazione elenco è un set di flag di bit che specificano gli stati dell'elemento per cui l'applicazione, anziché il controllo, archivia i dati correnti. La maschera di callback si applica a tutti gli elementi del controllo, a differenza della designazione dell'elemento di callback, che si applica a un elemento specifico. La maschera di callback è zero per impostazione predefinita, vale a dire che il controllo visualizzazione elenco archivia tutte le informazioni sullo stato degli elementi. Dopo aver creato un controllo visualizzazione elenco e aver inizializzato i relativi elementi, è possibile inviare il messaggio **LVM \_ SETCALLBACKMASK** per modificare la maschera di callback. Per recuperare la maschera di callback corrente, inviare il messaggio [**LVM \_ GETCALLBACKMASK.**](lvm-getcallbackmask.md)

Per altre informazioni sulle immagini sovrapposte e le immagini di stato, vedere [Aggiunta di List-View di immagini](using-list-view-controls.md).

Per altre informazioni sui callback di visualizzazione elenco, vedere [Elementi di callback e Maschera di callback](list-view-controls-overview.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LVN \_ GETDISPINFO**](lvn-getdispinfo.md)
</dt> </dl>

 

 





