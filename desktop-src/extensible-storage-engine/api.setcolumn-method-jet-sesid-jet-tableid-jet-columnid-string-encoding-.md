---
description: 'Altre informazioni su: metodo API. secolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding)'
title: Metodo API. secolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.String,System.Text.Encoding)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100935
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7237bd6ba02e15ade70ee03330332242977822d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314089"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-string-encoding"></a><span data-ttu-id="7e5a6-103">Metodo API. secolumn (JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding)</span><span class="sxs-lookup"><span data-stu-id="7e5a6-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding)</span></span>

<span data-ttu-id="7e5a6-104">Modifica il valore di una singola colonna in un record modificato da inserire o per aggiornare il record corrente.</span><span class="sxs-lookup"><span data-stu-id="7e5a6-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="7e5a6-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7e5a6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7e5a6-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7e5a6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7e5a6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e5a6-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As String, _
    encoding As Encoding _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As String
Dim encoding As EncodingApi.SetColumn(sesid, tableid, columnid, _
    data, encoding)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    string data,
    Encoding encoding
)
```

#### <a name="parameters"></a><span data-ttu-id="7e5a6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7e5a6-108">Parameters</span></span>

  - <span data-ttu-id="7e5a6-109">sesid</span><span class="sxs-lookup"><span data-stu-id="7e5a6-109">sesid</span></span>  
    <span data-ttu-id="7e5a6-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7e5a6-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7e5a6-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="7e5a6-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e5a6-112">TableID</span><span class="sxs-lookup"><span data-stu-id="7e5a6-112">tableid</span></span>  
    <span data-ttu-id="7e5a6-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7e5a6-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="7e5a6-114">Cursore da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="7e5a6-114">The cursor to update.</span></span> <span data-ttu-id="7e5a6-115">È necessario preparare un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="7e5a6-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e5a6-116">columnid</span><span class="sxs-lookup"><span data-stu-id="7e5a6-116">columnid</span></span>  
    <span data-ttu-id="7e5a6-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7e5a6-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="7e5a6-118">ColumnID da impostare.</span><span class="sxs-lookup"><span data-stu-id="7e5a6-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e5a6-119">data</span><span class="sxs-lookup"><span data-stu-id="7e5a6-119">data</span></span>  
    <span data-ttu-id="7e5a6-120">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7e5a6-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="7e5a6-121">Dati da impostare.</span><span class="sxs-lookup"><span data-stu-id="7e5a6-121">The data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e5a6-122">codifica</span><span class="sxs-lookup"><span data-stu-id="7e5a6-122">encoding</span></span>  
    <span data-ttu-id="7e5a6-123">Tipo: [System. Text. Encoding](/dotnet/api/system.text.encoding)</span><span class="sxs-lookup"><span data-stu-id="7e5a6-123">Type: [System.Text.Encoding](/dotnet/api/system.text.encoding)</span></span>  
    
    <span data-ttu-id="7e5a6-124">Codifica utilizzata per convertire la stringa.</span><span class="sxs-lookup"><span data-stu-id="7e5a6-124">The encoding used to convert the string.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e5a6-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e5a6-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7e5a6-126">Riferimento</span><span class="sxs-lookup"><span data-stu-id="7e5a6-126">Reference</span></span>

[<span data-ttu-id="7e5a6-127">Classe API</span><span class="sxs-lookup"><span data-stu-id="7e5a6-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7e5a6-128">Membri API</span><span class="sxs-lookup"><span data-stu-id="7e5a6-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7e5a6-129">Overload di secolumn</span><span class="sxs-lookup"><span data-stu-id="7e5a6-129">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="7e5a6-130">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7e5a6-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
