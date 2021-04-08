---
title: Messaggio di EM_SETZOOM (RichEdit. h)
description: Imposta il rapporto di zoom. Il rapporto deve essere un valore compreso tra 1/64 e 64. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 6cdec5b8-4ce7-4fd5-8083-4daa63d17f63
keywords:
- Controlli di Windows Message EM_SETZOOM
topic_type:
- apiref
api_name:
- EM_SETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d38630f27afcfc0ed29e3ccc3129e2dea22d4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874030"
---
# <a name="em_setzoom-message"></a>\_Messaggio di ridimensionamento em

Imposta la percentuale di zoom per un controllo di modifica su più righe o un controllo Rich Edit. Il rapporto deve essere un valore compreso tra 1/64 e 64. Il controllo di modifica deve avere il set di stili estesi **es \_ ex \_ Zoom** , perché questo messaggio abbia effetto, vedere [modificare gli stili estesi del controllo](edit-control-window-extended-styles.md).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numeratore del rapporto di zoom.

</dd> <dt>

*lParam* 
</dt> <dd>

Denominatore del rapporto di zoom. Questi parametri possono avere i valori seguenti.



| Valore                                                                                                                                                                                                                                                              | Significato                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Both_0"></span><span id="both_0"></span><span id="BOTH_0"></span><dl> <dt>**Entrambi 0**</dt> </dl>                                                                                                   | Disattiva lo zoom usando il messaggio di **Zoom \_ em** . è possibile che si verifichi ancora lo zoom usando [**TxGetExtent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent).<br/> |
| <span id="1_64____wParam___lParam____64"></span><span id="1_64____wparam___lparam____64"></span><span id="1_64____WPARAM___LPARAM____64"></span><dl> <dt>**1/64 < (wParam/lParam) < 64**</dt> </dl> | Consente di ingrandire la visualizzazione del numeratore/denominatore della percentuale di zoom<br/>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se viene accettata la nuova impostazione di zoom, il valore restituito è **true**.

Se la nuova impostazione di zoom non viene accettata, il valore restituito è **false**.

## <a name="remarks"></a>Commenti

**Modifica:** Supportato in Windows 10 1809 e versioni successive. Il controllo di modifica deve avere il set di stili estesi **es \_ ex \_ Zoom** , perché questo messaggio abbia effetto, vedere [modificare gli stili estesi del controllo](edit-control-window-extended-styles.md). Per informazioni sul controllo di modifica, vedere [modificare i controlli](about-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Componente ridistribuibile<br/>          | Modifica avanzata 3,0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h/COMmctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ GETzoom**](em-getzoom.md)
</dt> </dl>

 

 





