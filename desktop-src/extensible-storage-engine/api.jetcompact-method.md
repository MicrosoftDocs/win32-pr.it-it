---
description: 'Altre informazioni su: metodo API. JetCompact'
title: API. JetCompact, metodo
TOCTitle: 'JetCompact method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCompact(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS,Microsoft.Isam.Esent.Interop.JET_CONVERT,Microsoft.Isam.Esent.Interop.CompactGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcompact(v=EXCHG.10)
ms:contentKeyID: 55100666
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74d714a1b0fa8d53743945afb3a35cc2015df293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966562"
---
# <a name="apijetcompact-method"></a><span data-ttu-id="3a04b-103">API. JetCompact, metodo</span><span class="sxs-lookup"><span data-stu-id="3a04b-103">Api.JetCompact method</span></span>

<span data-ttu-id="3a04b-104">Crea una copia di un database esistente.</span><span class="sxs-lookup"><span data-stu-id="3a04b-104">Makes a copy of an existing database.</span></span> <span data-ttu-id="3a04b-105">La copia viene compattata in uno stato ottimale per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="3a04b-105">The copy is compacted to a state optimal for usage.</span></span> <span data-ttu-id="3a04b-106">I dati nei dati copiati verranno compressi in base alle misure scelte per gli indici in fase di creazione dell'indice.</span><span class="sxs-lookup"><span data-stu-id="3a04b-106">Data in the copied data will be packed according to the measures chosen for the indexes at index create.</span></span> <span data-ttu-id="3a04b-107">In questo modo, i dati compressi possono essere archiviati nel modo più denso possibile.</span><span class="sxs-lookup"><span data-stu-id="3a04b-107">In this way, compacted data may be stored as densely as possible.</span></span> <span data-ttu-id="3a04b-108">In alternativa, i dati compressi possono riservare spazio per gli inserimenti di indici o di crescita successivi.</span><span class="sxs-lookup"><span data-stu-id="3a04b-108">Alternatively, compacted data may reserve space for subsequent record growth or index insertions.</span></span>

<span data-ttu-id="3a04b-109">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3a04b-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3a04b-110">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3a04b-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3a04b-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a04b-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCompact ( _
    sesid As JET_SESID, _
    sourceDatabase As String, _
    destinationDatabase As String, _
    statusCallback As JET_PFNSTATUS, _
    ignored As JET_CONVERT, _
    grbit As CompactGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim sourceDatabase As String
Dim destinationDatabase As String
Dim statusCallback As JET_PFNSTATUS
Dim ignored As JET_CONVERT
Dim grbit As CompactGrbitApi.JetCompact(sesid, sourceDatabase, _
    destinationDatabase, statusCallback, _
    ignored, grbit)
```

``` csharp
public static void JetCompact(
    JET_SESID sesid,
    string sourceDatabase,
    string destinationDatabase,
    JET_PFNSTATUS statusCallback,
    JET_CONVERT ignored,
    CompactGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="3a04b-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a04b-112">Parameters</span></span>

  - <span data-ttu-id="3a04b-113">sesid</span><span class="sxs-lookup"><span data-stu-id="3a04b-113">sesid</span></span>  
    <span data-ttu-id="3a04b-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3a04b-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3a04b-115">Sessione da utilizzare per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="3a04b-115">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="3a04b-116">sourceDatabase</span><span class="sxs-lookup"><span data-stu-id="3a04b-116">sourceDatabase</span></span>  
    <span data-ttu-id="3a04b-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="3a04b-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="3a04b-118">Database di origine che verrà compattato.</span><span class="sxs-lookup"><span data-stu-id="3a04b-118">The source database that will be compacted.</span></span>

<!-- end list -->

  - <span data-ttu-id="3a04b-119">destinationDatabase</span><span class="sxs-lookup"><span data-stu-id="3a04b-119">destinationDatabase</span></span>  
    <span data-ttu-id="3a04b-120">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="3a04b-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="3a04b-121">Nome da utilizzare per il database compresso.</span><span class="sxs-lookup"><span data-stu-id="3a04b-121">The name to use for the compacted database.</span></span>

<!-- end list -->

  - <span data-ttu-id="3a04b-122">statusCallback</span><span class="sxs-lookup"><span data-stu-id="3a04b-122">statusCallback</span></span>  
    <span data-ttu-id="3a04b-123">Tipo: [Microsoft.ISAM.esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="3a04b-123">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="3a04b-124">Funzione di callback che può essere chiamata periodicamente tramite l'operazione di compattazione del database per segnalare lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="3a04b-124">A callback function that can be called periodically through the database compact operation to report progress.</span></span>

<!-- end list -->

  - <span data-ttu-id="3a04b-125">Ignorato</span><span class="sxs-lookup"><span data-stu-id="3a04b-125">ignored</span></span>  
    <span data-ttu-id="3a04b-126">Tipo: [Microsoft.ISAM.esent.Interop.JET_CONVERT](./jet-convert-class.md)</span><span class="sxs-lookup"><span data-stu-id="3a04b-126">Type: [Microsoft.Isam.Esent.Interop.JET_CONVERT](./jet-convert-class.md)</span></span>  
    
    <span data-ttu-id="3a04b-127">Questo parametro viene ignorato e deve essere null.</span><span class="sxs-lookup"><span data-stu-id="3a04b-127">This parameter is ignored and should be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="3a04b-128">grbit</span><span class="sxs-lookup"><span data-stu-id="3a04b-128">grbit</span></span>  
    <span data-ttu-id="3a04b-129">Tipo: [Microsoft. ISAM. esent. Interop. CompactGrbit](./compactgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3a04b-129">Type: [Microsoft.Isam.Esent.Interop.CompactGrbit](./compactgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="3a04b-130">Opzioni compatte.</span><span class="sxs-lookup"><span data-stu-id="3a04b-130">Compact options.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a04b-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a04b-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3a04b-132">Riferimento</span><span class="sxs-lookup"><span data-stu-id="3a04b-132">Reference</span></span>

[<span data-ttu-id="3a04b-133">Classe API</span><span class="sxs-lookup"><span data-stu-id="3a04b-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3a04b-134">Membri API</span><span class="sxs-lookup"><span data-stu-id="3a04b-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3a04b-135">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3a04b-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
