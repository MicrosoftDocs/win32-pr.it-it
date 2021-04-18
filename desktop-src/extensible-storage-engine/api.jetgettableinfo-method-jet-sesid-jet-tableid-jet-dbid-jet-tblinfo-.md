---
description: 'Altre informazioni su: metodo API. JetGetTableInfo (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)'
title: Metodo API. JetGetTableInfo (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)
TOCTitle: JetGetTableInfo method (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.JET_TblInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableinfo(v=EXCHG.10)
ms:contentKeyID: 55100736
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e955a1b854162bd8eca4e19506329c2cf6016e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316967"
---
# <a name="apijetgettableinfo-method-jet_sesid-jet_tableid-jet_dbid-jet_tblinfo"></a><span data-ttu-id="ff774-103">Metodo API. JetGetTableInfo (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</span><span class="sxs-lookup"><span data-stu-id="ff774-103">Api.JetGetTableInfo method (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</span></span>

<span data-ttu-id="ff774-104">Recupera varie informazioni su una tabella in un database.</span><span class="sxs-lookup"><span data-stu-id="ff774-104">Retrieves various pieces of information about a table in a database.</span></span>

<span data-ttu-id="ff774-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ff774-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ff774-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ff774-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ff774-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff774-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef result As JET_DBID, _
    infoLevel As JET_TblInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim result As JET_DBID
Dim infoLevel As JET_TblInfoApi.JetGetTableInfo(sesid, tableid, _
    result, infoLevel)
```

``` csharp
public static void JetGetTableInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_DBID result,
    JET_TblInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="ff774-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ff774-108">Parameters</span></span>

  - <span data-ttu-id="ff774-109">sesid</span><span class="sxs-lookup"><span data-stu-id="ff774-109">sesid</span></span>  
    <span data-ttu-id="ff774-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ff774-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ff774-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="ff774-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ff774-112">TableID</span><span class="sxs-lookup"><span data-stu-id="ff774-112">tableid</span></span>  
    <span data-ttu-id="ff774-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ff774-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ff774-114">Tabella per cui recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="ff774-114">The table to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="ff774-115">result</span><span class="sxs-lookup"><span data-stu-id="ff774-115">result</span></span>  
    <span data-ttu-id="ff774-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ff774-116">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="ff774-117">Informazioni recuperate.</span><span class="sxs-lookup"><span data-stu-id="ff774-117">Retrieved information.</span></span>

<!-- end list -->

  - <span data-ttu-id="ff774-118">infoLevel</span><span class="sxs-lookup"><span data-stu-id="ff774-118">infoLevel</span></span>  
    <span data-ttu-id="ff774-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ff774-119">Type: [Microsoft.Isam.Esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="ff774-120">Tipo di informazioni da recuperare.</span><span class="sxs-lookup"><span data-stu-id="ff774-120">The type of information to retrieve.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff774-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff774-121">Remarks</span></span>

<span data-ttu-id="ff774-122">Questo overload viene utilizzato con [dbid](./jet-tblinfo-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="ff774-122">This overload is used with [Dbid](./jet-tblinfo-enumeration.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ff774-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff774-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ff774-124">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ff774-124">Reference</span></span>

[<span data-ttu-id="ff774-125">Classe API</span><span class="sxs-lookup"><span data-stu-id="ff774-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ff774-126">Membri API</span><span class="sxs-lookup"><span data-stu-id="ff774-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ff774-127">Overload JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="ff774-127">JetGetTableInfo overload</span></span>](./api.jetgettableinfo-method.md)

[<span data-ttu-id="ff774-128">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ff774-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
