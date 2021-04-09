---
description: La \_ classe CIM CollectionSetting rappresenta l'associazione tra un \_ CollectionOfMSEs CIM e la classe di impostazione definita.
ms.assetid: f09bd656-5fdd-4ab1-8ef9-52d431a5117d
ms.tgt_platform: multiple
title: Classe CIM_CollectionSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionSetting
- CIM_CollectionSetting.Collection
- CIM_CollectionSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c290225ee38008f0345b695af794e57f311f2998
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877985"
---
# <a name="cim_collectionsetting-class"></a>CIM \_ CollectionSetting (classe)

La classe **CIM \_ CollectionSetting** rappresenta l'associazione tra un [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) e la classe di impostazione definita.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class CIM_CollectionSetting
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a>Members

La classe **CIM \_ CollectionSetting** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ CollectionSetting** dispone di queste proprietà.

<dl> <dt>

**Raccolta**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ CollectionOfMSEs**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento alla classe [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) .

</dd> <dt>

**Impostazione**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ impostazione CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento all'oggetto **Setting** associato alla proprietà della **raccolta** .

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe. Per ulteriori informazioni sulle classi WMI derivate da **CIM \_ CollectionSetting**, vedere [Win32 Classes](win32-provider.md).

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




