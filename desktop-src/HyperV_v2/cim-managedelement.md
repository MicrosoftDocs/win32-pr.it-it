---
description: La classe CIM ManagedElement è una classe astratta che fornisce una superclasse comune (o la parte superiore dell'albero di ereditarietà) per le classi non di associazione \_ nello schema CIM.
ms.assetid: 6655a480-37bd-403c-9673-4eaa3d381201
title: CIM_ManagedElement classe
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
ms.openlocfilehash: acce9925f057ab63e0697c2bc12cae4336533068afdf43f46322e4d3718b25c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648183"
---
# <a name="cim_managedelement-class"></a>Classe \_ CiM ManagedElement

La **classe \_ CIM ManagedElement** è una classe astratta che fornisce una superclasse comune (o la parte superiore dell'albero di ereditarietà) per le classi non di associazione nello schema CIM.

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

La **classe \_ CIM ManagedElement** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ CiM ManagedElement** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrizione testuale dell'oggetto.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto .

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome descrittivo dell'oggetto. Questa proprietà consente a ogni istanza di definire un nome descrittivo oltre alle relative proprietà chiave, ai dati di identità e alle informazioni sulla descrizione.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica in modo univoco e opaco un'istanza di questa classe all'interno dell'ambito dello spazio dei nomi contenitore.

> [!IMPORTANT]
>
> Per garantire l'univocità all'interno dello spazio dei nomi, il valore della proprietà **InstanceID** deve essere costruito nel modello seguente: *OrgID*:*LocalID*
>
> *OrgID* deve includere un nome protetto da copyright, registrato o altrimenti univoco di proprietà dell'entità aziendale che definisce **InstanceID** o essere un ID registrato assegnato da un'autorità globale riconosciuta. Questo modello è simile alla struttura dei nomi delle classi dello schema. Inoltre, per garantire l'univocità, i primi due punti in **InstanceID** devono essere compresi tra *OrgID* e *LocalID*. *L'ORGID non* deve pertanto contenere i due punti (':').
>
> *LocalID* viene scelto dall'entità business e non deve essere usato nuovamente per identificare diversi elementi reali sottostanti.
>
> Se il modello precedente non viene usato, l'entità di definizione deve garantire che il valore **InstanceID** risultante non sia usato di nuovo in tutte le proprietà **InstanceID** prodotte da questo provider o da altri provider per questo spazio dei nomi.
>
> Per le istanze definite da DmTF (Distributed Management Task Force), il modello deve essere usato con *OrgID* impostato su CIM.

 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

