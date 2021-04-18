---
description: Il metodo SwitchTerminalToSubStream imposta un terminale sul sottoflusso del partecipante.
ms.assetid: 39e1d4b9-2e39-4b36-9a6a-89e41cd59153
title: 'Metodo ITParticipantSubStreamControl:: SwitchTerminalToSubStream (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f10401b2cf1598c76537ebd3a7049d67bf0657
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333665"
---
# <a name="itparticipantsubstreamcontrolswitchterminaltosubstream-method"></a>Metodo ITParticipantSubStreamControl:: SwitchTerminalToSubStream

\[**SwitchTerminalToSubStream** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **SwitchTerminalToSubStream** imposta un terminale sul sottoflusso del partecipante.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SwitchTerminalToSubStream(
  [in] ITTerminal  *pITTerminal,
  [in] ITSubStream *pITSubStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pITTerminal* \[ in\]
</dt> <dd>

Puntatore all'interfaccia [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .

</dd> <dt>

*pITSubStream* \[ in\]
</dt> <dd>

Puntatore all'interfaccia [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                     | Descrizione                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>            | Il metodo è riuscito.<br/>                                                                       |
| <dl> <dt>**E \_ imprevisto**</dt> </dl>    | Non è possibile accedere alle informazioni del partecipante per il flusso.<br/>                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>    | Il *pParticipant* o il parametro *pITSubStream* non punta a un'interfaccia valida.<br/> |
| <dl> <dt>**TAPI \_ E \_ noitems**</dt> </dl> | Il sottoflusso non è pronto.<br/>                                                             |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>   | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
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

 

