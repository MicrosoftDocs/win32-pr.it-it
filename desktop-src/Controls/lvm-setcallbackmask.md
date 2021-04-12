---
title: Messaggio LVM_SETCALLBACKMASK (COMmctrl. h)
description: Modifica la maschera di callback per un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetCallbackMask di ListView.
ms.assetid: d7828bab-9897-408c-99ca-fad42b431be8
keywords:
- Controlli di Windows Message LVM_SETCALLBACKMASK
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
ms.openlocfilehash: ef6dd46228c4e4aeada30f469a77f9e67aff3a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119470"
---
# <a name="lvm_setcallbackmask-message"></a>\_Messaggio SETCALLBACKMASK LVM

Modifica la maschera di callback per un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetCallbackMask di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore della maschera di callback. I bit della maschera indicano gli Stati degli elementi o le immagini per cui l'applicazione archivia i dati dello stato corrente. Questo valore può essere una qualsiasi combinazione delle costanti seguenti:



| Valore                                                                                                                                                                           | Significato                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**\_taglia lvis**</dt> </dl>                                  | L'elemento è contrassegnato per un'operazione di taglia e incolla.<br/>                                       |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**\_DROPHILITED lvis**</dt> </dl>          | L'elemento è evidenziato come destinazione di trascinamento della selezione.<br/>                                      |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS con stato \_ attivo**</dt> </dl>                      | L'elemento ha lo stato attivo.<br/>                                                                 |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ selezionato**</dt> </dl>                   | L'elemento è selezionato. <br/>                                                                  |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**\_OVERLAYMASK lvis**</dt> </dl>          | L'applicazione archivia l'indice dell'elenco immagini dell'immagine sovrapposta corrente per ogni elemento.<br/> |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**\_STATEIMAGEMASK lvis**</dt> </dl> | L'applicazione archivia l'indice dell'elenco immagini dell'immagine di stato corrente per ogni elemento. <br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

La *maschera di callback* di un controllo visualizzazione elenco è un set di flag di bit che specificano gli Stati degli elementi per i quali l'applicazione, anziché il controllo, archivia i dati correnti. La maschera di callback viene applicata a tutti gli elementi del controllo, a differenza della designazione dell'elemento di callback che si applica a un elemento specifico. Per impostazione predefinita, la maschera di callback è zero, il che significa che il controllo elenco-visualizzazione archivia tutte le informazioni sullo stato dell'elemento. Dopo aver creato un controllo visualizzazione elenco e aver inizializzato gli elementi, è possibile inviare il messaggio **LVM \_ SETCALLBACKMASK** per modificare la maschera di callback. Per recuperare la maschera di callback corrente, inviare il messaggio [**LVM \_ GETCALLBACKMASK**](lvm-getcallbackmask.md) .

Per ulteriori informazioni sulle immagini sovrapposte e le immagini di stato, vedere [aggiunta di List-View elenchi di immagini](using-list-view-controls.md).

Per altre informazioni sui callback di visualizzazione elenco, vedere [elementi di callback e maschera di callback](list-view-controls-overview.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETDISPINFO LVN**](lvn-getdispinfo.md)
</dt> </dl>

 

 





