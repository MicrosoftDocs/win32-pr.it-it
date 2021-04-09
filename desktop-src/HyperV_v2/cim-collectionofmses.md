---
description: Classe astratta per le sottoclassi che rappresentano una raccolta di \_ oggetti MANAGEDSYSTEMELEMENT CIM. Queste raccolte consentono di raggruppare gli elementi di sistema gestiti a scopo di identificazione e di semplificare l'associazione delle impostazioni e delle configurazioni.
ms.assetid: f47bf1d6-6d89-4d9f-82d1-99a7343481bc
title: Classe CIM_CollectionOfMSEs (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.CollectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e467e775c78364718f25cc732d6689d9fb2b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880766"
---
# <a name="cim_collectionofmses-class-hyper-v-management"></a>Classe CIM_CollectionOfMSEs (gestione Hyper-V)

Classe astratta per le sottoclassi che rappresentano una raccolta di oggetti [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) . Queste raccolte consentono di raggruppare gli elementi di sistema gestiti a scopo di identificazione e di semplificare l'associazione delle impostazioni e delle configurazioni.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectionOfMSEs : CIM_Collection
{
  string CollectionID;
};
```

## <a name="members"></a>Members

La classe **CIM \_ CollectionOfMSEs** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ CollectionOfMSEs** dispone di queste proprietà.

<dl> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificazione dell'oggetto raccolta. Quando è sottoclassata, la proprietà **CollectionId** può essere sottoposta a override come proprietà chiave.

</dd> </dl>

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

[**\_Raccolta CIM**](cim-collection.md)
</dt> </dl>

 

