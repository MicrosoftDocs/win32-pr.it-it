---
description: Il metodo PeriodicUpdatePicture viene chiamato da un'applicazione per configurare un timer nel flusso che richiederà periodicamente gli aggiornamenti delle immagini. Gli aggiornamenti delle immagini provocano un utilizzo elevato della larghezza di banda, quindi questo metodo viene normalmente usato al posto di UpdatePicture.
ms.assetid: 6ae3b5e9-bc11-4f3f-972b-21c9ac299987
title: Metodo IKeyFrameControl::P eriodicUpdatePicture (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bbfb18b0be96d611f0fe385cc825602dc316ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324762"
---
# <a name="ikeyframecontrolperiodicupdatepicture-method"></a>IKeyFrameControl::P metodo eriodicUpdatePicture

\[**PeriodicUpdatePicture** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **PeriodicUpdatePicture** viene chiamato da un'applicazione per configurare un timer nel flusso che richiederà periodicamente gli aggiornamenti delle immagini. Gli aggiornamenti delle immagini provocano un utilizzo elevato della larghezza di banda, quindi questo metodo viene normalmente usato al posto di [**UpdatePicture**](ikeyframecontrol-updatepicture.md).

Se il metodo viene chiamato quando il flusso è attivo, il timer verrà avviato immediatamente. Se il flusso non è attivo, il timer viene avviato quando il flusso entra nello stato attivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PeriodicUpdatePicture(
  [in] BOOL  fEnable,
  [in] DWORD dwInterval
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fEnable* \[ in\]
</dt> <dd>

**True** Abilita il timer. **False** lo Disabilita.

</dd> <dt>

*dwInterval* \[ in\]
</dt> <dd>

Intervallo del timer, in secondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Il metodo è riuscito.<br/>              |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Non riuscito per motivi imprevisti.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MSP H323](h323-msp.md)
</dt> </dl>

 

 




