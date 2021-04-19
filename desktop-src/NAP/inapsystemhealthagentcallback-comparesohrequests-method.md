---
title: Metodo INapSystemHealthAgentCallback CompareSoHRequests (NapSystemHealthAgent. h)
description: Viene usato dall'SHA per confrontare le richieste del rapporto di integrità.
ms.assetid: 14ba189a-e745-44b0-b729-522087d4e08b
keywords:
- NAP metodo CompareSoHRequests
- Metodo CompareSoHRequests NAP, interfaccia INapSystemHealthAgentCallback
- Interfaccia INapSystemHealthAgentCallback NAP, metodo CompareSoHRequests
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
ms.openlocfilehash: 9c6713f3de47cfbde6df67662f89ab3c094d0674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301810"
---
# <a name="inapsystemhealthagentcallbackcomparesohrequests-method"></a>Metodo INapSystemHealthAgentCallback:: CompareSoHRequests

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthAgentCallback:: CompareSoHRequests** viene usato dall'SHA per confrontare le richieste del rapporto di integrità.

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

*LHS* \[ in\]
</dt> <dd>

Puntatore a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) a sinistra dell'operazione di confronto.

</dd> <dt>

*RHS* \[ in\]
</dt> <dd>

Puntatore a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) a destra dell'operazione di confronto.

</dd> <dt>

*è uguale* \[ a out\]
</dt> <dd>

Puntatore a un **bool** che è **true** se *LHS* e *RHS* sono semanticamente uguali e **false** in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                               | Descrizione                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Indica l'esito positivo dell'operazione.<br/>                         |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Il metodo non è stato implementato dall'SHA.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo di callback viene dichiarato dal sistema NAP e deve essere implementato dal writer SHA.

SHA deve confrontare invieranno e restituire **true** se invieranno sono semanticamente uguali. NapAgent utilizza queste informazioni per determinare se deve essere avviato un scambio di rapporto di integrità a causa del cambiamento dello stato del computer client.

Se SHAs hanno inserito gli ID incrementali o i timestamp nel rapporto di integrità, invieranno può essere semanticamente uguali (ovvero possono fornire le stesse informazioni sull'integrità), ma possono essere diversi da byte. SHAs deve implementare questa funzione per verificare l'uguaglianza semantica di invieranno.

Se SHAs non hanno inserito timestamp o ID nei rispettivi invieranno, possono scegliere di non implementare questa funzione e restituire **e \_ NOTIMPL**. In questo caso, NapAgent esegue un confronto byte in [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> <dt>

[**Rapporto**](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> </dl>

 

 





