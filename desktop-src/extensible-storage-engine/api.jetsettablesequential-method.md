---
description: 'Altre informazioni su: metodo API. JetSetTableSequential'
title: API. JetSetTableSequential, metodo
TOCTitle: 'JetSetTableSequential method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetTableSequentialGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsettablesequential(v=EXCHG.10)
ms:contentKeyID: 55100810
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetTableSequential
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 879eca53c4867bb41ee0a231bff9adce39aa58a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318825"
---
# <a name="apijetsettablesequential-method"></a><span data-ttu-id="d6ee9-103">API. JetSetTableSequential, metodo</span><span class="sxs-lookup"><span data-stu-id="d6ee9-103">Api.JetSetTableSequential method</span></span>

<span data-ttu-id="d6ee9-104">Notifica al motore di database che l'applicazione sta analizzando l'intero indice su cui è posizionato il cursore.</span><span class="sxs-lookup"><span data-stu-id="d6ee9-104">Notifies the database engine that the application is scanning the entire index that the cursor is positioned on.</span></span> <span data-ttu-id="d6ee9-105">Di conseguenza, i metodi usati per accedere ai dati dell'indice verranno ottimizzati per rendere questo scenario il più rapido possibile.</span><span class="sxs-lookup"><span data-stu-id="d6ee9-105">Consequently, the methods that are used to access the index data will be tuned to make this scenario as fast as possible.</span></span> <span data-ttu-id="d6ee9-106">Vedere anche [JetResetTableSequential (JET_SESID, JET_TABLEID, ResetTableSequentialGrbit)](./api.jetresettablesequential-method.md).</span><span class="sxs-lookup"><span data-stu-id="d6ee9-106">Also see [JetResetTableSequential(JET_SESID, JET_TABLEID, ResetTableSequentialGrbit)](./api.jetresettablesequential-method.md).</span></span>

<span data-ttu-id="d6ee9-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d6ee9-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d6ee9-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d6ee9-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d6ee9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6ee9-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetTableSequential ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetTableSequentialGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetTableSequentialGrbitApi.JetSetTableSequential(sesid, _
    tableid, grbit)
```

``` csharp
public static void JetSetTableSequential(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetTableSequentialGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="d6ee9-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d6ee9-110">Parameters</span></span>

  - <span data-ttu-id="d6ee9-111">sesid</span><span class="sxs-lookup"><span data-stu-id="d6ee9-111">sesid</span></span>  
    <span data-ttu-id="d6ee9-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d6ee9-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d6ee9-113">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="d6ee9-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d6ee9-114">TableID</span><span class="sxs-lookup"><span data-stu-id="d6ee9-114">tableid</span></span>  
    <span data-ttu-id="d6ee9-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d6ee9-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d6ee9-116">Cursore che effettuerà l'accesso ai dati.</span><span class="sxs-lookup"><span data-stu-id="d6ee9-116">The cursor that will be accessing the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="d6ee9-117">grbit</span><span class="sxs-lookup"><span data-stu-id="d6ee9-117">grbit</span></span>  
    <span data-ttu-id="d6ee9-118">Tipo: [Microsoft. ISAM. esent. Interop. SetTableSequentialGrbit](./settablesequentialgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d6ee9-118">Type: [Microsoft.Isam.Esent.Interop.SetTableSequentialGrbit](./settablesequentialgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="d6ee9-119">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="d6ee9-119">Reserved for future use.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6ee9-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6ee9-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d6ee9-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d6ee9-121">Reference</span></span>

[<span data-ttu-id="d6ee9-122">Classe API</span><span class="sxs-lookup"><span data-stu-id="d6ee9-122">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d6ee9-123">Membri API</span><span class="sxs-lookup"><span data-stu-id="d6ee9-123">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d6ee9-124">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d6ee9-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
