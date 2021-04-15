---
description: 'Altre informazioni su: Windows8Api. JetResizeDatabase, metodo'
title: Metodo Windows8Api. JetResizeDatabase (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetResizeDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetResizeDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetresizedatabase(v=EXCHG.10)
ms:contentKeyID: 55104462
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetResizeDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetResizeDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dcca9a4006f8c8da1758a85d12d716b5ce1bba23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527714"
---
# <a name="windows8apijetresizedatabase-method"></a><span data-ttu-id="b2f7e-103">Windows8Api. JetResizeDatabase, metodo</span><span class="sxs-lookup"><span data-stu-id="b2f7e-103">Windows8Api.JetResizeDatabase method</span></span>

<span data-ttu-id="b2f7e-104">Ridimensiona un database attualmente aperto.</span><span class="sxs-lookup"><span data-stu-id="b2f7e-104">Resizes a currently open database.</span></span>

<span data-ttu-id="b2f7e-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b2f7e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="b2f7e-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b2f7e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b2f7e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2f7e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetResizeDatabase ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    desiredPages As Integer, _
    <OutAttribute> ByRef actualPages As Integer, _
    grbit As ResizeDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim desiredPages As Integer
Dim actualPages As Integer
Dim grbit As ResizeDatabaseGrbitWindows8Api.JetResizeDatabase(sesid, dbid, _
    desiredPages, actualPages, grbit)
```

``` csharp
public static void JetResizeDatabase(
    JET_SESID sesid,
    JET_DBID dbid,
    int desiredPages,
    out int actualPages,
    ResizeDatabaseGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="b2f7e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2f7e-108">Parameters</span></span>

  - <span data-ttu-id="b2f7e-109">sesid</span><span class="sxs-lookup"><span data-stu-id="b2f7e-109">sesid</span></span>  
    <span data-ttu-id="b2f7e-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b2f7e-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b2f7e-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="b2f7e-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2f7e-112">dbid</span><span class="sxs-lookup"><span data-stu-id="b2f7e-112">dbid</span></span>  
    <span data-ttu-id="b2f7e-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b2f7e-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="b2f7e-114">Database da incrementare.</span><span class="sxs-lookup"><span data-stu-id="b2f7e-114">The database to grow.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2f7e-115">desiredPages</span><span class="sxs-lookup"><span data-stu-id="b2f7e-115">desiredPages</span></span>  
    <span data-ttu-id="b2f7e-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b2f7e-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b2f7e-117">Dimensioni desiderate del database, in pagine.</span><span class="sxs-lookup"><span data-stu-id="b2f7e-117">The desired size of the database, in pages.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2f7e-118">actualPages</span><span class="sxs-lookup"><span data-stu-id="b2f7e-118">actualPages</span></span>  
    <span data-ttu-id="b2f7e-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b2f7e-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b2f7e-120">Dimensioni del database, in pagine, dopo la chiamata a.</span><span class="sxs-lookup"><span data-stu-id="b2f7e-120">The size of the database, in pages, after the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="b2f7e-121">grbit</span><span class="sxs-lookup"><span data-stu-id="b2f7e-121">grbit</span></span>  
    <span data-ttu-id="b2f7e-122">Tipo: [Microsoft. ISAM. esent. Interop. Windows8. ResizeDatabaseGrbit](./resizedatabasegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b2f7e-122">Type: [Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit](./resizedatabasegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b2f7e-123">Opzioni di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="b2f7e-123">Resize options.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2f7e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2f7e-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b2f7e-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b2f7e-125">Reference</span></span>

[<span data-ttu-id="b2f7e-126">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="b2f7e-126">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="b2f7e-127">Membri di Windows8Api</span><span class="sxs-lookup"><span data-stu-id="b2f7e-127">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="b2f7e-128">Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="b2f7e-128">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
