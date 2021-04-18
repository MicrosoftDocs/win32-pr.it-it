---
description: Descrive le restrizioni sulle proprietà di un \_ oggetto ENABLEDLOGICALELEMENT CIM associato.
ms.assetid: debce40c-9a0e-43a7-88fa-9336afd52e17
title: Classe CIM_EnabledLogicalElementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElementCapabilities
- CIM_EnabledLogicalElementCapabilities.ElementNameEditSupported
- CIM_EnabledLogicalElementCapabilities.MaxElementNameLen
- CIM_EnabledLogicalElementCapabilities.RequestedStatesSupported
- CIM_EnabledLogicalElementCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35f400643e01821667c999342603fd402a3ae419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312924"
---
# <a name="cim_enabledlogicalelementcapabilities-class"></a>CIM \_ EnabledLogicalElementCapabilities (classe)

Descrive le restrizioni sulle proprietà di un oggetto [**\_ EnabledLogicalElement CIM**](cim-enabledlogicalelement.md) associato.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_EnabledLogicalElementCapabilities : CIM_Capabilities
{
  boolean ElementNameEditSupported;
  uint16  MaxElementNameLen;
  uint16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a>Members

La classe **CIM \_ EnabledLogicalElementCapabilities** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ EnabledLogicalElementCapabilities** dispone di queste proprietà.

<dl> <dt>

**ElementNameEditSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-swapi. Incis-T11 \| swapping \_ unità \_ config i \_ Caps \_ T \| EditName "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ Managed**](cim-managedelement.md).**ElementName**")
</dt> </dl>

**true** se la proprietà **ElementName** dell'elemento logico abilitato può essere modificata. in caso contrario, **false**.

</dd> <dt>

**ElementNameMask**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElementCapabilities**.**MaxElementNameLen**")
</dt> </dl>

Espressione regolare che indica le restrizioni sulla proprietà **ElementName** dell'elemento logico Enable. Vedere *DMTF standard ABNF con la Guida all'utilizzo della specifica del profilo di gestione*, Appendice C per la sintassi consentita.

> [!Note]  
> Se questa proprietà e la proprietà **ElementNameMask** dell'elemento logico Enable descrivono la lunghezza massima di **ElementName**, viene usato il valore più piccolo.

 

</dd> <dt>

**MaxElementNameLen**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-swapi. INCIs-T11 \| swapi \_ unit \_ config \_ Caps \_ T \| MaxNameChars "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ FCSwitchCapabilities. ElementNameEditSupported ","**CIM \_ EnabledLogicalElementCapabilities**.**ElementNameMask**")
</dt> </dl>

Lunghezza massima supportata della proprietà **ElementName** dell'elemento logico abilitato.

</dd> <dt>

**RequestedStatesSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**RequestStateChange**")
</dt> </dl>

Gli stati possibili che possono essere richiesti sull'elemento logico abilitato tramite il metodo [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) .

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Abilitato** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Disabilitato** (3)


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

**Arresto** (4)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Offline** (6)


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

**Test** (7)


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

**Rinvia** (8)


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

**Mettere in stato** (9)


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**Riavvio** (10)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Reimposta** (11)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Funzionalità CIM**](cim-capabilities.md)
</dt> </dl>

 

