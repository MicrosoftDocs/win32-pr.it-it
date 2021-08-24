---
title: Metodo StopService della classe MicrosoftDNS_Server
description: Il metodo StopService arresta il server DNS.
ms.assetid: 80637d5b-e43a-4710-b3ab-eec246587788
keywords:
- DNS del metodo StopService
- Metodo StopService DNS, MicrosoftDNS_Server classe
- MicrosoftDNS_Server classe DNS , metodo StopService
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StopService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d42a443e22d382dd6e7f6ec9d528d0a1f57c6062ba0e03742033c494b75cd8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076745"
---
# <a name="stopservice-method-of-the-microsoftdns_server-class"></a>Metodo StopService della classe Server \_ MicrosoftDNS

Il **metodo StopService** arresta il server DNS.

## <a name="syntax"></a>Sintassi


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

ERROR \_ SUCCESS indica che il servizio è stato arrestato correttamente. Qualsiasi altro valore è un codice di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MicrosoftDNS \_ Server**](microsoftdns-server.md)
</dt> <dt>

[**Metodo StartService della classe server \_ MicrosoftDNS**](microsoftdns-server-startservice.md)
</dt> <dt>

[**Metodo StartScavenging della classe server \_ MicrosoftDNS**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Metodo GetDistinguishedName della classe server \_ MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





