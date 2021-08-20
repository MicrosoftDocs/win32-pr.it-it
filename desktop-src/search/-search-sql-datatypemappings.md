---
description: Nella tabella seguente sono elencati i mapping tra i tipi di dati variant e OLE DB tipi di dati.
ms.assetid: 213458bf-b847-4ced-8a92-686b4eee6d07
title: Mapping dei tipi di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e25e909755c87b15526b97488285a0cf688e15dab64073fad603efc190f382b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462595"
---
# <a name="data-type-mappings"></a>Mapping dei tipi di dati

Nella tabella seguente sono elencati i mapping tra i tipi di dati variant e OLE DB tipi di dati.




| Tipo di dati Variant | Tipo di dati OLE DB |
|-------------------|------------------|
| VT \_ BOOL          | DBTYPE \_ BOOL     |
| VT \_ BSTR          | DBTYPE \_ BSTR     |
| VT \_ BYREF         | DBTYPE \_ BYREF    |
| VT \_ CY            | DBTYPE \_ CY       |
| DATA \_ VT          | DATA \_ DBTYPE     |
| VT \_ DECIMAL       | DBTYPE \_ DECIMAL  |
| VT \_ EMPTY         | DBTYPE \_ EMPTY    |
| VT \_ FILETIME      | DBTYPE \_ FILETIME |
| VT \_ GUID          | DBTYPE \_ GUID     |
| VT \_ I1            | DBTYPE \_ I1       |
| VT \_ I2            | DBTYPE \_ I2       |
| VT \_ I4            | DBTYPE \_ I4       |
| VT \_ I8            | DBTYPE \_ I8       |
| VT \_ NULL          | DBTYPE \_ NULL     |
| VT \_ R4            | DBTYPE \_ R4       |
| VT \_ R8            | DBTYPE \_ UI8      |
| VETTORE \_ VT        | VETTORE \_ DBTYPE   |
| VT \_ WSTR          | DBTYPE \_ WSTR     |



 

Nella tabella seguente sono elencati i mapping tra i tipi di dati XML e OLE DB tipi di dati.



| Tipo di dati Variant | Tipo di dati OLE DB |
|-------------------|------------------|
| Bin. BASE64        | BYTE \_ DBTYPE    |
| Bin. Hex           | DBTYPE \_ I8       |
| BOOLEAN           | DBTYPE \_ BOOL     |
| CHAR              | DBTYPE \_ STR      |
| DATE              | DATA \_ DBTYPE     |
| DATETIME          | DATA \_ DBTYPE     |
| Datetime. Tz       | DATA \_ DBTYPE     |
| FIXED.14.4        | DBTYPE \_ R4       |
| FLOAT             | DBTYPE \_ R8       |
| I1                | DBTYPE \_ I1       |
| I2                | DBTYPE \_ I2       |
| I4                | DBTYPE \_ I4       |
| I8                | DBTYPE \_ I8       |
| INT               | DBTYPE \_ I8       |
| LONG              | DBTYPE \_ I4       |
| NUMBER            | DBTYPE \_ R8       |
| R4                | DBTYPE \_ R4       |
| R8                | DBTYPE \_ R8       |
| STRING            | DBTYPE \_ WSTR     |
| TIME              | DBTYPE \_ FILETIME |
| Tempo. Tz           | DBTYPE \_ FILETIME |
| Interfaccia utente1               | DBTYPE \_ UI2      |
| Interfaccia utente2               | DBTYPE \_ UI2      |
| Interfaccia utente4               | DBTYPE \_ UI4      |
| Interfaccia utente8               | DBTYPE \_ UI8      |
| URI               | DBTYPE \_ WSTR     |
| UUID              | DBTYPE \_ GUID     |



 

È possibile eseguire il cast dei dati stringa ad altri tipi di dati. Per altre informazioni, vedere Cast [del tipo di dati di una colonna.](-search-sql-castingdatacolumntype.md)

 

 



