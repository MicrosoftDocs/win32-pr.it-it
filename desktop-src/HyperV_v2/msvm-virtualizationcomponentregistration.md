---
description: Rappresenta la registrazione di un servizio nella piattaforma Microsoft Hyper-V.
ms.assetid: 706557C2-49D6-453F-9DC0-2C655888EEBE
title: Msvm_VirtualizationComponentRegistration classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponentRegistration
- Msvm_VirtualizationComponentRegistration.Component
- Msvm_VirtualizationComponentRegistration.ResourceType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c7acd111ab95f59146763e874d40c4efb411313938c94b1a4527aa1e2d08490c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146555"
---
# <a name="msvm_virtualizationcomponentregistration-class"></a>Classe Msvm \_ VirtualizationComponentRegistration

Rappresenta la registrazione di un servizio nella piattaforma Microsoft Hyper-V.

La sintassi seguente è semplificata Managed Object Format (MOF).

## <a name="syntax"></a>Sintassi

``` syntax
class Msvm_VirtualizationComponentRegistration
{
  Msvm_VirtualizationComponent REF Component;
  Msvm_ResourceTypeDefinition  REF ResourceType;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ VirtualizationComponentRegistration** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ VirtualizationComponentRegistration** ha queste proprietà.

<dl> <dt>

**Componente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un'istanza di che descrive l'oggetto COM che implementa questa classe.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un'istanza di che descrive un tipo di risorsa supportato dal servizio.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ VirtualizationComponentRegistration** potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Fine del supporto client<br/>    | Windows 8.1<br/>                                                                                  |
| Fine del supporto server<br/>    | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

