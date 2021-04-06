---
description: 'Altre informazioni su: struttura JET_DBID'
title: Struttura JET_DBID
TOCTitle: JET_DBID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DBID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid(v=EXCHG.10)
ms:contentKeyID: 39515255
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e92373015b64593936ee8d447b619932d168157c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882517"
---
# <a name="jet_dbid-structure"></a><span data-ttu-id="b7566-103">Struttura JET_DBID</span><span class="sxs-lookup"><span data-stu-id="b7566-103">JET_DBID structure</span></span>

<span data-ttu-id="b7566-104">Un JET_DBID contiene l'handle per il database.</span><span class="sxs-lookup"><span data-stu-id="b7566-104">A JET_DBID contains the handle to the database.</span></span> <span data-ttu-id="b7566-105">Per gestire lo schema di un database viene utilizzato un handle di database.</span><span class="sxs-lookup"><span data-stu-id="b7566-105">A database handle is used to manage the schema of a database.</span></span> <span data-ttu-id="b7566-106">Può inoltre essere utilizzato per gestire le tabelle all'interno di tale database.</span><span class="sxs-lookup"><span data-stu-id="b7566-106">It can also be used to manage the tables inside of that database.</span></span>

<span data-ttu-id="b7566-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b7566-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b7566-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b7566-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b7566-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7566-109">Syntax</span></span>

``` vb
'Declaration
Public Structure JET_DBID _
    Implements IEquatable(Of JET_DBID), IFormattable
'Usage
Dim instance As JET_DBID
```

``` csharp
public struct JET_DBID : IEquatable<JET_DBID>, 
    IFormattable
```

## <a name="thread-safety"></a><span data-ttu-id="b7566-110">Thread safety</span><span class="sxs-lookup"><span data-stu-id="b7566-110">Thread safety</span></span>

<span data-ttu-id="b7566-111">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="b7566-111">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b7566-112">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="b7566-112">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b7566-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7566-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b7566-114">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b7566-114">Reference</span></span>

[<span data-ttu-id="b7566-115">Membri JET_DBID</span><span class="sxs-lookup"><span data-stu-id="b7566-115">JET_DBID members</span></span>](./jet-dbid-members.md)

[<span data-ttu-id="b7566-116">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b7566-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
