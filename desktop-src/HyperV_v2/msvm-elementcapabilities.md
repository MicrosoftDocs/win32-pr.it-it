---
description: Rappresenta l'associazione tra gli elementi gestiti e le relative funzionalità.
ms.assetid: F083E6D2-CC74-4DAD-8FF7-3FE3CA4EEFFF
title: Classe Msvm_ElementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementCapabilities
- Msvm_ElementCapabilities.ManagedElement
- Msvm_ElementCapabilities.Capabilities
- Msvm_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7602de569a51aec73130a4b5f4d3ba339cb29c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314329"
---
# <a name="msvm_elementcapabilities-class"></a>\_Classe MSVM ElementCapabilities

Rappresenta l'associazione tra gli elementi gestiti e le relative funzionalità.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementCapabilities : CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a>Members

La **classe \_ ElementCapabilities di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ElementCapabilities di MSVM** dispone di queste proprietà.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **\_ funzionalità CIM**](/previous-versions//cc136806(v=vs.85))**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Oggetto funzionalità associato all'elemento. Questa proprietà viene ereditata da [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).

</dd> <dt>

**Caratteristiche**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni descrittive sulle funzionalità. Questa proprietà viene ereditata da [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).



| Valore                                                                                                                                                                                                                       | Significato                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <dt>**Impostazione predefinita**</dt> <dt>2</dt> </dl> | Le funzionalità associate rappresentano le funzionalità predefinite dell'elemento gestito.<br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <dt>**Corrente**</dt> <dt>3</dt> </dl> | Le funzionalità associate rappresentano le funzionalità correnti dell'elemento gestito.<br/> |



 

</dd> <dt>

**ManagedElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**, **min** (1)
</dt> </dl>

Elemento gestito. Questa proprietà viene ereditata da [**CIM \_ ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ ElementCapabilities di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ELEMENTCAPABILITIES CIM**](cim-elementcapabilities.md)
</dt> <dt>

[**\_ELEMENTCAPABILITIES CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)
</dt> <dt>

[**MSVM \_ ElementCapabilities (V1)**](/previous-versions/windows/desktop/virtual/msvm-elementcapabilities)
</dt> </dl>

 

