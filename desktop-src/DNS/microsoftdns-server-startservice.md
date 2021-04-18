---
title: Metodo StartService della classe MicrosoftDNS_Server
description: Il metodo StartService avvia il server DNS.
ms.assetid: f6343a34-9d1b-4f82-897e-289650af6be9
keywords:
- DNS del metodo StartService
- DNS del metodo StartService, classe MicrosoftDNS_Server
- Classe MicrosoftDNS_Server DNS, metodo StartService
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartService
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e103b3d2648bf2c061eb047090cfdfeb907518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301832"
---
# <a name="startservice-method-of-the-microsoftdns_server-class"></a>Metodo StartService della \_ classe server MicrosoftDNS

Il metodo **StartService** avvia il server DNS.

## <a name="syntax"></a>Sintassi


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

ERRORE \_ con esito positivo indica che il servizio è stato avviato correttamente. Qualsiasi altro valore è un codice di errore.

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

[**Metodo StopService della \_ classe server MicrosoftDNS**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Metodo StartScavenging della \_ classe server MicrosoftDNS**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Metodo getdistinguishname della \_ classe server MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





