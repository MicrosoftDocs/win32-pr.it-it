---
description: La classe CIM ElementSetting rappresenta l'associazione tra gli elementi di sistema gestiti e la classe \_ di impostazione definita per essi.
ms.assetid: e9b7c43f-7539-48c3-8679-568fb4b036bb
ms.tgt_platform: multiple
title: CIM_ElementSetting classe (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementSetting
- CIM_ElementSetting.Element
- CIM_ElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 706e1d1c4745586e902c5fe527c7153e77eb88c34201b39bf2da001c365421c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080675"
---
# <a name="cim_elementsetting-class-cimwin32-wmi-providers"></a>CIM_ElementSetting classe (provider WMI CIMWin32)

La **classe CIM \_ ElementSetting** rappresenta l'associazione tra gli elementi di sistema gestiti e la classe di impostazione definita per essi.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Association, UUID("{8502C577-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ElementSetting
{
  CIM_ManagedSystemElement REF Element;
  CIM_Setting              REF Setting;
};
```

## <a name="members"></a>Members

La **classe CIM \_ ElementSetting** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ ElementSetting** ha queste proprietà.

<dl> <dt>

**elemento**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento al ruolo dell'oggetto [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) **dell'associazione CIM \_ ElementSetting.** L'elemento di sistema gestito associato fornisce l'elemento che implementa l'impostazione dell'elemento.

</dd> <dt>

**Impostazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **impostazione \_ CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento al ruolo dell'oggetto [**\_ CIM Setting**](cim-setting.md) dell'associazione **CIM \_ ElementSetting.** L'impostazione associata fornisce l'impostazione che implementa l'impostazione dell'elemento .

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe. Per le classi derivate **da CIM \_ ElementSetting,** vedere [Classi Win32](win32-provider.md).

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




