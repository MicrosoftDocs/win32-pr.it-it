---
description: 'Altre informazioni su: Proprietà JET_INSTANCE_INFO. szDatabaseFileName'
title: Proprietà JET_INSTANCE_INFO. szDatabaseFileName
TOCTitle: 'szDatabaseFileName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.szdatabasefilename(v=EXCHG.10)
ms:contentKeyID: 55103711
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.get_szDatabaseFileName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55414184fd25a90f3fbb57be8fb5d84264fde5dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318123"
---
# <a name="jet_instance_infoszdatabasefilename-property"></a><span data-ttu-id="f305b-103">Proprietà JET_INSTANCE_INFO. szDatabaseFileName</span><span class="sxs-lookup"><span data-stu-id="f305b-103">JET_INSTANCE_INFO.szDatabaseFileName property</span></span>

<span data-ttu-id="f305b-104">Ottiene una raccolta di stringhe, ognuna delle quali contiene il nome file di un database associato all'istanza del database.</span><span class="sxs-lookup"><span data-stu-id="f305b-104">Gets a collection of strings, each holding the file name of a database that is attached to the database instance.</span></span> <span data-ttu-id="f305b-105">La matrice contiene elementi cDatabases.</span><span class="sxs-lookup"><span data-stu-id="f305b-105">The array has cDatabases elements.</span></span>

<span data-ttu-id="f305b-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f305b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f305b-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f305b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f305b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f305b-108">Syntax</span></span>

``` vb
'Declaration
Public ReadOnly Property szDatabaseFileName As IList(Of String)
    Get
'Usage
Dim instance As JET_INSTANCE_INFO
Dim value As IList(Of String)

value = instance.szDatabaseFileName
```

``` csharp
public IList<string> szDatabaseFileName { get; }
```

#### <a name="property-value"></a><span data-ttu-id="f305b-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f305b-109">Property value</span></span>

<span data-ttu-id="f305b-110">Tipo: [System. Collections. Generic. IList](/dotnet/api/system.collections.generic.ilist-1)\<[String](/dotnet/api/system.string)\></span><span class="sxs-lookup"><span data-stu-id="f305b-110">Type: [System.Collections.Generic.IList](/dotnet/api/system.collections.generic.ilist-1)\<[String](/dotnet/api/system.string)\></span></span>  

## <a name="see-also"></a><span data-ttu-id="f305b-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f305b-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f305b-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f305b-112">Reference</span></span>

[<span data-ttu-id="f305b-113">Classe JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="f305b-113">JET_INSTANCE_INFO class</span></span>](./jet-instance-info-class.md)

[<span data-ttu-id="f305b-114">Membri JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="f305b-114">JET_INSTANCE_INFO members</span></span>](./jet-instance-info-members.md)

[<span data-ttu-id="f305b-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f305b-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
