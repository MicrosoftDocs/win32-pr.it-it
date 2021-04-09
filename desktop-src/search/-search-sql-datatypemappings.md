---
description: Nella tabella seguente sono elencati i mapping tra i tipi di dati Variant e i tipi di dati OLE DB.
ms.assetid: 213458bf-b847-4ced-8a92-686b4eee6d07
title: Mapping dei tipi di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9beae5a9ce1fbaafadfae54979d63c97310f57db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128551"
---
# <a name="data-type-mappings"></a>Mapping dei tipi di dati

Nella tabella seguente sono elencati i mapping tra i tipi di dati Variant e i tipi di dati OLE DB.




| Tipo di dati Variant | Tipo di dati OLE DB |
|-------------------|------------------|
| \_bool VT          | DBTYPE \_ bool     |
| \_BSTR VT          | \_BSTR (BSTR)     |
| \_ByRef VT         | DBTYPE ( \_ ByRef)    |
| \_CY VT            | DBTYPE ( \_ CY)       |
| \_Data VT          | \_Data DbType     |
| \_decimale VT       | \_decimale DbType  |
| VT \_ vuoto         | DBTYPE \_ vuoto    |
| FILETIME VT \_      | sqltime DBTYPE \_ |
| \_GUID VT          | \_GUID DbType     |
| VT \_ I1            | DBTYPE \_ I1       |
| \_I2 VT            | DBTYPE \_ I2       |
| VT \_ I4            | DBTYPE \_ I4       |
| \_I8 VT            | DBTYPE \_ i8       |
| VT \_ null          | DBTYPE \_ null     |
| \_R4 VT            | DBTYPE \_ R4       |
| VT \_ R8            | DBTYPE \_ UI8      |
| \_vettore VT        | \_vettore DbType   |
| \_WSTR VT          | DBTYPE \_ WSTR     |



 

Nella tabella seguente sono elencati i mapping tra i tipi di dati XML e i tipi di dati OLE DB.



| Tipo di dati Variant | Tipo di dati OLE DB |
|-------------------|------------------|
| BIN. BASE64        | \_byte DbType    |
| BIN. ESADECIMALE           | DBTYPE \_ i8       |
| BOOLEAN           | DBTYPE \_ bool     |
| CHAR              | DBTYPE \_ Str      |
| DATE              | \_Data DbType     |
| DATETIME          | \_Data DbType     |
| DateTime. TZ       | \_Data DbType     |
| CORRETTO. 14.4        | DBTYPE \_ R4       |
| FLOAT             | DBTYPE \_ R8       |
| I1                | DBTYPE \_ I1       |
| I2                | DBTYPE \_ I2       |
| I4                | DBTYPE \_ I4       |
| I8                | DBTYPE \_ i8       |
| INT               | DBTYPE \_ i8       |
| LONG              | DBTYPE \_ I4       |
| NUMBER            | DBTYPE \_ R8       |
| R4                | DBTYPE \_ R4       |
| R8                | DBTYPE \_ R8       |
| STRING            | DBTYPE \_ WSTR     |
| TIME              | sqltime DBTYPE \_ |
| Tempo. TZ           | sqltime DBTYPE \_ |
| UI1               | DBTYPE \_ UI2      |
| UI2               | DBTYPE \_ UI2      |
| UI4               | DBTYPE \_ UI4      |
| UI8               | DBTYPE \_ UI8      |
| URI               | DBTYPE \_ WSTR     |
| UUID              | \_GUID DbType     |



 

È possibile eseguire il cast dei dati stringa ad altri tipi di dati. Per ulteriori informazioni, fare riferimento a [cast del tipo di dati di una colonna](-search-sql-castingdatacolumntype.md).

 

 



