---
description: 'Altre informazioni su: metodo API. GetColumnDictionary'
title: API. GetColumnDictionary, metodo
TOCTitle: 'GetColumnDictionary method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.getcolumndictionary(v=EXCHG.10)
ms:contentKeyID: 55100653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ab359c5b8b163ce67f576f35250dd521eb14472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305568"
---
# <a name="apigetcolumndictionary-method"></a><span data-ttu-id="0a0b0-103">API. GetColumnDictionary, metodo</span><span class="sxs-lookup"><span data-stu-id="0a0b0-103">Api.GetColumnDictionary method</span></span>

<span data-ttu-id="0a0b0-104">Crea un dizionario che esegue il mapping dei nomi delle colonne ai rispettivi ID di colonna.</span><span class="sxs-lookup"><span data-stu-id="0a0b0-104">Creates a dictionary which maps column names to their column IDs.</span></span>

<span data-ttu-id="0a0b0-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0a0b0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0a0b0-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0a0b0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0a0b0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a0b0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetColumnDictionary ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IDictionary(Of String, JET_COLUMNID)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IDictionary(Of String, JET_COLUMNID)

returnValue = Api.GetColumnDictionary(sesid, _
    tableid)
```

``` csharp
public static IDictionary<string, JET_COLUMNID> GetColumnDictionary(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="0a0b0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a0b0-108">Parameters</span></span>

  - <span data-ttu-id="0a0b0-109">sesid</span><span class="sxs-lookup"><span data-stu-id="0a0b0-109">sesid</span></span>  
    <span data-ttu-id="0a0b0-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0a0b0-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0a0b0-111">Sesid da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="0a0b0-111">The sesid to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="0a0b0-112">TableID</span><span class="sxs-lookup"><span data-stu-id="0a0b0-112">tableid</span></span>  
    <span data-ttu-id="0a0b0-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0a0b0-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="0a0b0-114">Tabella per cui recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="0a0b0-114">The table to retrieve the information for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0a0b0-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a0b0-115">Return value</span></span>

<span data-ttu-id="0a0b0-116">Tipo: [System. Collections. Generic. IDictionary](/dotnet/api/system.collections.generic.idictionary-2)\<[String](/dotnet/api/system.string), [JET_COLUMNID](./jet-columnid-structure.md)\></span><span class="sxs-lookup"><span data-stu-id="0a0b0-116">Type: [System.Collections.Generic.IDictionary](/dotnet/api/system.collections.generic.idictionary-2)\<[String](/dotnet/api/system.string), [JET_COLUMNID](./jet-columnid-structure.md)\></span></span>  
<span data-ttu-id="0a0b0-117">Dizionario che mappa i nomi di colonna agli ID di colonna.</span><span class="sxs-lookup"><span data-stu-id="0a0b0-117">A dictionary mapping column names to column IDs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0a0b0-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a0b0-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0a0b0-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="0a0b0-119">Reference</span></span>

[<span data-ttu-id="0a0b0-120">Classe API</span><span class="sxs-lookup"><span data-stu-id="0a0b0-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0a0b0-121">Membri API</span><span class="sxs-lookup"><span data-stu-id="0a0b0-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0a0b0-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0a0b0-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
