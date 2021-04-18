---
title: Metodo INapSystemHealthAgentBinding FlushCache (NapSystemHealthAgent. h)
description: Viene chiamato da un SHA per scaricare la cache del rapporto di integrità.
ms.assetid: a771ce03-1922-4e2d-9490-7ee9f693857c
keywords:
- NAP Metodo FlushCache
- Metodo FlushCache NAP, interfaccia INapSystemHealthAgentBinding
- Interfaccia INapSystemHealthAgentBinding NAP, Metodo FlushCache
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.FlushCache
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ead6e496d220619439b80fdc5c7601675fdb7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300956"
---
# <a name="inapsystemhealthagentbindingflushcache-method"></a>Metodo INapSystemHealthAgentBinding:: FlushCache

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthAgentBinding:: FlushCache** viene chiamato da un SHA per scaricare la cache del rapporto di integrità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT FlushCache();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                         | Descrizione                                                                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>               | Operazione riuscita.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>     | Errore delle autorizzazioni, accesso negato.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>      | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/>                                                             |
| <dl> <dt>**RPC \_ E \_ disconnessa**</dt> </dl> | Il NapAgent è stato arrestato. Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, una volta riavviato.<br/> |



 

## <a name="remarks"></a>Commenti

NapAgent gestisce una cache di invieranno recenti forniti da SHAs diversi. Questa cache è utile per ottimizzare le prestazioni in fase di avvio, quando SHAs può o meno essere associato al sistema.

SHA deve chiamare [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) prima di chiamare questo metodo o qualsiasi altro metodo dell'interfaccia [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





