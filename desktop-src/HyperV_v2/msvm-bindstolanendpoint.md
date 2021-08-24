---
description: Questa associazione stabilisce un punto di accesso al servizio (SAP) come richiedente dei servizi di protocollo da un endpoint di protocollo.
ms.assetid: 14edefd8-d59b-4925-8b78-a979fb9a975f
title: Msvm_BindsToLANEndpoint classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BindsToLANEndpoint
- Msvm_BindsToLANEndpoint.Antecedent
- Msvm_BindsToLANEndpoint.Dependent
- Msvm_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44dc8d88475b23d8d7ac12ec36eba96376cf19b7d4d3168556519597d445c73d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870407"
---
# <a name="msvm_bindstolanendpoint-class"></a>Classe \_ Msvm BindsToLANEndpoint

Questa associazione stabilisce un punto di accesso al servizio (SAP) come richiedente dei servizi di protocollo da un endpoint di protocollo. In genere, questa associazione viene eseguita tra i punti di accesso condiviso e gli endpoint in un singolo sistema. Poiché un endpoint del protocollo è un tipo di SAP, questa associazione può essere usata per stabilire un livello di due protocolli, con il livello superiore rappresentato da **Dependent** e il livello inferiore rappresentato **dall'attività** precedente.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BindsToLANEndpoint : CIM_BindsToLANEndpoint
{
  Msvm_LANEndpoint  REF Antecedent;
  Msvm_VLANEndpoint REF Dependent;
  uint16                FrameType;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ BindsToLANEndpoint** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ BindsToLANEndpoint** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Riferimento a una [**classe \_ MSvm LANEndpoint**](msvm-lanendpoint.md) che rappresenta la porta del commutatore. Questa proprietà viene ereditata dalla [**dipendenza CIM \_**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ VLANEndpoint**](msvm-vlanendpoint.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

Riferimento all'oggetto [**\_ VLANEndpoint msvm**](msvm-vlanendpoint.md) associato alla porta del commutatore. Questa proprietà viene ereditata dalla [**dipendenza CIM \_**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**FrameType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive il metodo di framing per l'endpoint SAP di livello superiore associato all'endpoint LAN. Questa proprietà viene ereditata da **CIM \_ BindsToLANEndpoint** ed è sempre impostata su **Null.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

