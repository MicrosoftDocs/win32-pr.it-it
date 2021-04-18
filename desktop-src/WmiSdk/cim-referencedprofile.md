---
description: Utilizzato per associare un'istanza CIM \_ RegisteredProfile a un'istanza di CIM \_ RegisteredProfile di un altro profilo che fa riferimento al profilo dipendente come profilo correlato.
ms.assetid: 631003de-477b-4447-9633-1601a7f8eadb
ms.tgt_platform: multiple
title: Classe CIM_ReferencedProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReferencedProfile
- CIM_ReferencedProfile.Antecedent
- CIM_ReferencedProfile.Dependent
api_type:
- Schema
api_location:
- Root\interop
ms.openlocfilehash: 8fdc0d8dccd325ae7e13de971e09cce6faf93455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316573"
---
# <a name="cim_referencedprofile-class"></a>CIM \_ ReferencedProfile (classe)

Utilizzato per associare un'istanza [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) a un'istanza di **CIM \_ RegisteredProfile** di un altro profilo che fa riferimento al profilo dipendente come profilo correlato.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Version("2.8.0"), UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_ReferencedProfile : CIM_Dependency
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ ReferencedProfile** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ReferencedProfile** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'istanza [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) a cui fa riferimento il profilo **dipendente** .

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica un'istanza [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) che fa riferimento ad altri profili.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'uso delle proprietà **dipendenti** e **precedenti** nell'associazione **CIM \_ ReferencedProfile** è definito in modo che il profilo a cui viene fatto riferimento sia l'attività precedente e che il profilo che esegue il riferimento sia il dipendente.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                      |
| Spazio dei nomi<br/>                | \\Interoperabilità radice<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Interop. mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

