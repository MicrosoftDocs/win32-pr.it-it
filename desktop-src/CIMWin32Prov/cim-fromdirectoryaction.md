---
description: L'associazione CIM \_ FromDirectoryAction identifica la directory di origine per l'azione file.
ms.assetid: 25d06dad-ae39-4cfc-9331-4be7ef02d87c
ms.tgt_platform: multiple
title: CIM_FromDirectoryAction classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FromDirectoryAction
- CIM_FromDirectoryAction.FileName
- CIM_FromDirectoryAction.SourceDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2d9055b47448bf21543dd738f5378ac0e19d209ebb0a40346e07cd57e01c8f63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923731"
---
# <a name="cim_fromdirectoryaction-class"></a>Classe CIM \_ FromDirectoryAction

**L'associazione CIM \_ FromDirectoryAction** identifica la directory di origine per l'azione file. Quando si usa questa associazione, si presuppone che la directory di origine sia stata creata da un'azione precedente. Questa associazione non può esistere con [**un'associazione CIM \_ FromDirectorySpecification.**](cim-fromdirectoryspecification.md) Un'azione di file può includere solo una singola directory di origine.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{55D5B446-DB2A-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_FromDirectoryAction
{
  CIM_FileAction      REF FileName;
  CIM_DirectoryAction REF SourceDirectory;
};
```

## <a name="members"></a>Members

La **classe CIM \_ FromDirectoryAction** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ FromDirectoryAction** ha queste proprietà.

<dl> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ FileAction**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Riferimento al nome del file.

</dd> <dt>

**SourceDirectory**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ DirectoryAction**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Riferimento alla directory di origine.

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

