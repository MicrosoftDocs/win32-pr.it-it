---
description: 'Altre informazioni su: metodo API. TryMove'
title: API. TryMove, metodo
TOCTitle: 'TryMove method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMove(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_Move,Microsoft.Isam.Esent.Interop.MoveGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymove(v=EXCHG.10)
ms:contentKeyID: 55100883
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMove
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6d4b3aa596bb5e813d87dcc6f278112fe1e4cbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305547"
---
# <a name="apitrymove-method"></a><span data-ttu-id="1ed14-103">API. TryMove, metodo</span><span class="sxs-lookup"><span data-stu-id="1ed14-103">Api.TryMove method</span></span>

<span data-ttu-id="1ed14-104">Provare a spostarsi all'interno di un indice.</span><span class="sxs-lookup"><span data-stu-id="1ed14-104">Try to navigate through an index.</span></span> <span data-ttu-id="1ed14-105">Se la navigazione ha esito positivo, questo metodo restituisce true.</span><span class="sxs-lookup"><span data-stu-id="1ed14-105">If the navigation succeeds this method returns true.</span></span> <span data-ttu-id="1ed14-106">Se non è presente alcun record per passare a questo metodo restituisce false; verrà generata un'eccezione per altri errori.</span><span class="sxs-lookup"><span data-stu-id="1ed14-106">If there is no record to navigate to this method returns false; an exception will be thrown for other errors.</span></span>

<span data-ttu-id="1ed14-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1ed14-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1ed14-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1ed14-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1ed14-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ed14-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMove ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    move As JET_Move, _
    grbit As MoveGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim move As JET_Move
Dim grbit As MoveGrbit
Dim returnValue As Boolean

returnValue = Api.TryMove(sesid, _
    tableid, move, grbit)
```

``` csharp
public static bool TryMove(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_Move move,
    MoveGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1ed14-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ed14-110">Parameters</span></span>

  - <span data-ttu-id="1ed14-111">sesid</span><span class="sxs-lookup"><span data-stu-id="1ed14-111">sesid</span></span>  
    <span data-ttu-id="1ed14-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1ed14-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1ed14-113">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="1ed14-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1ed14-114">TableID</span><span class="sxs-lookup"><span data-stu-id="1ed14-114">tableid</span></span>  
    <span data-ttu-id="1ed14-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1ed14-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1ed14-116">Cursore da posizionare.</span><span class="sxs-lookup"><span data-stu-id="1ed14-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="1ed14-117">spostamento</span><span class="sxs-lookup"><span data-stu-id="1ed14-117">move</span></span>  
    <span data-ttu-id="1ed14-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_Move](./jet-move-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1ed14-118">Type: [Microsoft.Isam.Esent.Interop.JET_Move](./jet-move-enumeration.md)</span></span>  
    
    <span data-ttu-id="1ed14-119">Direzione di spostamento.</span><span class="sxs-lookup"><span data-stu-id="1ed14-119">The direction to move in.</span></span>

<!-- end list -->

  - <span data-ttu-id="1ed14-120">grbit</span><span class="sxs-lookup"><span data-stu-id="1ed14-120">grbit</span></span>  
    <span data-ttu-id="1ed14-121">Tipo: [Microsoft. ISAM. esent. Interop. MoveGrbit](./movegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1ed14-121">Type: [Microsoft.Isam.Esent.Interop.MoveGrbit](./movegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1ed14-122">Opzioni di spostamento.</span><span class="sxs-lookup"><span data-stu-id="1ed14-122">Move options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1ed14-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ed14-123">Return value</span></span>

<span data-ttu-id="1ed14-124">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="1ed14-124">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="1ed14-125">True se lo spostamento ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="1ed14-125">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1ed14-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ed14-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1ed14-127">Riferimento</span><span class="sxs-lookup"><span data-stu-id="1ed14-127">Reference</span></span>

[<span data-ttu-id="1ed14-128">Classe API</span><span class="sxs-lookup"><span data-stu-id="1ed14-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1ed14-129">Membri API</span><span class="sxs-lookup"><span data-stu-id="1ed14-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1ed14-130">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1ed14-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
