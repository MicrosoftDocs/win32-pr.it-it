---
description: L'associazione CIM \_ ToDirectoryAction identifica la directory di destinazione per l'azione file.
ms.assetid: f4dcd99c-4da8-447d-b6f7-7e3da63ca9c4
ms.tgt_platform: multiple
title: CIM_ToDirectoryAction classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectoryAction
- CIM_ToDirectoryAction.DestinationDirectory
- CIM_ToDirectoryAction.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 37ecee55fa76f6e86ccc60921851eca6cb922bec8fb6b00de01c3e410ca19940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020869"
---
# <a name="cim_todirectoryaction-class"></a>Classe \_ CiM ToDirectoryAction

**L'associazione CIM \_ ToDirectoryAction** identifica la directory di destinazione per l'azione file. Quando si utilizza questa associazione, si presuppone che la directory di destinazione sia stata creata da un'azione precedente. Questa associazione non può esistere con [**un'associazione \_ CiM ToDirectorySpecification**](cim-todirectoryspecification.md) perché un'azione file può interessare solo una singola directory di destinazione.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{B58D172E-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectoryAction
{
  CIM_DirectoryAction REF DestinationDirectory;
  CIM_CopyFileAction  REF FileName;
};
```

## <a name="members"></a>Members

La **classe \_ CiM ToDirectoryAction** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ ToDirectoryAction** ha queste proprietà.

<dl> <dt>

**DestinationDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ DirectoryAction**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Riferimento alla directory di destinazione.

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ CopyFileAction**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Riferimento al nome del file.

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

