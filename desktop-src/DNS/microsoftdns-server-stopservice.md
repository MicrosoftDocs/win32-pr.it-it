---
title: Metodo StopService della classe MicrosoftDNS_Server
description: Il metodo StopService arresta il server DNS.
ms.assetid: 80637d5b-e43a-4710-b3ab-eec246587788
keywords:
- DNS del metodo StopService
- DNS del metodo StopService, classe MicrosoftDNS_Server
- Classe MicrosoftDNS_Server DNS, metodo StopService
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
ms.openlocfilehash: f811533c66185304c5c674fdfff2eda8cf5bef69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477267"
---
# <a name="stopservice-method-of-the-microsoftdns_server-class"></a>Metodo StopService della \_ classe server MicrosoftDNS

Il metodo **StopService** arresta il server DNS.

## <a name="syntax"></a>Sintassi


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

ERRORE \_ indica che il servizio è stato arrestato correttamente. Qualsiasi altro valore è un codice di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                   |
| Spazio dei nomi<br/>                | \\MicrosoftDNS radice<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Server MicrosoftDNS**](microsoftdns-server.md)
</dt> <dt>

[**Metodo StartService della \_ classe server MicrosoftDNS**](microsoftdns-server-startservice.md)
</dt> <dt>

[**Metodo StartScavenging della \_ classe server MicrosoftDNS**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Metodo getdistinguishname della \_ classe server MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





