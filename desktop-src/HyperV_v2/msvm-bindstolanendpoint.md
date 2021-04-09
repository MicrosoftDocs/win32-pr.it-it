---
description: Questa associazione stabilisce un punto di accesso al servizio (SAP) come richiedente dei servizi del protocollo da un endpoint del protocollo.
ms.assetid: 14edefd8-d59b-4925-8b78-a979fb9a975f
title: Classe Msvm_BindsToLANEndpoint
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
ms.openlocfilehash: c2fa01c8e9e7df40a2907e6e43a9cb4b507a53d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968326"
---
# <a name="msvm_bindstolanendpoint-class"></a>\_Classe MSVM BindsToLANEndpoint

Questa associazione stabilisce un punto di accesso al servizio (SAP) come richiedente dei servizi del protocollo da un endpoint del protocollo. In genere, questa associazione viene eseguita tra i succhi e gli endpoint in un singolo sistema. Poiché un endpoint di protocollo è un tipo di SAP, questa associazione può essere usata per stabilire una sovrapposizione di due protocolli, con il livello superiore rappresentato dall'oggetto **dipendente** e il livello inferiore rappresentato dall'attività **precedente**.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

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

La **classe \_ BindsToLANEndpoint di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ BindsToLANEndpoint di MSVM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ LANEndpoint**](msvm-lanendpoint.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Riferimento a una classe [**MSVM \_ LANEndpoint**](msvm-lanendpoint.md) che rappresenta la porta di commutazione. Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ VLANEndpoint**](msvm-vlanendpoint.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Riferimento al [**\_ VLANEndpoint MSVM**](msvm-vlanendpoint.md) associato alla porta di commutazione. Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**FrameType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive il metodo di framing per il livello superiore SAP o endpoint associato all'endpoint LAN. Questa proprietà viene ereditata da **CIM \_ BindsToLANEndpoint** ed è sempre impostata su **null**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

