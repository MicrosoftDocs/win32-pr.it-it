---
description: Apre il database shim.
ms.assetid: ece1bd39-20a1-42e6-8e2b-1d38f7223d42
title: Funzione SdbInitDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbInitDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0504b12254658250820cb3ecac3e9e47ee2a6ca242b15600fa69241b597bb0dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666382"
---
# <a name="sdbinitdatabase-function"></a>Funzione SdbInitDatabase

Apre il database shim.

## <a name="syntax"></a>Sintassi


```C++
HSDB WINAPI SdbInitDatabase(
  _In_ DWORD   dwFlags,
  _In_ LPCTSTR pszDatabasePath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro specifica il formato del percorso nel *parametro pszDatabasePath.* Può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                      | Significato                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="HID_DOS_PATHS"></span><span id="hid_dos_paths"></span><dl> <dt>**HID \_ PERCORSI \_ DOS**</dt> <dt>0x00000001</dt> </dl>                             | Percorso di stile MS-DOS.<br/>                                                                       |
| <span id="HID_DATABASE_FULLPATH"></span><span id="hid_database_fullpath"></span><dl> <dt>**HID \_ DATABASE \_ FULLPATH**</dt> <dt>0x00000002</dt> </dl>     | Percorso completo.<br/>                                                                                |
| <span id="HID_NO_DATABASE"></span><span id="hid_no_database"></span><dl> <dt>**HID \_ NO \_ DATABASE**</dt> <dt>0x00000004</dt> </dl>                       | Il *parametro pszDatabasePath* viene ignorato e non viene aperto alcun database.<br/>                       |
| <span id="HID_DATABASE_TYPE_MASK"></span><span id="hid_database_type_mask"></span><dl> <dt>**HID \_ MASCHERA \_ DEL \_ TIPO DI**</dt> DATABASE <dt>0xF00F0000</dt> </dl> | Questo parametro specifica un database predefinito. Il *parametro pszDatabasePath* viene ignorato.<br/> |



 

Se *dwFlags* contiene **HID \_ DATA TYPE \_ \_ MASK,** questo parametro può includere anche uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                               | Significato                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**SDB \_ DATABASE \_ MAIN \_ SHIM**</dt> <dt>0x80030000</dt> </dl>          | Database shim dell'applicazione.<br/>         |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**SDB \_ DATABASE \_ MAIN \_ MSI**</dt> <dt>0x80020000</dt> </dl>             | Database MSI.<br/>                      |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**SDB \_ DRIVER \_ PRINCIPALI \_ DEL**</dt> DATABASE <dt>0x80040000</dt> </dl> | Database dei driver da bloccare.<br/> |



 

</dd> <dt>

*pszDatabasePath* \[ Pollici\]
</dt> <dd>

Percorso del database. Questo parametro può essere **NULL** se il *parametro dwFlags* specifica un database predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un handle per il database aperto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SdbGetAppPatchDir**](sdbgetapppatchdir.md)
</dt> <dt>

[**SdbGetMatchingExe**](sdbgetmatchingexe.md)
</dt> <dt>

[**SdbReleaseMatchingExe**](sdbreleasematchingexe.md)
</dt> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> </dl>

 

 




