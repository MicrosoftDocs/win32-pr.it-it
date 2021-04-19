---
description: Il metodo successivo ottiene il numero specificato successivo di elementi nella sequenza di enumerazione. Questo metodo è nascosto Visual Basic e linguaggi di scripting.
ms.assetid: bd94f592-ac6f-48b7-8190-352a5e18f224
title: 'Metodo IEnumParticipant:: Next (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89586370d01aaac54f05242e0eb3c53eb938c47b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333142"
---
# <a name="ienumparticipantnext-method"></a>IEnumParticipant:: Next (metodo)

\[Il passaggio **successivo** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **successivo** ottiene il numero specificato successivo di elementi nella sequenza di enumerazione. Questo metodo è nascosto Visual Basic e linguaggi di scripting.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Next(
  [in]  ULONG         celt,
  [out] ITParticipant **ppElements,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*celt* \[ in\]
</dt> <dd>

Numero di elementi richiesti.

</dd> <dt>

*ppElements* \[ out\]
</dt> <dd>

Puntatore a interfacce [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) .

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Puntatore al numero di elementi effettivamente forniti. Può essere **null** se *celt* è uno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo ha restituito il numero *celt* di elementi.<br/>           |
| <dl> <dt>**S \_ false**</dt> </dl>       | Il numero di elementi rimanenti è minore di *celt*.<br/>   |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *ppElements* non è un puntatore valido.<br/>   |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

TAPI chiama il metodo [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sull'interfaccia [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) restituita da **IEnumParticipant:: Next**. L'applicazione deve chiamare [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sull'interfaccia **ITAgentHandler** per liberare risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

