---
description: Descrive le restrizioni relative alle proprietà di un oggetto CIM \_ EnabledLogicalElement associato.
ms.assetid: debce40c-9a0e-43a7-88fa-9336afd52e17
title: CIM_EnabledLogicalElementCapabilities classe
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
ms.openlocfilehash: cbec7b52d735b6dcff4da4c211da1db8b36d18adf20798fdcaa3932e1761119a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695911"
---
# <a name="cim_enabledlogicalelementcapabilities-class"></a>Classe CIM \_ EnabledLogicalElementCapabilities

Descrive le restrizioni relative alle proprietà di un oggetto [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md) associato.

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

La **classe CIM \_ EnabledLogicalElementCapabilities** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ EnabledLogicalElementCapabilities** ha queste proprietà.

<dl> <dt>

**ElementNameEditSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI. INCITS-T11 \| SWAPI \_ UNIT CONFIG \_ \_ CAPS T \_ \| EditName"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ManagedElement**](cim-managedelement.md).**ElementName**")
</dt> </dl>

**true** se la **proprietà ElementName** dell'elemento logico abilitato può essere modificata; in caso contrario, **false.**

</dd> <dt>

**ElementNameMask**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElementCapabilities**.**MaxElementNameLen**")
</dt> </dl>

Espressione regolare che indica le restrizioni per la proprietà **ElementName** dell'elemento logico enable. Per *la sintassi consentita, vedere ABNF standard DMTF con la Guida all'utilizzo della* specifica del profilo di gestione , appendice C.

> [!Note]  
> Se questa proprietà e la **proprietà ElementNameMask** dell'elemento logico enable descrivono la lunghezza massima di **ElementName**, viene usato il valore più piccolo.

 

</dd> <dt>

**MaxElementNameLen**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI. INCITS-T11 \| SWAPI \_ UNIT CONFIG \_ \_ CAPS T \_ \| MaxNameChars"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ FCSwitchCapabilities.ElementNameEditSupported", "**CIM \_ EnabledLogicalElementCapabilities**.**ElementNameMask**")
</dt> </dl>

Lunghezza massima supportata della proprietà **ElementName** dell'elemento logico abilitato.

</dd> <dt>

**RequestedStatesSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**RequestStateChange**")
</dt> </dl>

Stati possibili che possono essere richiesti nell'elemento logico abilitato dal [**metodo RequestStateChange.**](cim-enabledlogicalelement-requeststatechange.md)

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Abilitato** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Disabilitato** (3)


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

**Arresta** (4)


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

**Inattiva** (9)


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

**Riavvio** (10)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Reset** (11)


</dt> <dd></dd> </dl>

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

[**Funzionalità \_ CIM**](cim-capabilities.md)
</dt> </dl>

 

