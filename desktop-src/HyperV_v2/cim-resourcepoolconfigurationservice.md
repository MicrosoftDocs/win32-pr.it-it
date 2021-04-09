---
description: Gestisce la configurazione dei pool di risorse utilizzando i processi.
ms.assetid: cc0f0236-2335-4dd9-9132-51b3e6b9fcf4
title: Classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e8dbbce21f7749b7f436e2f49acb7ce6c7340faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879509"
---
# <a name="cim_resourcepoolconfigurationservice-class"></a>CIM \_ ResourcePoolConfigurationService (classe)

Gestisce la configurazione dei pool di risorse utilizzando i processi.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationService : CIM_Service
{
};
```

## <a name="members"></a>Members

La classe **CIM \_ ResourcePoolConfigurationService** presenta questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La classe **CIM \_ ResourcePoolConfigurationService** presenta questi metodi.



| Metodo                                                                                                          | Descrizione                                                                   |
|:----------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**AddResourcesToResourcePool**](cim-resourcepoolconfigurationservice-addresourcestoresourcepool.md)           | Avvia un processo per l'aggiunta di risorse a un pool di risorse.<br/>                  |
| [**ChangeParentResourcePool**](cim-resourcepoolconfigurationservice-changeparentresourcepool.md)               | Avviare un processo per modificare il pool di risorse padre di un pool di risorse.<br/> |
| [**CreateChildResourcePool**](cim-resourcepoolconfigurationservice-createchildresourcepool.md)                 | Avviare un processo per creare un pool di risorse da un pool di risorse padre.<br/> |
| [**CreateResourcePool**](cim-resourcepoolconfigurationservice-createresourcepool.md)                           | Avvia un processo per creare un pool di risorse radice.<br/>                       |
| [**DeleteResourcePool**](cim-resourcepoolconfigurationservice-deleteresourcepool.md)                           | Avviare un processo per eliminare un pool di risorse.<br/>                             |
| [**RemoveResourcesFromResourcePool**](cim-resourcepoolconfigurationservice-removeresourcesfromresourcepool.md) | Avvia un processo per rimuovere le risorse da un pool di risorse.<br/>             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Servizio CIM**](cim-service.md)
</dt> </dl>

 

 




