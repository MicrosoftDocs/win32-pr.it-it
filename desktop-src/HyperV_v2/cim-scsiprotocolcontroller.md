---
description: Rappresenta un controller di protocollo che gestisce un'interfaccia SCSI.
ms.assetid: 01ef85fc-2f05-4453-b524-7d63b647f6fb
title: Classe CIM_SCSIProtocolController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIProtocolController
- CIM_SCSIProtocolController.NameFormat
- CIM_SCSIProtocolController.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6479b405d3ca499615981d62744b1eaf25c7598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307769"
---
# <a name="cim_scsiprotocolcontroller-class"></a>CIM \_ SCSIProtocolController (classe)

Rappresenta un controller di protocollo che gestisce un'interfaccia SCSI.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.8.1000"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_SCSIProtocolController : CIM_ProtocolController
{
  uint16 NameFormat;
  string OtherNameFormat;
};
```

## <a name="members"></a>Members

La classe **CIM \_ SCSIProtocolController** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ SCSIProtocolController** dispone di queste proprietà.

<dl> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SCSIProtocolController**.**Nome**","**CIM \_ SCSIProtocolController**.**OtherNameFormat**")
</dt> </dl>

Formato della proprietà **Name** del **\_ SCSIProtocolController CIM**.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="FC_Port_WWN"></span><span id="fc_port_wwn"></span><span id="FC_PORT_WWN"></span>

**Porta FC WWN** (2)


</dt> <dd></dd> <dt>

<span id="iSCSI_Name"></span><span id="iscsi_name"></span><span id="ISCSI_NAME"></span>

**nome iSCSI** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherNameFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SCSIProtocolController**.**Nome**","**CIM \_ SCSIProtocolController**.**NameFormat**")
</dt> </dl>

Descrizione della proprietà **NameFormat** quando **NameFormat** è impostato su "1" (other).

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

[**\_PROTOCOLCONTROLLER CIM**](cim-protocolcontroller.md)
</dt> </dl>

 

