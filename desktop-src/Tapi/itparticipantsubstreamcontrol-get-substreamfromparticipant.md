---
description: Il \_ metodo Get SubStreamFromParticipant consente a un'applicazione di individuare i flussi sottoflussi associati a un determinato partecipante.
ms.assetid: d45cdd1d-13cf-433a-9b19-193d5c0cba11
title: 'Metodo ITParticipantSubStreamControl:: get_SubStreamFromParticipant (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0eae68cd62c38348e1a576f114a9e93ac52f9cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333667"
---
# <a name="itparticipantsubstreamcontrolget_substreamfromparticipant-method"></a>Metodo ITParticipantSubStreamControl:: Get \_ SubStreamFromParticipant

\[**ottenere \_ SubStreamFromParticipant** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ SubStreamFromParticipant** consente a un'applicazione di individuare i flussi sottoflussi associati a un determinato partecipante.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_SubStreamFromParticipant(
  [in]  ITParticipant *pParticipant,
  [out] ITSubStream   **ppITSubStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pParticipant* \[ in\]
</dt> <dd>

Puntatore all'interfaccia [**ITParticipant**](itparticipant.md) .

</dd> <dt>

*ppITSubStream* \[ out\]
</dt> <dd>

Puntatore alla matrice di puntatori dell'interfaccia [**ITParticipant**](itparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                                  |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                                 |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *ppITSubStream* non è un puntatore valido.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *pParticipant* non punta a un'interfaccia valida.<br/> |
| <dl> <dt>**E \_ imprevisto**</dt> </dl>  | Non è possibile accedere alle informazioni del partecipante del flusso.<br/>       |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>              |



 

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
</dt> </dl>

 

