---
description: Classe astratta per sottoclassi che rappresentano una raccolta di oggetti CIM \_ ManagedSystemElement. Queste raccolte consentono di raggruppare gli elementi di sistema gestiti a scopo di identificazione e di semplificare l'associazione di impostazioni e configurazioni.
ms.assetid: f47bf1d6-6d89-4d9f-82d1-99a7343481bc
title: CIM_CollectionOfMSEs classe (gestione Hyper-V)
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
ms.openlocfilehash: 8598b8208b9291ec9dabc405f1b1c8d18513ff111e22ec8caa6c8bf32fb946f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813324"
---
# <a name="cim_collectionofmses-class-hyper-v-management"></a>CIM_CollectionOfMSEs classe (gestione Hyper-V)

Classe astratta per sottoclassi che rappresentano una raccolta di [**oggetti CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md) Queste raccolte consentono di raggruppare gli elementi di sistema gestiti a scopo di identificazione e di semplificare l'associazione di impostazioni e configurazioni.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectionOfMSEs : CIM_Collection
{
  string CollectionID;
};
```

## <a name="members"></a>Members

La **classe CIM \_ CollectionOfMSEs** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ CollectionOfMSEs** ha queste proprietà.

<dl> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificazione dell'oggetto raccolta. In caso di sottoclasse, la **proprietà CollectionID** può essere sottoposta a override come proprietà chiave.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Raccolta \_ CIM**](cim-collection.md)
</dt> </dl>

 

