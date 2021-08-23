---
description: La classe di associazione CIM CollectedMSEs rappresenta i membri dell'oggetto \_ di raggruppamento, una classe CollectionOfMSEs.
ms.assetid: 3dca2094-57f1-447e-809c-f924f88a185a
ms.tgt_platform: multiple
title: CIM_CollectedMSEs classe (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 82ffbf9e3c00a9a0463e1337ee5c5ed6ab188dc5258c622cfa6b41eb717d8589
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959080"
---
# <a name="cim_collectedmses-class-cimwin32-wmi-providers"></a>CIM_CollectedMSEs classe (provider WMI CIMWin32)

La **classe di associazione CIM \_ CollectedMSEs** rappresenta i membri dell'oggetto di raggruppamento, [**una classe CollectionOfMSEs.**](cim-collectionofmses.md)

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class CIM_CollectedMSEs
{
  CM_CollectionOfMSEs      REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a>Members

La **classe CIM \_ CollectedMSEs** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ CollectedMSEs** ha queste proprietà.

<dl> <dt>

**Raccolta**
</dt> <dd> <dl> <dt>

Tipo di dati: **CM \_ CollectionOfMSEs**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento all'oggetto di raggruppamento o "bag" che rappresenta la raccolta.

</dd> <dt>

**Membro**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un membro della raccolta.

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe. Per altre informazioni sulle classi WMI derivate **da CIM \_ CollectedMSEs,** vedere [Classi Win32](win32-provider.md).

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




