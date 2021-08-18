---
description: Usato per associare un'istanza di CIM RegisteredProfile a un'istanza di CIM RegisteredProfile di un altro profilo che fa riferimento al profilo \_ \_ dipendente come profilo correlato.
ms.assetid: 631003de-477b-4447-9633-1601a7f8eadb
ms.tgt_platform: multiple
title: CIM_ReferencedProfile classe
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
ms.openlocfilehash: 39cfa6dac2fd827b2ce690afa5cdd7126322c2f81182db674517c75911791a0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556813"
---
# <a name="cim_referencedprofile-class"></a>Classe \_ ReferencedProfile CIM

Usato per associare [**un'istanza di CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) a un'istanza di **CIM \_ RegisteredProfile** di un altro profilo che fa riferimento al profilo dipendente come profilo correlato.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

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

La **classe CIM \_ ReferencedProfile** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ ReferencedProfile** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica [**l'istanza CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) a cui fa riferimento il **profilo Dipendente.**

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica [**un'istanza CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) che fa riferimento ad altri profili.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'uso delle proprietà **Dependent** e **Antecedent** nell'associazione **CIM \_ ReferencedProfile** è definito in modo che il profilo a cui viene fatto riferimento sia l'antecedente e che il profilo che effettua il riferimento sia il dipendente.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                      |
| Spazio dei nomi<br/>                | Interoperabilità \\ radice<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Interop.mof</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Dipendenza \_ CIM**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

