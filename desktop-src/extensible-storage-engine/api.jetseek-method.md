---
description: 'Altre informazioni su: metodo API. JetSeek'
title: API. JetSeek, metodo
TOCTitle: 'JetSeek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSeek(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SeekGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetseek(v=EXCHG.10)
ms:contentKeyID: 55100796
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSeek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSeek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85c8c61bd4e56b342b33d26f22ae3946967640e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968543"
---
# <a name="apijetseek-method"></a><span data-ttu-id="3e6c9-103">API. JetSeek, metodo</span><span class="sxs-lookup"><span data-stu-id="3e6c9-103">Api.JetSeek method</span></span>

<span data-ttu-id="3e6c9-104">Posiziona in modo efficiente un cursore in una voce di indice che corrisponde ai criteri di ricerca specificati dalla chiave di ricerca in tale cursore e alla disuguaglianza specificata.</span><span class="sxs-lookup"><span data-stu-id="3e6c9-104">Efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="3e6c9-105">È necessario che una chiave di ricerca sia stata costruita in precedenza utilizzando [JetMakeKey (JET_SESID, JET_TABLEID, \[ \] , Int32, MakeKeyGrbit)](./api.jetmakekey-method.md).</span><span class="sxs-lookup"><span data-stu-id="3e6c9-105">A search key must have been previously constructed using [JetMakeKey(JET_SESID, JET_TABLEID, \[\], Int32, MakeKeyGrbit)](./api.jetmakekey-method.md).</span></span> <span data-ttu-id="3e6c9-106">Vedere anche [TrySeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.tryseek-method.md).</span><span class="sxs-lookup"><span data-stu-id="3e6c9-106">Also see [TrySeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.tryseek-method.md).</span></span>

<span data-ttu-id="3e6c9-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3e6c9-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3e6c9-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3e6c9-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3e6c9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e6c9-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSeek ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SeekGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SeekGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetSeek(sesid, _
    tableid, grbit)
```

``` csharp
public static JET_wrn JetSeek(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SeekGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="3e6c9-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e6c9-110">Parameters</span></span>

  - <span data-ttu-id="3e6c9-111">sesid</span><span class="sxs-lookup"><span data-stu-id="3e6c9-111">sesid</span></span>  
    <span data-ttu-id="3e6c9-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3e6c9-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3e6c9-113">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="3e6c9-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3e6c9-114">TableID</span><span class="sxs-lookup"><span data-stu-id="3e6c9-114">tableid</span></span>  
    <span data-ttu-id="3e6c9-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3e6c9-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="3e6c9-116">Cursore da posizionare.</span><span class="sxs-lookup"><span data-stu-id="3e6c9-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="3e6c9-117">grbit</span><span class="sxs-lookup"><span data-stu-id="3e6c9-117">grbit</span></span>  
    <span data-ttu-id="3e6c9-118">Tipo: [Microsoft. ISAM. esent. Interop. SeekGrbit](./seekgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3e6c9-118">Type: [Microsoft.Isam.Esent.Interop.SeekGrbit](./seekgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="3e6c9-119">Opzioni di ricerca.</span><span class="sxs-lookup"><span data-stu-id="3e6c9-119">Seek options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="3e6c9-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e6c9-120">Return value</span></span>

<span data-ttu-id="3e6c9-121">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3e6c9-121">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="3e6c9-122">Avviso ESENT.</span><span class="sxs-lookup"><span data-stu-id="3e6c9-122">An ESENT warning.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3e6c9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e6c9-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3e6c9-124">Riferimento</span><span class="sxs-lookup"><span data-stu-id="3e6c9-124">Reference</span></span>

[<span data-ttu-id="3e6c9-125">Classe API</span><span class="sxs-lookup"><span data-stu-id="3e6c9-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3e6c9-126">Membri API</span><span class="sxs-lookup"><span data-stu-id="3e6c9-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3e6c9-127">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3e6c9-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
