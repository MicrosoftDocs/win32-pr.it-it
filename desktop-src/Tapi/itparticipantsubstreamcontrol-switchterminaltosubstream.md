---
description: Il metodo SwitchTerminalToSubStream imposta un terminale sul flusso secondario del partecipante.
ms.assetid: 39e1d4b9-2e39-4b36-9a6a-89e41cd59153
title: Metodo ITParticipantSubStreamControl::SwitchTerminalToSubStream (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41f211d4f3ff0f01801fb5497d36d81fa46e43397d8b69227180b022c9e74a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774651"
---
# <a name="itparticipantsubstreamcontrolswitchterminaltosubstream-method"></a>Metodo ITParticipantSubStreamControl::SwitchTerminalToSubStream

\[**SwitchTerminalToSubStream** non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo SwitchTerminalToSubStream** imposta un terminale sul flusso secondario del partecipante.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SwitchTerminalToSubStream(
  [in] ITTerminal  *pITTerminal,
  [in] ITSubStream *pITSubStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pITTerminal* \[ Pollici\]
</dt> <dd>

Puntatore [**all'interfaccia ITTerminal.**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)

</dd> <dt>

*pITSubStream* \[ Pollici\]
</dt> <dd>

Puntatore [**all'interfaccia ITSubStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                     | Descrizione                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | Il metodo è riuscito.<br/>                                                                       |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>    | Impossibile accedere alle informazioni sul partecipante per il flusso.<br/>                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>    | Il *parametro pParticipant* o *pITSubStream* non punta a un'interfaccia valida.<br/> |
| <dl> <dt>**TAPI \_ E \_ NOITEMS**</dt> </dl> | Il flusso secondario non è pronto.<br/>                                                             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | Memoria insufficiente per eseguire l'operazione.<br/>                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITParticipantSubStreamControl**](itparticipantsubstreamcontrol.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> </dl>

 

