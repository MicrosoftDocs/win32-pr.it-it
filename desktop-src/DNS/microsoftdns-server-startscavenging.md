---
title: Metodo StartScavenging della classe MicrosoftDNS_Server
description: Il metodo StartScavenging avvia lo scavenging dei record non aggiornati nelle zone sottoposte a scavenging.
ms.assetid: ee1bc0e0-9334-4971-a524-4bb8a9015b5b
keywords:
- DNS del metodo StartScavenging
- Metodo StartScavenging DNS, MicrosoftDNS_Server classe
- MicrosoftDNS_Server classe DNS , metodo StartScavenging
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
ms.openlocfilehash: b6173021ca49dc73b7ec89f60b097b2179078a774c9a40c26fda2c41b2ad25f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874771"
---
# <a name="startscavenging-method-of-the-microsoftdns_server-class"></a>Metodo StartScavenging della classe Server \_ MicrosoftDNS

Il **metodo StartScavenging** avvia lo scavenging dei record non aggiornati nelle zone sottoposte a scavenging.

## <a name="syntax"></a>Sintassi


```mof
uint32 StartScavenging();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

ERROR \_ SUCCESS indica che lo scavenging è stato avviato correttamente. Qualsiasi altro valore è un codice di errore.

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

[**Metodo StopService della classe server \_ MicrosoftDNS**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Metodo GetDistinguishedName della classe server \_ MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





