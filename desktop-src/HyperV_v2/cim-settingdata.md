---
description: Rappresenta i parametri di configurazione e operativi per le istanze \_ di CIM ManagedElement.
ms.assetid: a9ee0eb6-dc48-43f2-bdb5-f84fe7bbc1f2
title: CIM_SettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingData
- CIM_SettingData.InstanceID
- CIM_SettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 19c62496b7980c265ff20ae0b1cdb050e311e4c5e09fd981b49b562eed14596b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647323"
---
# <a name="cim_settingdata-class"></a>Classe CIM \_ SettingData

Rappresenta i parametri di configurazione e operativi [**per le istanze di \_ CIM ManagedElement.**](cim-managedelement.md)

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingData : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a>Members

La **classe CIM \_ SettingData** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ SettingData** ha queste proprietà.

<dl> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Obbligatorio,**](/windows/desktop/WmiSdk/standard-qualifiers) [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")
</dt> </dl>

Nome descrittivo per un'istanza di questa classe. Inoltre, il nome descrittivo può essere usato come indice per una ricerca o una query. Il nome non deve essere univoco all'interno di uno spazio dei nomi.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe nell'ambito dello spazio dei nomi contenitore.

> [!IMPORTANT]
>
> Per garantire l'univocità all'interno dello spazio dei nomi, il valore della proprietà **InstanceID** deve essere costruito nel modello seguente: *OrgID*:*LocalID*
>
> -   *OrgID* deve includere un nome protetto da copyright, con marchio o altrimenti univoco di proprietà dell'entità aziendale che definisce la proprietà **InstanceID** o un ID registrato assegnato da un'autorità globale riconosciuta.
> -   *OrgID non* deve contenere i due punti. I primi due punti in **InstanceID** devono essere compresi tra *OrgID* e *LocalID*.
> -   *LocalID* viene scelto dall'entità aziendale e non deve essere usato nuovamente per identificare diversi elementi reali sottostanti.
> -   Se il modello precedente non viene usato, l'entità di definizione deve garantire che il valore **InstanceID** risultante non viene usato di nuovo in tutte le proprietà **InstanceID** prodotte da questo provider o da altri provider per questo spazio dei nomi.
> -   Per le istanze definite da DMTF, il modello deve essere usato con *OrgID* impostato su "CIM".

 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ ManagedElement**](cim-managedelement.md)
</dt> </dl>

 

