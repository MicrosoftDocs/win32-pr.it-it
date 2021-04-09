---
description: 'Altre informazioni su: Windows8Api. JetCreateIndex4, metodo'
title: Metodo Windows8Api. JetCreateIndex4 (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetCreateIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_INDEXCREATE[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetcreateindex4(v=EXCHG.10)
ms:contentKeyID: 55104455
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8cc06fa47b8463c6c3b731a7e0e06b7ba13ae687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130374"
---
# <a name="windows8apijetcreateindex4-method"></a><span data-ttu-id="c58f4-103">Windows8Api. JetCreateIndex4, metodo</span><span class="sxs-lookup"><span data-stu-id="c58f4-103">Windows8Api.JetCreateIndex4 method</span></span>

<span data-ttu-id="c58f4-104">Crea indici sui dati in un database ESE.</span><span class="sxs-lookup"><span data-stu-id="c58f4-104">Creates indexes over data in an ESE database.</span></span>

<span data-ttu-id="c58f4-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c58f4-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="c58f4-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c58f4-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c58f4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c58f4-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateIndex4 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexcreates As JET_INDEXCREATE(), _
    numIndexCreates As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexcreates As JET_INDEXCREATE()
Dim numIndexCreates As IntegerWindows8Api.JetCreateIndex4(sesid, tableid, _
    indexcreates, numIndexCreates)
```

``` csharp
public static void JetCreateIndex4(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEXCREATE[] indexcreates,
    int numIndexCreates
)
```

#### <a name="parameters"></a><span data-ttu-id="c58f4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c58f4-108">Parameters</span></span>

  - <span data-ttu-id="c58f4-109">sesid</span><span class="sxs-lookup"><span data-stu-id="c58f4-109">sesid</span></span>  
    <span data-ttu-id="c58f4-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c58f4-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c58f4-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="c58f4-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c58f4-112">TableID</span><span class="sxs-lookup"><span data-stu-id="c58f4-112">tableid</span></span>  
    <span data-ttu-id="c58f4-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c58f4-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c58f4-114">Tabella in cui creare l'indice.</span><span class="sxs-lookup"><span data-stu-id="c58f4-114">The table to create the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="c58f4-115">indexcreates</span><span class="sxs-lookup"><span data-stu-id="c58f4-115">indexcreates</span></span>  
    <span data-ttu-id="c58f4-116">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="c58f4-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="c58f4-117">Matrice di oggetti che descrivono gli indici da creare.</span><span class="sxs-lookup"><span data-stu-id="c58f4-117">Array of objects describing the indexes to be created.</span></span>

<!-- end list -->

  - <span data-ttu-id="c58f4-118">numIndexCreates</span><span class="sxs-lookup"><span data-stu-id="c58f4-118">numIndexCreates</span></span>  
    <span data-ttu-id="c58f4-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c58f4-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c58f4-120">Numero di oggetti Descrizione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="c58f4-120">Number of index description objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="c58f4-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="c58f4-121">Remarks</span></span>

<span data-ttu-id="c58f4-122">Quando si creano più indici, ad esempio con numIndexCreates maggiore di 1, è necessario chiamare questo metodo all'esterno di qualsiasi transazione e con accesso esclusivo alla tabella.</span><span class="sxs-lookup"><span data-stu-id="c58f4-122">When creating multiple indexes (i.e. with numIndexCreates greater than 1) this method MUST be called outside of any transactions and with exclusive access to the table.</span></span> <span data-ttu-id="c58f4-123">Il JET_TABLEID restituito da "API. JetCreateTable" avrà accesso a esclusivo o la tabella può essere aperta per l'accesso esclusivo passando [DenyRead](./opentablegrbit-enumeration.md) a [JetOpenTable (JET_SESID, JET_DBID, String, \[ \] , Int32, OpenTableGrbit, JET_TABLEID)](./api.jetopentable-method.md).</span><span class="sxs-lookup"><span data-stu-id="c58f4-123">The JET_TABLEID returned by "Api.JetCreateTable" will have exlusive access or the table can be opened for exclusive access by passing [DenyRead](./opentablegrbit-enumeration.md) to [JetOpenTable(JET_SESID, JET_DBID, String, \[\], Int32, OpenTableGrbit, JET_TABLEID)](./api.jetopentable-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c58f4-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c58f4-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c58f4-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c58f4-125">Reference</span></span>

[<span data-ttu-id="c58f4-126">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="c58f4-126">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="c58f4-127">Membri di Windows8Api</span><span class="sxs-lookup"><span data-stu-id="c58f4-127">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="c58f4-128">Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="c58f4-128">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
