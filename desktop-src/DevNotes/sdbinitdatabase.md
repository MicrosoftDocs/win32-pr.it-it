---
description: Apre il database di shim.
ms.assetid: ece1bd39-20a1-42e6-8e2b-1d38f7223d42
title: SdbInitDatabase (funzione)
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
ms.openlocfilehash: 7a3c63fa712aec988dbf13c4fb7f9fddbf159fdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482893"
---
# <a name="sdbinitdatabase-function"></a>SdbInitDatabase (funzione)

Apre il database di shim.

## <a name="syntax"></a>Sintassi


```C++
HSDB WINAPI SdbInitDatabase(
  _In_ DWORD   dwFlags,
  _In_ LPCTSTR pszDatabasePath
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro specifica il formato del percorso nel parametro *pszDatabasePath* . Può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                      | Significato                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="HID_DOS_PATHS"></span><span id="hid_dos_paths"></span><dl> <dt>**Nascosto \_ \_Percorsi DOS**</dt> <dt>0x00000001</dt> </dl>                             | Un percorso di stile MS-DOS.<br/>                                                                       |
| <span id="HID_DATABASE_FULLPATH"></span><span id="hid_database_fullpath"></span><dl> <dt>**Nascosto \_ DATABASE \_ FullPath**</dt> <dt>0x00000002</dt> </dl>     | Percorso completo.<br/>                                                                                |
| <span id="HID_NO_DATABASE"></span><span id="hid_no_database"></span><dl> <dt>**Nascosto \_ Nessun \_ database**</dt> <dt>0x00000004</dt> </dl>                       | Il parametro *pszDatabasePath* viene ignorato e non viene aperto alcun database.<br/>                       |
| <span id="HID_DATABASE_TYPE_MASK"></span><span id="hid_database_type_mask"></span><dl> <dt>**Nascosto \_ \_ \_ Maschera del tipo di database**</dt> <dt>0xF00F0000</dt> </dl> | Questo parametro specifica un database predefinito. Il parametro *pszDatabasePath* viene ignorato.<br/> |



 

Se *dwFlags* contiene **il \_ tipo di dati HID \_ \_ mask**, questo parametro può includere anche uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                               | Significato                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <dt>**Sdb \_ 0x80030000 \_ \_ shim principale database**</dt> <dt></dt> </dl>          | Database shim applicazione.<br/>         |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <dt>**Sdb \_ 0x80020000 \_ \_ MSI principale del database**</dt> <dt></dt> </dl>             | Database MSI.<br/>                      |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <dt>**Sdb \_ \_ \_ Driver principali del database**</dt> <dt>0x80040000</dt> </dl> | Database di driver da bloccare.<br/> |



 

</dd> <dt>

*pszDatabasePath* \[ in\]
</dt> <dd>

Percorso del database. Questo parametro può essere **null** se il parametro *dwFlags* specifica un database predefinito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La funzione restituisce un handle per il database aperto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
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

 

 




