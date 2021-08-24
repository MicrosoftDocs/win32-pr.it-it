---
description: La classe CIM \_ CollectionSetting rappresenta l'associazione tra un oggetto CIM CollectionOfMSEs e la classe di impostazione \_ definita per loro.
ms.assetid: f09bd656-5fdd-4ab1-8ef9-52d431a5117d
ms.tgt_platform: multiple
title: CIM_CollectionSetting classe
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
ms.openlocfilehash: d3f8e1c57301c3357ff4d28a056cb92bc4572eb29b62b6414a0064113189173a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119700891"
---
# <a name="cim_collectionsetting-class"></a>Classe CIM \_ CollectionSetting

La **classe CIM \_ CollectionSetting** rappresenta l'associazione tra [**un oggetto CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) e la classe di impostazione definita per loro.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class CIM_CollectionSetting
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a>Members

La **classe CIM \_ CollectionSetting** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ CollectionSetting** ha queste proprietà.

<dl> <dt>

**Raccolta**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ CollectionOfMSEs**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento alla [**classe CIM \_ CollectionOfMSEs.**](cim-collectionofmses.md)

</dd> <dt>

**Impostazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **impostazione \_ CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento **all'oggetto Setting** associato alla **proprietà Collection.**

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe. Per altre informazioni sulle classi WMI derivate da **CIM \_ CollectionSetting,** vedere [Classi Win32](win32-provider.md).

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




