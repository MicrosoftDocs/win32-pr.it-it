---
description: La classe CIM AllocatedResource rappresenta un'associazione tra dispositivi logici e risorse di sistema e indica che la risorsa \_ è assegnata al dispositivo.
ms.assetid: e1702635-32f5-4280-8c02-3940fd858106
ms.tgt_platform: multiple
title: CIM_AllocatedResource classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AllocatedResource
- CIM_AllocatedResource.Dependent
- CIM_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2caf51e4b6a76693a64253e1046ea74c6ec19b8f5895618419aa693a10260f56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322701"
---
# <a name="cim_allocatedresource-class"></a>Classe CiM \_ AllocatedResource

La **classe CIM \_ AllocatedResource** rappresenta un'associazione tra dispositivi logici e risorse di sistema e indica che la risorsa è assegnata al dispositivo.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{8502C579-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a>Members

La **classe CIM \_ AllocatedResource** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ AllocatedResource** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CiM \_ SystemResource**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Oggetto [**\_ SystemResource CIM**](cim-systemresource.md) che descrive la risorsa.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

[**LogicalDevice \_ CIM**](cim-logicaldevice.md) che contiene il dispositivo logico a cui è assegnata la risorsa.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe CIM \_ AllocatedResource** è derivata dalla [**dipendenza CIM \_**](cim-dependency.md).

WMI non implementa questa classe. Per altre informazioni sulle classi derivate da **CIM \_ AllocatedResource,** vedere [Classi Win32.](win32-provider.md)

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Dipendenza \_ CIM**](cim-dependency.md)
</dt> </dl>

 

