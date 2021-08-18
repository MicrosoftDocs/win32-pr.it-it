---
title: Metodo CompareSoHRequests INapSystemHealthAgentCallback (NapSystemHealthAgent.h)
description: Viene usato dall'SHA per confrontare le richieste SoH.
ms.assetid: 14ba189a-e745-44b0-b729-522087d4e08b
keywords:
- Metodo CompareSoHRequests nap
- Metodo CompareSoHRequests NAP , interfaccia INapSystemHealthAgentCallback
- Interfaccia INapSystemHealthAgentCallback nap , metodo CompareSoHRequests
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.CompareSoHRequests
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3af26786c8ef021794876d8876ae5d8faee65b8cbbfc39b434b000ff502c64c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939436"
---
# <a name="inapsystemhealthagentcallbackcomparesohrequests-method"></a>Metodo INapSystemHealthAgentCallback::CompareSoHRequests

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSystemHealthAgentCallback::CompareSoHRequests** viene usato dall'SHA per confrontare le richieste SoH.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CompareSoHRequests(
  [in]  const SoHRequest *lhs,
  [in]  const SoHRequest *rhs,
  [out]       BOOL       *isEqual
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lhs* \[ Pollici\]
</dt> <dd>

Puntatore a [**SoHRequest a**](/windows/win32/api/naptypes/ns-naptypes-soh) sinistra dell'operazione di confronto.

</dd> <dt>

*rhs* \[ Pollici\]
</dt> <dd>

Puntatore a [**SoHRequest a**](/windows/win32/api/naptypes/ns-naptypes-soh) destra dell'operazione di confronto.

</dd> <dt>

*isEqual* \[ Cambio\]
</dt> <dd>

Puntatore a un **oggetto BOOL** **che è TRUE se** *lhs* e *rhs* sono semanticamente uguali e **FALSE in caso contrario.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                               | Descrizione                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Indica l'esito positivo dell'operazione.<br/>                         |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Il metodo non è stato implementato dall'SHA.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo di callback viene dichiarato dal sistema di Protezione accesso alla rete e deve essere implementato dal writer SHA.

L'SHA deve confrontare i soh e restituire **TRUE** se i soh sono semanticamente uguali. NapAgent usa queste informazioni per determinare se deve essere avviato uno scambio SoH a causa della modifica dello stato del computer client.

Se gli SHA hanno inserito ID incrementali o timestamp nel proprio soH, i file SoH possono essere semanticamente uguali (ad esempio, possono trasmettere le stesse informazioni sull'integrità), ma possono essere disuguali a livello di byte. Gli SHA devono implementare questa funzione per verificare l'uguaglianza semantica dei soh.

Se gli SHA non hanno inserito timestamp o ID nei relativi soH, possono scegliere di non implementare questa funzione e restituire **E \_ NOTIMPL**. In questo caso, NapAgent esegue un confronto byte per byte su [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> <dt>

[**Soh**](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> </dl>

 

 





