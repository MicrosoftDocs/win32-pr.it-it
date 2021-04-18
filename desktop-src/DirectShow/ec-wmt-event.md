---
description: Inviato dal filtro di lettura ASF WM quando legge i file ASF protetti da Digital Rights Management (DRM).
ms.assetid: ac6ea7a1-238e-42ae-9f10-e1db60381357
title: EC_WMT_EVENT (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ce974cd83a404242fb51486f0889ac9b79e044
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325491"
---
# <a name="ec_wmt_event-dshowh"></a>EC_WMT_EVENT (dshow. h)

Inviato dal filtro di [lettura ASF WM](wm-asf-reader-filter.md) quando legge i file ASF protetti da Digital Rights Management (DRM).

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Uno dei valori di **\_ stato di WMT** seguenti:



| Valore                         | Descrizione                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------|
| \_licenza di acquisizione WMT \_         | Inviato quando il componente DRM ha completato il processo di acquisizione della licenza, con esito positivo o negativo. |
| WMT di \_ personalizzazione            | Il processo di aggiornamento della sicurezza è stato completato correttamente o senza esito positivo.                                |
| WMT \_ richiede l' \_ individualizzazione | Il file richiede che un'applicazione riceva un aggiornamento della sicurezza prima di eseguire l'azione richiesta.          |
| \_nessun \_ diritto di WMT               | L'applicazione non dispone dei diritti necessari per eseguire l'azione richiesta su un file protetto da DRM versione 1.                |
| WMT \_ No \_ Rights \_           | L'applicazione non dispone dei diritti necessari per eseguire l'azione richiesta su un file protetto da DRM versione 7.                |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Puntatore a una struttura di [**\_ dati dell' \_ evento \_ am WMT**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) che contiene informazioni sull'evento o **null**. Il membro **pData** di questa struttura punta a dati aggiuntivi il cui tipo dipende dal valore di **lParam1**, come illustrato nella tabella seguente.



| lParam1                       | \_ \_ Dati evento WMT \_ . pData                                                                                                                       |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| \_licenza di acquisizione WMT \_         | Puntatore a una struttura di [**\_ dati di \_ licenza \_ WM Get**](/windows/desktop/wmformat/wm-get-license-data) . Questa struttura è documentata in Windows Media Format SDK. |
| WMT di \_ personalizzazione            | Puntatore a una struttura di [**\_ \_ stato di personalizzazione WM**](/windows/desktop/wmformat/wm-individualize-status) .                                                        |
| WMT \_ richiede l' \_ individualizzazione | **Valore null**.                                                                                                                                        |
| \_nessun \_ diritto di WMT               | Puntatore a una stringa di caratteri wide contenente un URL della richiesta di verifica.                                                                                   |
| WMT \_ No \_ Rights \_           | Puntatore a una struttura di [**\_ dati di \_ licenza \_ WM Get**](/windows/desktop/wmformat/wm-get-license-data) .                                                               |



 

Il valore di *lParam2* potrebbe essere **null**. Verificare il valore prima di dereferenziare il puntatore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per ulteriori informazioni sull'abilitazione della riproduzione di file protetti da DRM, vedere la documentazione di Windows Media Format SDK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

