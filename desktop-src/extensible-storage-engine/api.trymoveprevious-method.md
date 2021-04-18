---
description: 'Altre informazioni su: metodo API. TryMovePrevious'
title: API. TryMovePrevious, metodo
TOCTitle: 'TryMovePrevious method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMovePrevious(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymoveprevious(v=EXCHG.10)
ms:contentKeyID: 55100940
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMovePrevious
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMovePrevious
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe512ac4443f670ac73964a422bd9606d903055a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310935"
---
# <a name="apitrymoveprevious-method"></a><span data-ttu-id="cc5c0-103">API. TryMovePrevious, metodo</span><span class="sxs-lookup"><span data-stu-id="cc5c0-103">Api.TryMovePrevious method</span></span>

<span data-ttu-id="cc5c0-104">Provare a passare al record precedente nella tabella.</span><span class="sxs-lookup"><span data-stu-id="cc5c0-104">Try to move to the previous record in the table.</span></span> <span data-ttu-id="cc5c0-105">Se non è presente un record precedente, viene restituito false, se viene rilevato un errore diverso, viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="cc5c0-105">If there is not a previous record this returns false, if a different error is encountered an exception is thrown.</span></span>

<span data-ttu-id="cc5c0-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cc5c0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cc5c0-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cc5c0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cc5c0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc5c0-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMovePrevious ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryMovePrevious(sesid, _
    tableid)
```

``` csharp
public static bool TryMovePrevious(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="cc5c0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc5c0-109">Parameters</span></span>

  - <span data-ttu-id="cc5c0-110">sesid</span><span class="sxs-lookup"><span data-stu-id="cc5c0-110">sesid</span></span>  
    <span data-ttu-id="cc5c0-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cc5c0-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="cc5c0-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="cc5c0-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="cc5c0-113">TableID</span><span class="sxs-lookup"><span data-stu-id="cc5c0-113">tableid</span></span>  
    <span data-ttu-id="cc5c0-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cc5c0-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="cc5c0-115">Cursore da posizionare.</span><span class="sxs-lookup"><span data-stu-id="cc5c0-115">The cursor to position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="cc5c0-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc5c0-116">Return value</span></span>

<span data-ttu-id="cc5c0-117">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="cc5c0-117">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="cc5c0-118">True se lo spostamento ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="cc5c0-118">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cc5c0-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc5c0-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cc5c0-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="cc5c0-120">Reference</span></span>

[<span data-ttu-id="cc5c0-121">Classe API</span><span class="sxs-lookup"><span data-stu-id="cc5c0-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="cc5c0-122">Membri API</span><span class="sxs-lookup"><span data-stu-id="cc5c0-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="cc5c0-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="cc5c0-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
