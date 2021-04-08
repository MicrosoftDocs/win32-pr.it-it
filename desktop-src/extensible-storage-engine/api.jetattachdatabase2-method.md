---
description: 'Altre informazioni su: metodo API. JetAttachDatabase2'
title: API. JetAttachDatabase2, metodo
TOCTitle: 'JetAttachDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetattachdatabase2(v=EXCHG.10)
ms:contentKeyID: 55107224
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 33d91f0746b3ebf178bd61de58919ab99d85b1f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750770"
---
# <a name="apijetattachdatabase2-method"></a><span data-ttu-id="d2ffc-103">API. JetAttachDatabase2, metodo</span><span class="sxs-lookup"><span data-stu-id="d2ffc-103">Api.JetAttachDatabase2 method</span></span>

<span data-ttu-id="d2ffc-104">Associa un file di database per l'utilizzo con un'istanza di database.</span><span class="sxs-lookup"><span data-stu-id="d2ffc-104">Attaches a database file for use with a database instance.</span></span> <span data-ttu-id="d2ffc-105">Per utilizzare il database, sarà necessario aprirlo successivamente con [JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="d2ffc-105">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span></span>

<span data-ttu-id="d2ffc-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d2ffc-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d2ffc-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d2ffc-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d2ffc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2ffc-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetAttachDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    maxPages As Integer, _
    grbit As AttachDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim maxPages As Integer
Dim grbit As AttachDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetAttachDatabase2(sesid, _
    database, maxPages, grbit)
```

``` csharp
public static JET_wrn JetAttachDatabase2(
    JET_SESID sesid,
    string database,
    int maxPages,
    AttachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="d2ffc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2ffc-109">Parameters</span></span>

  - <span data-ttu-id="d2ffc-110">sesid</span><span class="sxs-lookup"><span data-stu-id="d2ffc-110">sesid</span></span>  
    <span data-ttu-id="d2ffc-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d2ffc-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d2ffc-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="d2ffc-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d2ffc-113">database</span><span class="sxs-lookup"><span data-stu-id="d2ffc-113">database</span></span>  
    <span data-ttu-id="d2ffc-114">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d2ffc-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d2ffc-115">Database da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="d2ffc-115">The database to attach.</span></span>

<!-- end list -->

  - <span data-ttu-id="d2ffc-116">maxPages</span><span class="sxs-lookup"><span data-stu-id="d2ffc-116">maxPages</span></span>  
    <span data-ttu-id="d2ffc-117">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d2ffc-117">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d2ffc-118">Dimensione massima, in pagine del database, del database.</span><span class="sxs-lookup"><span data-stu-id="d2ffc-118">The maximum size, in database pages, of the database.</span></span> <span data-ttu-id="d2ffc-119">Se il valore è 0, non viene applicato alcun valore massimo imposto.</span><span class="sxs-lookup"><span data-stu-id="d2ffc-119">Passing 0 means there is no enforced maximum.</span></span>

<!-- end list -->

  - <span data-ttu-id="d2ffc-120">grbit</span><span class="sxs-lookup"><span data-stu-id="d2ffc-120">grbit</span></span>  
    <span data-ttu-id="d2ffc-121">Tipo: [Microsoft. ISAM. esent. Interop. AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d2ffc-121">Type: [Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="d2ffc-122">Opzioni di connessione.</span><span class="sxs-lookup"><span data-stu-id="d2ffc-122">Attach options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d2ffc-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2ffc-123">Return value</span></span>

<span data-ttu-id="d2ffc-124">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d2ffc-124">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="d2ffc-125">Codice di avviso ESENT.</span><span class="sxs-lookup"><span data-stu-id="d2ffc-125">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d2ffc-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2ffc-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d2ffc-127">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d2ffc-127">Reference</span></span>

[<span data-ttu-id="d2ffc-128">Classe API</span><span class="sxs-lookup"><span data-stu-id="d2ffc-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d2ffc-129">Membri API</span><span class="sxs-lookup"><span data-stu-id="d2ffc-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d2ffc-130">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d2ffc-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
