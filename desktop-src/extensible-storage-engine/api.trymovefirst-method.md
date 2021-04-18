---
description: 'Altre informazioni su: metodo API. TryMoveFirst'
title: API. TryMoveFirst, metodo
TOCTitle: 'TryMoveFirst method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMoveFirst(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymovefirst(v=EXCHG.10)
ms:contentKeyID: 55100946
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMoveFirst
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMoveFirst
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 624fba29ab6fe653b7af674e32b907ea3934d643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305546"
---
# <a name="apitrymovefirst-method"></a><span data-ttu-id="708c9-103">API. TryMoveFirst, metodo</span><span class="sxs-lookup"><span data-stu-id="708c9-103">Api.TryMoveFirst method</span></span>

<span data-ttu-id="708c9-104">Provare a spostarsi sul primo record della tabella.</span><span class="sxs-lookup"><span data-stu-id="708c9-104">Try to move to the first record in the table.</span></span> <span data-ttu-id="708c9-105">Se la tabella è vuota, viene restituito false, se viene rilevato un errore diverso, viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="708c9-105">If the table is empty this returns false, if a different error is encountered an exception is thrown.</span></span>

<span data-ttu-id="708c9-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="708c9-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="708c9-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="708c9-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="708c9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="708c9-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMoveFirst ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryMoveFirst(sesid, _
    tableid)
```

``` csharp
public static bool TryMoveFirst(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="708c9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="708c9-109">Parameters</span></span>

  - <span data-ttu-id="708c9-110">sesid</span><span class="sxs-lookup"><span data-stu-id="708c9-110">sesid</span></span>  
    <span data-ttu-id="708c9-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="708c9-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="708c9-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="708c9-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="708c9-113">TableID</span><span class="sxs-lookup"><span data-stu-id="708c9-113">tableid</span></span>  
    <span data-ttu-id="708c9-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="708c9-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="708c9-115">Cursore da posizionare.</span><span class="sxs-lookup"><span data-stu-id="708c9-115">The cursor to position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="708c9-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="708c9-116">Return value</span></span>

<span data-ttu-id="708c9-117">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="708c9-117">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="708c9-118">True se lo spostamento ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="708c9-118">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="708c9-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="708c9-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="708c9-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="708c9-120">Reference</span></span>

[<span data-ttu-id="708c9-121">Classe API</span><span class="sxs-lookup"><span data-stu-id="708c9-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="708c9-122">Membri API</span><span class="sxs-lookup"><span data-stu-id="708c9-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="708c9-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="708c9-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
