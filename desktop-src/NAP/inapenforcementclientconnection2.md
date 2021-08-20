---
title: Interfaccia INapEnforcementClientConnection2 (NapEnforcementClient.h)
description: Consente la gestione delle connessioni client. | Interfaccia INapEnforcementClientConnection2 (NapEnforcementClient.h)
ms.assetid: f7b5d8cc-6a91-4e49-8957-cf67d1001089
keywords:
- Interfaccia INapEnforcementClientConnection2 NAP
- Interfaccia INapEnforcementClientConnection2 NAP, descritta
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60e91ffbc12534bb3b5a8ac22cbd13a1238ba32e09b4f56b4ab570ffd1ea8be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144394"
---
# <a name="inapenforcementclientconnection2-interface"></a>Interfaccia INapEnforcementClientConnection2

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**INapEnforcementClientConnection2** fornisce metodi che consentono la gestione della connessione client.

> [!Note]  
> Questa interfaccia eredita tutti i metodi di [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) e deve essere usata.

 

## <a name="members"></a>Membri

**L'interfaccia INapEnforcementClientConnection2** eredita da [**INapEnforcementClientConnection.**](inapenforcementclientconnection.md) **INapEnforcementClientConnection2** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia INapEnforcementClientConnection2** include questi metodi.



| Metodo                                                                                                              | Descrizione                                                                      |
|:--------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**INapEnforcementClientConnection2::GetInstalledShvs**](inapenforcementclientconnection2-getinstalledshvs.md)     | Usato per ottenere gli ID dei file SHV installati per il client.<br/>             |
| [**INapEnforcementClientConnection2::GetIsolationInfoEx**](inapenforcementclientconnection2-getisolationinfoex.md) | Utilizzato per ottenere le informazioni di isolamento per il client.<br/>                 |
| [**INapEnforcementClientConnection2::SetInstalledShvs**](inapenforcementclientconnection2-setinstalledshvs.md)     | Usato da NapAgent per impostare gli ID SHV installati per il client.<br/>     |
| [**INapEnforcementClientConnection2::SetIsolationInfoEx**](inapenforcementclientconnection2-setisolationinfoex.md) | Utilizzato da NapAgent per impostare le informazioni di isolamento per il client.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> <dt>

[Interfacce di Protezione accesso alla rete](nap-interfaces.md)
</dt> <dt>

[Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)
</dt> </dl>

 

 





