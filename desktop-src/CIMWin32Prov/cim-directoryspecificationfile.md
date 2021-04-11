---
description: L' \_ associazione CIM DirectorySpecificationFile rappresenta la directory che contiene il file specificato facendo riferimento alla \_ classe CIM DirectorySpecification.
ms.assetid: 57fe996e-6bd4-4070-9e99-460b2a36243f
ms.tgt_platform: multiple
title: Classe CIM_DirectorySpecificationFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecificationFile
- CIM_DirectorySpecificationFile.DirectorySpecification
- CIM_DirectorySpecificationFile.FileSpecification
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1877d9864a76334c2b2e00fc7822adb09b91028b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127183"
---
# <a name="cim_directoryspecificationfile-class"></a>CIM \_ DirectorySpecificationFile (classe)

L'associazione **CIM \_ DirectorySpecificationFile** rappresenta la directory che contiene il file specificato facendo riferimento alla classe [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) .

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{BCD64CCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_DirectorySpecificationFile
{
  CIM_DirectorySpecification REF DirectorySpecification;
  CIM_FileSpecification      REF FileSpecification;
};
```

## <a name="members"></a>Members

La classe **CIM \_ DirectorySpecificationFile** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ DirectorySpecificationFile** dispone di queste proprietà.

<dl> <dt>

**DirectorySpecification**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ DirectorySpecification**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Riferimento alla specifica di directory.

</dd> <dt>

**Filespecificazione**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ filespecificazione CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Riferimento alla specifica del file.

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

