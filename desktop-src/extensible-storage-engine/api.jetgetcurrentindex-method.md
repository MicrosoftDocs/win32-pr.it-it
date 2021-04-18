---
description: 'Altre informazioni su: metodo API. JetGetCurrentIndex'
title: API. JetGetCurrentIndex, metodo
TOCTitle: 'JetGetCurrentIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcurrentindex(v=EXCHG.10)
ms:contentKeyID: 55100699
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bacc6973b1a105e128533a1116abdeb4c6cfafa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306293"
---
# <a name="apijetgetcurrentindex-method"></a><span data-ttu-id="ac531-103">API. JetGetCurrentIndex, metodo</span><span class="sxs-lookup"><span data-stu-id="ac531-103">Api.JetGetCurrentIndex method</span></span>

<span data-ttu-id="ac531-104">Ddetermines il nome dell'indice corrente di un determinato cursore.</span><span class="sxs-lookup"><span data-stu-id="ac531-104">Ddetermines the name of the current index of a given cursor.</span></span> <span data-ttu-id="ac531-105">Questo nome viene usato anche per riselezionare in seguito l'indice come indice corrente usando [JetSetCurrentIndex (JET_SESID, JET_TABLEID, String)](./api.jetsetcurrentindex-method.md).</span><span class="sxs-lookup"><span data-stu-id="ac531-105">This name is also used to later re-select that index as the current index using [JetSetCurrentIndex(JET_SESID, JET_TABLEID, String)](./api.jetsetcurrentindex-method.md).</span></span> <span data-ttu-id="ac531-106">Può essere usato anche per individuare le proprietà dell'indice usando JetGetTableIndexInfo.</span><span class="sxs-lookup"><span data-stu-id="ac531-106">It can also be used to discover the properties of that index using JetGetTableIndexInfo.</span></span>

<span data-ttu-id="ac531-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ac531-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ac531-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ac531-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ac531-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac531-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetCurrentIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef indexName As String, _
    maxNameLength As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexName As String
Dim maxNameLength As IntegerApi.JetGetCurrentIndex(sesid, tableid, _
    indexName, maxNameLength)
```

``` csharp
public static void JetGetCurrentIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out string indexName,
    int maxNameLength
)
```

#### <a name="parameters"></a><span data-ttu-id="ac531-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac531-110">Parameters</span></span>

  - <span data-ttu-id="ac531-111">sesid</span><span class="sxs-lookup"><span data-stu-id="ac531-111">sesid</span></span>  
    <span data-ttu-id="ac531-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ac531-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ac531-113">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="ac531-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ac531-114">TableID</span><span class="sxs-lookup"><span data-stu-id="ac531-114">tableid</span></span>  
    <span data-ttu-id="ac531-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ac531-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ac531-116">Cursore per il quale ottenere il nome dell'indice.</span><span class="sxs-lookup"><span data-stu-id="ac531-116">The cursor to get the index name for.</span></span>

<!-- end list -->

  - <span data-ttu-id="ac531-117">indexName</span><span class="sxs-lookup"><span data-stu-id="ac531-117">indexName</span></span>  
    <span data-ttu-id="ac531-118">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="ac531-118">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="ac531-119">Restituisce il nome dell'indice.</span><span class="sxs-lookup"><span data-stu-id="ac531-119">Returns the name of the index.</span></span>

<!-- end list -->

  - <span data-ttu-id="ac531-120">maxNameLength</span><span class="sxs-lookup"><span data-stu-id="ac531-120">maxNameLength</span></span>  
    <span data-ttu-id="ac531-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ac531-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="ac531-122">Lunghezza massima del nome dell'indice.</span><span class="sxs-lookup"><span data-stu-id="ac531-122">The maximum length of the index name.</span></span> <span data-ttu-id="ac531-123">I nomi di indice non sono più di [NameMost](./systemparameters.namemost-field.md) caratteri.</span><span class="sxs-lookup"><span data-stu-id="ac531-123">Index names are no more than [NameMost](./systemparameters.namemost-field.md) characters.</span></span>

## <a name="see-also"></a><span data-ttu-id="ac531-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac531-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ac531-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ac531-125">Reference</span></span>

[<span data-ttu-id="ac531-126">Classe API</span><span class="sxs-lookup"><span data-stu-id="ac531-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ac531-127">Membri API</span><span class="sxs-lookup"><span data-stu-id="ac531-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ac531-128">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ac531-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
