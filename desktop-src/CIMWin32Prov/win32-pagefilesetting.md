---
description: Oggetto PageFileSetting Win32 \_&\# 8194; La classe WMI rappresenta le impostazioni di un file di pagina.
ms.assetid: 22190ede-1db6-4d69-ae74-63d10977cc78
ms.tgt_platform: multiple
title: Win32_PageFileSetting classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileSetting
- Win32_PageFileSetting.Caption
- Win32_PageFileSetting.Description
- Win32_PageFileSetting.SettingID
- Win32_PageFileSetting.InitialSize
- Win32_PageFileSetting.MaximumSize
- Win32_PageFileSetting.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b860e5b9677b4d4774e0a3a01fb1cc27b336e7c1a02ebcfc40351f5eda21eb8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020189"
---
# <a name="win32_pagefilesetting-class"></a>Classe PageFileSetting Win32 \_

La classe  [WMI](../wmisdk/retrieving-a-class.md) **\_ Win32 PageFileSetting** rappresenta le impostazioni di un file di paging. Le informazioni contenute negli oggetti di cui è stata creata un'istanza da questa classe specificano i parametri del file di pagina usati quando il file viene creato all'avvio del sistema. Le proprietà in questa classe possono essere modificate e posticipate fino all'avvio. Queste impostazioni sono diverse dallo stato di esecuzione di un file di paging espresso tramite la classe [**associata Win32 \_ PageFileUsage**](win32-pagefileusage.md).

Per creare un'istanza di questa classe, abilitare il **privilegio SeCreatePagefilePrivilege.** Per altre informazioni, vedere [**Costanti dei privilegi**](../wmisdk/privilege-constants.md) ed Esecuzione di operazioni con [privilegi](../wmisdk/executing-privileged-operations.md).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{514A9270-C856-11D2-B364-00105A1f77A1}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFileSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 InitialSize;
  uint32 MaximumSize;
  string Name;
};
```

## <a name="members"></a>Members

La **classe \_ PageFileSetting Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ PageFileSetting Win32** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> <dt>

**InitialSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control Session Manager Memory \\ \\ \\ \\ Management \| PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")
</dt> </dl>

Dimensioni iniziali del file di pagina.

Esempio: 139

</dd> <dt>

**MaximumSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control Session Manager Memory \\ \\ \\ \\ Management \| PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")
</dt> </dl>

Dimensioni massime del file di pagina.

Esempio: 178

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Percorso e nome del file di pagina.

Esempio: "C: \\PAGEFILE.SYS"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificatore con cui è noto l'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ PageFileSetting Win32** deriva dall'impostazione [**CIM \_**](cim-setting.md).

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

[**Impostazione \_ CIM**](cim-setting.md)
</dt> <dt>

[Classi del sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
