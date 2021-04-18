---
title: Interfaccia INapComponentConfig2 (NapCommon. h)
description: Fornisce metodi di configurazione del sistema NAP per i validator di integrità di sistema (SHV) per configurare un'interfaccia utente di server dei criteri di rete in modalità remota.
ms.assetid: 35150184-300c-4ea4-bff9-b3c33fa3156b
keywords:
- NAP interfaccia INapComponentConfig2
- Interfaccia NAP di INapComponentConfig2, descrizione
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
ms.openlocfilehash: 29bd6fbea7696d0e4d5eacefd028ce7d33e549e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301368"
---
# <a name="inapcomponentconfig2-interface"></a>Interfaccia INapComponentConfig2

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

L'interfaccia **INapComponentConfig2** fornisce metodi di configurazione del sistema NAP per i validator di integrità di sistema (SHV) per configurare un'interfaccia utente di server dei criteri di rete in modalità remota.

> [!Note]  
> Questa interfaccia eredita tutti i metodi di [**INapComponentConfig**](inapcomponentconfig.md) e deve essere usata in alternativa.

 

## <a name="members"></a>Membri

L'interfaccia **INapComponentConfig2** eredita da [**INapComponentConfig**](inapcomponentconfig.md). **INapComponentConfig2** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapComponentConfig2** dispone di questi metodi.



| Metodo                                                                                                | Descrizione                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig2::InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md)           | Implementato da SHV in base alle esigenze per gestire la configurazione remota direttamente nel computer specificato.<br/>                                                                 |
| [**INapComponentConfig2::InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)   | Implementata da SHV in base alle esigenze per caricare la configurazione del computer remoto in memoria e visualizzare un'interfaccia utente che consente la modifica dei dati di configurazione.<br/> |
| [**INapComponentConfig2::IsRemoteConfigSupported**](inapcomponentconfig2-isremoteconfigsupported.md) | Implementato da SHV per indicare se la configurazione remota è supportata.<br/>                                                                                      |



 

## <a name="remarks"></a>Commenti

Questa interfaccia non deve essere implementata dagli agenti di integrità del sistema (SHAs) o dai client di imposizione di quarantena (QeC).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

 





