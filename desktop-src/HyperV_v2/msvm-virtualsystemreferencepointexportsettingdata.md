---
description: Fornisce informazioni aggiuntive da utilizzare con il metodo ExportReferencePoint della \_ classe VirtualSystemReferencePointService di MSVM.
ms.assetid: 4897fad4-3a3f-47bc-837d-2e36434b3fab
title: Classe Msvm_VirtualSystemReferencePointExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportSettingData
- Msvm_VirtualSystemReferencePointExportSettingData.BaseReferencePoint
- Msvm_VirtualSystemReferencePointExportSettingData.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65fc16f409fd79782ec4a91f223dfc754563f8bb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104058452"
---
# <a name="msvm_virtualsystemreferencepointexportsettingdata-class"></a>\_Classe MSVM VirtualSystemReferencePointExportSettingData

Fornisce informazioni aggiuntive da utilizzare con il metodo [**ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) della classe [**\_ VirtualSystemReferencePointService di MSVM**](msvm-virtualsystemreferencepointservice.md) .

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointExportSettingData : CIM_SettingData
{
  String BaseReferencePoint;
  String DisksToExport[];
};
```

## <a name="members"></a>Members

La **classe \_ VirtualSystemReferencePointExportSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ VirtualSystemReferencePointExportSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**BaseReferencePoint**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso del punto di riferimento di base rispetto al quale eseguire l'esportazione.

</dd> <dt>

**DisksToExport**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ID dell'istanza WMI dei dischi per i quali è necessario esportare i dati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

 




