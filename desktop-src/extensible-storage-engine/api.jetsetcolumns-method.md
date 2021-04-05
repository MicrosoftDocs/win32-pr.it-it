---
description: 'Altre informazioni su: metodo API. JetSetColumns'
title: API. JetSetColumns, metodo
TOCTitle: 'JetSetColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_SETCOLUMN[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumns(v=EXCHG.10)
ms:contentKeyID: 55100800
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 59d1d16a21996937357d0358625772a4b6712019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750754"
---
# <a name="apijetsetcolumns-method"></a><span data-ttu-id="22725-103">API. JetSetColumns, metodo</span><span class="sxs-lookup"><span data-stu-id="22725-103">Api.JetSetColumns method</span></span>

<span data-ttu-id="22725-104">Consente a un'applicazione di impostare più valori di colonna in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="22725-104">Allows an application to set multiple column values in a single operation.</span></span> <span data-ttu-id="22725-105">Una matrice di strutture di [JET_SETCOLUMN](./jet-setcolumn-class.md) viene utilizzata per descrivere il set di valori di colonna da impostare e per descrivere i buffer di input per ogni valore di colonna da impostare.</span><span class="sxs-lookup"><span data-stu-id="22725-105">An array of [JET_SETCOLUMN](./jet-setcolumn-class.md) structures is used to describe the set of column values to be set, and to describe input buffers for each column value to be set.</span></span>

<span data-ttu-id="22725-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="22725-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="22725-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="22725-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="22725-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22725-108">Syntax</span></span>

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Shared Function JetSetColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    setcolumns As JET_SETCOLUMN(), _
    numColumns As Integer _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim setcolumns As JET_SETCOLUMN()
Dim numColumns As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumns(sesid, _
    tableid, setcolumns, numColumns)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public static JET_wrn JetSetColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_SETCOLUMN[] setcolumns,
    int numColumns
)
```

#### <a name="parameters"></a><span data-ttu-id="22725-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="22725-109">Parameters</span></span>

  - <span data-ttu-id="22725-110">sesid</span><span class="sxs-lookup"><span data-stu-id="22725-110">sesid</span></span>  
    <span data-ttu-id="22725-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="22725-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="22725-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="22725-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="22725-113">TableID</span><span class="sxs-lookup"><span data-stu-id="22725-113">tableid</span></span>  
    <span data-ttu-id="22725-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="22725-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="22725-115">Cursore su cui impostare le colonne.</span><span class="sxs-lookup"><span data-stu-id="22725-115">The cursor to set the columns on.</span></span>

<!-- end list -->

  - <span data-ttu-id="22725-116">SetColumns</span><span class="sxs-lookup"><span data-stu-id="22725-116">setcolumns</span></span>  
    <span data-ttu-id="22725-117">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="22725-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="22725-118">Matrice di [JET_SETCOLUMN](./jet-setcolumn-class.md) strutture che descrivono i dati da impostare.</span><span class="sxs-lookup"><span data-stu-id="22725-118">An array of [JET_SETCOLUMN](./jet-setcolumn-class.md) structures describing the data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="22725-119">numColumns</span><span class="sxs-lookup"><span data-stu-id="22725-119">numColumns</span></span>  
    <span data-ttu-id="22725-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="22725-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="22725-121">Numero di voci nel parametro secolumns.</span><span class="sxs-lookup"><span data-stu-id="22725-121">Number of entries in the setcolumns parameter.</span></span>

#### <a name="return-value"></a><span data-ttu-id="22725-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22725-122">Return value</span></span>

<span data-ttu-id="22725-123">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="22725-123">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="22725-124">Avviso.</span><span class="sxs-lookup"><span data-stu-id="22725-124">A warning.</span></span> <span data-ttu-id="22725-125">Se l'ultimo set di colonne presenta un avviso, questo avviso verrà restituito da JetSetColumns stesso.</span><span class="sxs-lookup"><span data-stu-id="22725-125">If the last column set has a warning, then this warning will be returned from JetSetColumns itself.</span></span>  

## <a name="see-also"></a><span data-ttu-id="22725-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22725-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="22725-127">Riferimento</span><span class="sxs-lookup"><span data-stu-id="22725-127">Reference</span></span>

[<span data-ttu-id="22725-128">Classe API</span><span class="sxs-lookup"><span data-stu-id="22725-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="22725-129">Membri API</span><span class="sxs-lookup"><span data-stu-id="22725-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="22725-130">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="22725-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
