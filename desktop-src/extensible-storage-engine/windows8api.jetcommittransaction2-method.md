---
description: 'Altre informazioni su: Windows8Api. JetCommitTransaction2, metodo'
title: Metodo Windows8Api. JetCommitTransaction2 (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetCommitTransaction2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.CommitTransactionGrbit,System.TimeSpan,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetcommittransaction2(v=EXCHG.10)
ms:contentKeyID: 55104454
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCommitTransaction2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80ddc0670b60a3f2a280ff2aca3f051242c453ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308805"
---
# <a name="windows8apijetcommittransaction2-method"></a><span data-ttu-id="b39bf-103">Windows8Api. JetCommitTransaction2, metodo</span><span class="sxs-lookup"><span data-stu-id="b39bf-103">Windows8Api.JetCommitTransaction2 method</span></span>

<span data-ttu-id="b39bf-104">Esegue il commit delle modifiche apportate allo stato del database durante il punto di salvataggio corrente e ne esegue la migrazione al punto di salvataggio precedente.</span><span class="sxs-lookup"><span data-stu-id="b39bf-104">Commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="b39bf-105">Se viene eseguito il commit del punto di salvataggio più esterno, verrà eseguito il commit delle modifiche apportate durante tale punto di salvataggio nello stato del database e la sessione uscirà dalla transazione.</span><span class="sxs-lookup"><span data-stu-id="b39bf-105">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

<span data-ttu-id="b39bf-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b39bf-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="b39bf-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b39bf-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b39bf-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b39bf-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCommitTransaction2 ( _
    sesid As JET_SESID, _
    grbit As CommitTransactionGrbit, _
    durableCommit As TimeSpan, _
    <OutAttribute> ByRef commitId As JET_COMMIT_ID _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As CommitTransactionGrbit
Dim durableCommit As TimeSpan
Dim commitId As JET_COMMIT_IDWindows8Api.JetCommitTransaction2(sesid, _
    grbit, durableCommit, commitId)
```

``` csharp
public static void JetCommitTransaction2(
    JET_SESID sesid,
    CommitTransactionGrbit grbit,
    TimeSpan durableCommit,
    out JET_COMMIT_ID commitId
)
```

#### <a name="parameters"></a><span data-ttu-id="b39bf-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b39bf-109">Parameters</span></span>

  - <span data-ttu-id="b39bf-110">sesid</span><span class="sxs-lookup"><span data-stu-id="b39bf-110">sesid</span></span>  
    <span data-ttu-id="b39bf-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b39bf-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b39bf-112">Sessione per la quale eseguire il commit della transazione.</span><span class="sxs-lookup"><span data-stu-id="b39bf-112">The session to commit the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="b39bf-113">grbit</span><span class="sxs-lookup"><span data-stu-id="b39bf-113">grbit</span></span>  
    <span data-ttu-id="b39bf-114">Tipo: [Microsoft. ISAM. esent. Interop. CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b39bf-114">Type: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b39bf-115">Opzioni di commit.</span><span class="sxs-lookup"><span data-stu-id="b39bf-115">Commit options.</span></span>

<!-- end list -->

  - <span data-ttu-id="b39bf-116">durableCommit</span><span class="sxs-lookup"><span data-stu-id="b39bf-116">durableCommit</span></span>  
    <span data-ttu-id="b39bf-117">Tipo: [System. TimeSpan](/dotnet/api/system.timespan)</span><span class="sxs-lookup"><span data-stu-id="b39bf-117">Type: [System.TimeSpan](/dotnet/api/system.timespan)</span></span>  
    
    <span data-ttu-id="b39bf-118">Durata per eseguire il commit della transazione Lazy.</span><span class="sxs-lookup"><span data-stu-id="b39bf-118">Duration to commit lazy transaction.</span></span>

<!-- end list -->

  - <span data-ttu-id="b39bf-119">commitId</span><span class="sxs-lookup"><span data-stu-id="b39bf-119">commitId</span></span>  
    <span data-ttu-id="b39bf-120">Tipo: [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="b39bf-120">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="b39bf-121">Commit-ID associato al record di commit.</span><span class="sxs-lookup"><span data-stu-id="b39bf-121">Commit-id associated with this commit record.</span></span>

## <a name="see-also"></a><span data-ttu-id="b39bf-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b39bf-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b39bf-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b39bf-123">Reference</span></span>

[<span data-ttu-id="b39bf-124">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="b39bf-124">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="b39bf-125">Membri di Windows8Api</span><span class="sxs-lookup"><span data-stu-id="b39bf-125">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="b39bf-126">Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="b39bf-126">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
