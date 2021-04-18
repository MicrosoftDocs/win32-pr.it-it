---
description: Rappresenta un'associazione tra un processo e l'elemento gestito che ha creato il processo.
ms.assetid: 08c33a81-0a3f-4545-9812-96a854a7509e
title: Classe CIM_OwningJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OwningJobElement
- CIM_OwningJobElement.OwningElement
- CIM_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9d3879104a8f7406ff24dc2f63b79b51eb2fa58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317210"
---
# <a name="cim_owningjobelement-class"></a>CIM \_ OwningJobElement (classe)

Rappresenta un'associazione tra un processo e l'elemento gestito che ha creato il processo. Poiché un processo può spostarsi tra i sistemi e l'elemento gestito potrebbe non esistere per l'intera durata del processo, in alcuni casi, questa associazione potrebbe non essere possibile o esistere solo per una parte dell'esistenza del processo.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::System::Processing"), ModelCorrespondence("CIM_Job.Owner"), AMENDMENT]
class CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  CIM_Job            REF OwnedElement;
};
```

## <a name="members"></a>Members

La classe **CIM \_ OwningJobElement** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ OwningJobElement** dispone di queste proprietà.

<dl> <dt>

**Proprietàelement**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ processo CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Riferimento al processo creato dall'elemento gestito.

</dd> <dt>

**OwningElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ Managed**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Riferimento all'elemento gestito che ha creato il processo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

