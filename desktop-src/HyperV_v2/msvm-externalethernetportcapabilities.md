---
description: Descrive le funzionalità del ExternalEthernetPort MSVM associato \_ .
ms.assetid: 63731b62-b1c7-4dd9-b906-03225bbc3154
title: Classe Msvm_ExternalEthernetPortCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalEthernetPortCapabilities
- Msvm_ExternalEthernetPortCapabilities.InstanceID
- Msvm_ExternalEthernetPortCapabilities.Caption
- Msvm_ExternalEthernetPortCapabilities.Description
- Msvm_ExternalEthernetPortCapabilities.ElementName
- Msvm_ExternalEthernetPortCapabilities.IOVSupport
- Msvm_ExternalEthernetPortCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 748b207151fb1d11b013af7c736de52bbe5bec8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879589"
---
# <a name="msvm_externalethernetportcapabilities-class"></a>\_Classe MSVM ExternalEthernetPortCapabilities

Descrive le funzionalità del [**\_ ExternalEthernetPort MSVM**](msvm-externalethernetport.md)associato.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalEthernetPortCapabilities : CIM_Capabilities
{
  string  InstanceID;
  string  Caption = "Ethernet Port Capabilities";
  string  Description = "Describes the capabilities of the Microsoft External Ethernet Port";
  string  ElementName = "Ethernet Port Capabilities";
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a>Members

La **classe \_ ExternalEthernetPortCapabilities di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ExternalEthernetPortCapabilities di MSVM** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Port Capabilities".

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "descrive le funzionalità della porta Ethernet esterna Microsoft".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Port Capabilities".

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**IOVSupport**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore booleano che indica se la virtualizzazione I/O (IOV) è supportata dalla scheda di rete. Se il valore è **true**, IOV è supportato dalla scheda di rete e la proprietà **IOVSupportReasons** sarà vuota. In caso contrario, la proprietà **IOVSupportReasons** avrà i motivi per cui non è possibile supportare IOV.

</dd> <dt>

**IOVSupportReasons**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe che indica i possibili motivi per cui IOV non è supportato. Se il valore di **IOVSupport** è **true**, questa matrice sarà vuota.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

