---
title: Interfaccia INapComponentConfig2 (NapCommon.h)
description: Fornisce metodi di configurazione del sistema di Protezione accesso alla rete per validator dell'integrità del sistema per configurare un'interfaccia utente del server dei criteri di rete in modalità remota.
ms.assetid: 35150184-300c-4ea4-bff9-b3c33fa3156b
keywords:
- Interfaccia INapComponentConfig2 nap
- Interfaccia INapComponentConfig2 nap , descritta
topic_type:
- apiref
api_name:
- INapComponentConfig2
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a80dfa1a9160b32b6d3c869795c9e23e41a5fdba39e38051bd29376caf8847
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368380"
---
# <a name="inapcomponentconfig2-interface"></a>Interfaccia INapComponentConfig2

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**L'interfaccia INapComponentConfig2** fornisce metodi di configurazione del sistema di Protezione accesso alla rete per validator dell'integrità del sistema (SHV) per configurare un'interfaccia utente del server dei criteri di rete (NPS) in modalità remota.

> [!Note]  
> Questa interfaccia eredita tutti i metodi di [**INapComponentConfig**](inapcomponentconfig.md) e deve essere usata.

 

## <a name="members"></a>Membri

**L'interfaccia INapComponentConfig2** eredita da [**INapComponentConfig**](inapcomponentconfig.md). **INapComponentConfig2** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia INapComponentConfig2** include questi metodi.



| Metodo                                                                                                | Descrizione                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig2::InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md)           | Implementata dagli SHV in base alle esigenze per gestire la configurazione remota direttamente nel computer specificato.<br/>                                                                 |
| [**INapComponentConfig2::InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)   | Implementata dagli SHV in base alle esigenze per caricare la configurazione del computer remoto in memoria e per visualizzare un'interfaccia utente che consente la manipolazione dei dati di configurazione.<br/> |
| [**INapComponentConfig2::IsRemoteConfigSupported**](inapcomponentconfig2-isremoteconfigsupported.md) | Implementato da SHV per indicare se la configurazione remota è supportata.<br/>                                                                                      |



 

## <a name="remarks"></a>Commenti

Questa interfaccia non deve essere implementata dagli agenti di integrità del sistema (SHA) o dai client di imposizione della quarantena (QEC).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[Interfacce di Protezione accesso alla rete](nap-interfaces.md)
</dt> <dt>

[Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)
</dt> </dl>

 

 





