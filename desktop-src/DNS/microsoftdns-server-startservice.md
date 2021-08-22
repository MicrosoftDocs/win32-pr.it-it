---
title: Metodo StartService della classe MicrosoftDNS_Server
description: Il metodo StartService avvia il server DNS.
ms.assetid: f6343a34-9d1b-4f82-897e-289650af6be9
keywords:
- DNS del metodo StartService
- Metodo StartService DNS , MicrosoftDNS_Server classe
- MicrosoftDNS_Server classe DNS , metodo StartService
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
ms.openlocfilehash: b5e74de96ad24ff16ea2c2effaef78003011f5d6bd5d421336084ac5c7701f79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432641"
---
# <a name="startservice-method-of-the-microsoftdns_server-class"></a>Metodo StartService della classe Server \_ MicrosoftDNS

Il **metodo StartService** avvia il server DNS.

## <a name="syntax"></a>Sintassi


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

ERROR \_ SUCCESS indica che il servizio è stato avviato correttamente. Qualsiasi altro valore è un codice di errore.

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

[**Metodo StopService della classe server \_ MicrosoftDNS**](microsoftdns-server-stopservice.md)
</dt> <dt>

[**Metodo StartScavenging della classe server \_ MicrosoftDNS**](microsoftdns-server-startscavenging.md)
</dt> <dt>

[**Metodo GetDistinguishedName della classe server \_ MicrosoftDNS**](microsoftdns-server-getdistinguishedname.md)
</dt> </dl>

 

 





