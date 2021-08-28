---
description: Il metodo Next ottiene il successivo numero specificato di elementi nella sequenza di enumerazione. Questo metodo è nascosto ai linguaggi Visual Basic e di scripting.
ms.assetid: bd94f592-ac6f-48b7-8190-352a5e18f224
title: Metodo IEnumParticipant::Next (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d574f7c34bc48679ea679caf8ba07c881bcd1c692fa3215ae48a9ecf54d7cbfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003589"
---
# <a name="ienumparticipantnext-method"></a>Metodo IEnumParticipant::Next

\[**Successivamente** non è disponibile per l'uso in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo Next** ottiene il successivo numero specificato di elementi nella sequenza di enumerazione. Questo metodo è nascosto ai linguaggi Visual Basic e di scripting.

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

*celt* \[ Pollici\]
</dt> <dd>

Numero di elementi richiesti.

</dd> <dt>

*Elementi ppElements* \[ Cambio\]
</dt> <dd>

Puntatore [**alle interfacce ITAgentHandler.**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler)

</dd> <dt>

*pceltFetched* \[ Cambio\]
</dt> <dd>

Puntatore al numero di elementi effettivamente forniti. Può essere **NULL se** *celt* è uno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo ha restituito il numero di elementi *celt.*<br/>           |
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | Il numero di elementi rimanenti è minore di *celt*.<br/>   |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | Il *parametro ppElements* non è un puntatore valido.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

TAPI chiama [**il metodo AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sull'interfaccia [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) restituita da **IEnumParticipant::Next.** L'applicazione deve [**chiamare Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) **sull'interfaccia ITAgentHandler** per liberare le risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

