---
title: EM_SETZOOM messaggio (Richedit.h)
description: Imposta il rapporto di zoom. Il rapporto deve essere un valore compreso tra 1/64 e 64. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 6cdec5b8-4ce7-4fd5-8083-4daa63d17f63
keywords:
- EM_SETZOOM dei controlli Windows messaggio
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
ms.openlocfilehash: ecf6541bc018df253a3ed45f8bced42e2f19938449d7fc35bf7f309909d53a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437181"
---
# <a name="em_setzoom-message"></a>Messaggio \_ EM SETZOOM

Imposta il rapporto di zoom per un controllo di modifica su più righe o un controllo Rich Edit. Il rapporto deve essere un valore compreso tra 1/64 e 64. Per il controllo di modifica deve essere impostato lo stile esteso **ES \_ EX \_ ZOOMABLE.** Per un effetto su questo messaggio, vedere Modifica degli stili [estesi del controllo.](edit-control-window-extended-styles.md)

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
| <span id="Both_0"></span><span id="both_0"></span><span id="BOTH_0"></span><dl> <dt>**Entrambi 0**</dt> </dl>                                                                                                   | Disattiva lo zoom usando il messaggio **EM \_ SETZOOM** (lo zoom può comunque verificarsi [**usando TxGetExtent).**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)<br/> |
| <span id="1_64____wParam___lParam____64"></span><span id="1_64____wparam___lparam____64"></span><span id="1_64____WPARAM___LPARAM____64"></span><dl> <dt>**1/64 < (wParam/lParam) < 64**</dt> </dl> | Zoom visualizzato in base al numeratore/denominatore del rapporto di zoom<br/>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la nuova impostazione di zoom viene accettata, il valore restituito è **TRUE.**

Se la nuova impostazione di zoom non viene accettata, il valore restituito è **FALSE.**

## <a name="remarks"></a>Commenti

**Modifica:** Supportato in Windows 10 1809 e versioni successive. Per il controllo di modifica deve essere impostato lo stile esteso **ES \_ EX \_ ZOOMABLE.** Per un effetto su questo messaggio, vedere Modifica degli stili [estesi del controllo.](edit-control-window-extended-styles.md) Per informazioni sul controllo di modifica, vedere [Edit Controls.](about-edit-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Componente ridistribuibile<br/>          | Rich Edit 3.0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>Richedit.h/Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ GETZOOM**](em-getzoom.md)
</dt> </dl>

 

 





