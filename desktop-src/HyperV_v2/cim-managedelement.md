---
description: La \_ classe CIM Managed è una classe astratta che fornisce una superclasse comune (o parte superiore dell'albero di ereditarietà) per le classi non di associazione nello schema CIM.
ms.assetid: 6655a480-37bd-403c-9673-4eaa3d381201
title: Classe CIM_ManagedElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedElement
- CIM_ManagedElement.InstanceID
- CIM_ManagedElement.Caption
- CIM_ManagedElement.Description
- CIM_ManagedElement.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5d98c6e594103932b180fcb63a2eebaf2c328c4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305661"
---
# <a name="cim_managedelement-class"></a>CIM \_ managementelement (classe)

La classe **CIM \_ Managed** è una classe astratta che fornisce una superclasse comune (o parte superiore dell'albero di ereditarietà) per le classi non di associazione nello schema CIM.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a>Members

La classe **CIM \_ Managed** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ Managed** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrizione testuale dell'oggetto.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome descrittivo dell'oggetto. Questa proprietà consente a ogni istanza di definire un nome descrittivo in aggiunta alle relative proprietà chiave, dati di identità e informazioni sulla descrizione.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica in modo univoco e opaco un'istanza di questa classe nell'ambito dello spazio dei nomi che lo contiene.

> [!IMPORTANT]
>
> Per garantire l'univocità all'interno dello spazio dei nomi, il valore della proprietà **InstanceID** deve essere costruito nel modello seguente: *OrgID*:*LocalId*
>
> *OrgID* deve includere un nome con copyright, marchio o in altro modo univoco, di proprietà dell'entità di business che definisce **InstanceID**, oppure essere un ID registrato assegnato da un'autorità globale riconosciuta. Questo modello è simile alla struttura dei nomi delle classi dello schema. Inoltre, per garantire l'univocità, i primi due punti in **InstanceID** devono essere compresi tra *OrgID* e *LocalId*. Pertanto *OrgID* non deve contenere i due punti (':').
>
> Il *localizzato* viene scelto dall'entità di business e non deve essere riutilizzato per identificare diversi elementi reali sottostanti.
>
> Se il criterio precedente non viene utilizzato, l'entità di definizione deve assicurare che il valore **InstanceID** risultante non venga riutilizzato nelle proprietà **InstanceID** generate dal provider o da altri provider per questo spazio dei nomi.
>
> Per le istanze definite DMTF (Distributed Management Task Force), il modello deve essere usato con *OrgID* impostato su CIM.

 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

