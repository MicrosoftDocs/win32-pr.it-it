---
description: 'Altre informazioni su: metodo API. JetSetLS'
title: API. JetSetLS, metodo
TOCTitle: 'JetSetLS method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetLS(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_LS,Microsoft.Isam.Esent.Interop.LsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetls(v=EXCHG.10)
ms:contentKeyID: 55100808
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetLS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetLS
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d11d0790bb1d9340c427fd1b836d927527c6ca63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233242"
---
# <a name="apijetsetls-method"></a><span data-ttu-id="84db5-103">API. JetSetLS, metodo</span><span class="sxs-lookup"><span data-stu-id="84db5-103">Api.JetSetLS method</span></span>

<span data-ttu-id="84db5-104">Consente all'applicazione di associare un handle di contesto noto come archiviazione locale con un cursore o la tabella associata a tale cursore.</span><span class="sxs-lookup"><span data-stu-id="84db5-104">Enables the application to associate a context handle known as Local Storage with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="84db5-105">Questo handle di contesto può essere utilizzato dall'applicazione per archiviare dati ausiliari associati a un cursore o a una tabella.</span><span class="sxs-lookup"><span data-stu-id="84db5-105">This context handle can be used by the application to store auxiliary data that is associated with a cursor or table.</span></span> <span data-ttu-id="84db5-106">In seguito, l'applicazione riceve una notifica tramite un callback di runtime quando è necessario rilasciare l'handle del contesto.</span><span class="sxs-lookup"><span data-stu-id="84db5-106">The application is later notified using a runtime callback when the context handle must be released.</span></span> <span data-ttu-id="84db5-107">Ciò consente di associare lo stato allocato in modo dinamico a un cursore o a una tabella.</span><span class="sxs-lookup"><span data-stu-id="84db5-107">This makes it possible to associate dynamically allocated state with a cursor or table.</span></span>

<span data-ttu-id="84db5-108">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="84db5-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="84db5-109">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="84db5-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="84db5-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84db5-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetLS ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ls As JET_LS, _
    grbit As LsGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim ls As JET_LS
Dim grbit As LsGrbitApi.JetSetLS(sesid, tableid, ls, _
    grbit)
```

``` csharp
public static void JetSetLS(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_LS ls,
    LsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="84db5-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="84db5-111">Parameters</span></span>

  - <span data-ttu-id="84db5-112">sesid</span><span class="sxs-lookup"><span data-stu-id="84db5-112">sesid</span></span>  
    <span data-ttu-id="84db5-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="84db5-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="84db5-114">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="84db5-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="84db5-115">TableID</span><span class="sxs-lookup"><span data-stu-id="84db5-115">tableid</span></span>  
    <span data-ttu-id="84db5-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="84db5-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="84db5-117">Cursore da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="84db5-117">The cursor to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="84db5-118">ls</span><span class="sxs-lookup"><span data-stu-id="84db5-118">ls</span></span>  
    <span data-ttu-id="84db5-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="84db5-119">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="84db5-120">Handle di contesto da associare alla sessione o al cursore.</span><span class="sxs-lookup"><span data-stu-id="84db5-120">The context handle to be associated with the session or cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="84db5-121">grbit</span><span class="sxs-lookup"><span data-stu-id="84db5-121">grbit</span></span>  
    <span data-ttu-id="84db5-122">Tipo: [Microsoft. ISAM. esent. Interop. LsGrbit](./lsgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="84db5-122">Type: [Microsoft.Isam.Esent.Interop.LsGrbit](./lsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="84db5-123">Opzioni set.</span><span class="sxs-lookup"><span data-stu-id="84db5-123">Set options.</span></span>

## <a name="see-also"></a><span data-ttu-id="84db5-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84db5-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="84db5-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="84db5-125">Reference</span></span>

[<span data-ttu-id="84db5-126">Classe API</span><span class="sxs-lookup"><span data-stu-id="84db5-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="84db5-127">Membri API</span><span class="sxs-lookup"><span data-stu-id="84db5-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="84db5-128">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="84db5-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
