---
description: 'Altre informazioni su: metodo API. JetCommitTransaction'
title: API. JetCommitTransaction, metodo
TOCTitle: 'JetCommitTransaction method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.CommitTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcommittransaction(v=EXCHG.10)
ms:contentKeyID: 55100665
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCommitTransaction
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edf0799af53c3da422f92f981f7a28ee7a283d4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305562"
---
# <a name="apijetcommittransaction-method"></a><span data-ttu-id="90c9c-103">API. JetCommitTransaction, metodo</span><span class="sxs-lookup"><span data-stu-id="90c9c-103">Api.JetCommitTransaction method</span></span>

<span data-ttu-id="90c9c-104">Esegue il commit delle modifiche apportate allo stato del database durante il punto di salvataggio corrente e ne esegue la migrazione al punto di salvataggio precedente.</span><span class="sxs-lookup"><span data-stu-id="90c9c-104">Commits the changes made to the state of the database during the current save point and migrates them to the previous save point.</span></span> <span data-ttu-id="90c9c-105">Se viene eseguito il commit del punto di salvataggio più esterno, verrà eseguito il commit delle modifiche apportate durante tale punto di salvataggio nello stato del database e la sessione uscirà dalla transazione.</span><span class="sxs-lookup"><span data-stu-id="90c9c-105">If the outermost save point is committed then the changes made during that save point will be committed to the state of the database and the session will exit the transaction.</span></span>

<span data-ttu-id="90c9c-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="90c9c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="90c9c-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="90c9c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="90c9c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90c9c-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCommitTransaction ( _
    sesid As JET_SESID, _
    grbit As CommitTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As CommitTransactionGrbitApi.JetCommitTransaction(sesid, _
    grbit)
```

``` csharp
public static void JetCommitTransaction(
    JET_SESID sesid,
    CommitTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="90c9c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="90c9c-109">Parameters</span></span>

  - <span data-ttu-id="90c9c-110">sesid</span><span class="sxs-lookup"><span data-stu-id="90c9c-110">sesid</span></span>  
    <span data-ttu-id="90c9c-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="90c9c-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="90c9c-112">Sessione per la quale eseguire il commit della transazione.</span><span class="sxs-lookup"><span data-stu-id="90c9c-112">The session to commit the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="90c9c-113">grbit</span><span class="sxs-lookup"><span data-stu-id="90c9c-113">grbit</span></span>  
    <span data-ttu-id="90c9c-114">Tipo: [Microsoft. ISAM. esent. Interop. CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="90c9c-114">Type: [Microsoft.Isam.Esent.Interop.CommitTransactionGrbit](./committransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="90c9c-115">Opzioni di commit.</span><span class="sxs-lookup"><span data-stu-id="90c9c-115">Commit options.</span></span>

## <a name="see-also"></a><span data-ttu-id="90c9c-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90c9c-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="90c9c-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="90c9c-117">Reference</span></span>

[<span data-ttu-id="90c9c-118">Classe API</span><span class="sxs-lookup"><span data-stu-id="90c9c-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="90c9c-119">Membri API</span><span class="sxs-lookup"><span data-stu-id="90c9c-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="90c9c-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="90c9c-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
