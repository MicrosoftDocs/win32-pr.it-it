---
description: Inviato dal filtro lettore ASF WM quando legge i file ASF protetti da Digital Rights Management (DRM).
ms.assetid: ac6ea7a1-238e-42ae-9f10-e1db60381357
title: EC_WMT_EVENT (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2ae2659c26d170bef14a76c0528eb5159e92ef3598fb999215e1fbd848ea90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819924"
---
# <a name="ec_wmt_event-dshowh"></a>EC_WMT_EVENT (Dshow.h)

Inviato dal filtro [lettore ASF WM](wm-asf-reader-filter.md) quando legge i file ASF protetti da Digital Rights Management (DRM).

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Uno dei valori **DI \_ STATO WMT** seguenti:



| Valore                         | Descrizione                                                                                                       |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------|
| WMT \_ ACQUIRE \_ LICENSE         | Inviato quando il componente DRM ha completato il processo di acquisizione della licenza, con esito positivo o negativo. |
| WMT \_ INDIVIDUALIZE            | Il processo di aggiornamento della sicurezza è stato completato, con esito positivo o negativo.                                |
| WMT \_ RICHIEDE \_ L'INDIVIDUALIZZAZIONE | Il file richiede che un'applicazione riceva un aggiornamento della sicurezza prima di eseguire l'azione richiesta.          |
| WMT \_ NO \_ RIGHTS               | L'applicazione non ha diritti per eseguire l'azione richiesta su un file protetto da DRM versione 1.                |
| WMT \_ NO \_ RIGHTS \_ EX           | L'applicazione non ha diritti per eseguire l'azione richiesta su un file protetto da DRM versione 7.                |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Puntatore a [**una \_ struttura AM WMT EVENT \_ \_ DATA**](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) che contiene informazioni sull'evento oppure **NULL.** Il **membro pData** di questa struttura punta a dati aggiuntivi, il cui tipo dipende dal valore di **lParam1,** come illustrato nella tabella seguente.



| lParam1                       | AM \_ WMT \_ EVENT \_ DATA.pData                                                                                                                       |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| WMT \_ ACQUIRE \_ LICENSE         | Puntatore a una [**struttura WM GET LICENSE \_ \_ \_ DATA.**](/windows/desktop/wmformat/wm-get-license-data) Questa struttura è documentata in Windows Media Format SDK. |
| WMT \_ INDIVIDUALIZE            | Puntatore a [**una struttura \_ WM INDIVIDUALIZE \_ STATUS.**](/windows/desktop/wmformat/wm-individualize-status)                                                        |
| WMT \_ RICHIEDE \_ L'INDIVIDUALIZZAZIONE | **NULL**.                                                                                                                                        |
| WMT \_ NO \_ RIGHTS               | Puntatore a una stringa di caratteri wide contenente un URL di richiesta di richiesta.                                                                                   |
| WMT \_ NO \_ RIGHTS \_ EX           | Puntatore a una [**struttura WM GET LICENSE \_ \_ \_ DATA.**](/windows/desktop/wmformat/wm-get-license-data)                                                               |



 

Il valore di *lParam2* potrebbe essere **NULL.** Controllare il valore prima di dereferenziare il puntatore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per altre informazioni sull'abilitazione della riproduzione di file protetti da DRM, vedere la documentazione di Windows Media Format SDK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

