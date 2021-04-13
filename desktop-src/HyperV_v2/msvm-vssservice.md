---
description: Rappresenta il servizio VSS Guest. Viene utilizzato per eseguire query sulle informazioni del cluster guest dall'host Hyper-V.
ms.assetid: 82321456-a24e-4f67-9346-f0844e2913dc
title: Classe Msvm_VssService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 298ced09537ffc6e17f98484f600b05155fe0d97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342771"
---
# <a name="msvm_vssservice-class"></a>\_Classe MSVM VssService

Rappresenta il servizio VSS Guest. Viene utilizzato per eseguire query sulle informazioni del cluster guest dall'host Hyper-V.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VssService : Msvm_GuestService
{
};
```

## <a name="members"></a>Members

La **classe \_ VssService di MSVM** dispone di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe \_ VssService di MSVM** dispone di questi metodi.



| Metodo                                                                               | Descrizione                                                                 |
|:-------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md) | Esecuzione di query sulle informazioni del cluster dall'host Hyper-V al Guest.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GuestService MSVM**](msvm-guestservice.md)
</dt> </dl>

 

 




