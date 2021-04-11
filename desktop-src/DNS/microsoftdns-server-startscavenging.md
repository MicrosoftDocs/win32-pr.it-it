---
title: Metodo StartScavenging della classe MicrosoftDNS_Server
description: Il metodo StartScavenging avvia lo scavenging dei record non aggiornati nelle zone soggette allo scavenging.
ms.assetid: ee1bc0e0-9334-4971-a524-4bb8a9015b5b
keywords:
- DNS del metodo StartScavenging
- DNS del metodo StartScavenging, classe MicrosoftDNS_Server
- Classe MicrosoftDNS_Server DNS, metodo StartScavenging
topic_type:
- apiref
api_name:
- MicrosoftDNS_Server.StartScavenging
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8e1927ed069d3e3e3cf27fd94b1ffd54e6bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964370"
---
# <a name="startscavenging-method-of-the-microsoftdns_server-class"></a>Metodo StartScavenging della \_ classe server MicrosoftDNS

Il metodo **StartScavenging** avvia lo scavenging dei record non aggiornati nelle zone soggette allo scavenging.

## <a name="syntax"></a>Sintassi


```mof
uint32 StartScavenging();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

ERRORE \_ indica che l'operazione di scavenging è stata avviata correttamente. Qualsiasi altro valore è un codice di errore.

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

[**Metodo StopService della \_ classe server MicrosoftDNS**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Metodo getdistinguishname della \_ classe server MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





