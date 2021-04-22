---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: DWRITE_FACTORY_TYPE (dwrite.h)
description: Specifica il tipo di oggetto factory DirectWrite.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_FACTORY_TYPE
- dwrite/DWRITE_FACTORY_TYPE
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite.h
api_name:
- DWRITE_FACTORY_TYPE
ms.openlocfilehash: 87b0d1c2edcb836afd06d732f242b62441b9bd01
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881810"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a><span data-ttu-id="874fc-103">DWRITE_FACTORY_TYPE enumerazione (dwrite.h)</span><span class="sxs-lookup"><span data-stu-id="874fc-103">DWRITE_FACTORY_TYPE enumeration (dwrite.h)</span></span>

<span data-ttu-id="874fc-104">Specifica il tipo di oggetto factory DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="874fc-104">Specifies the type of DirectWrite factory object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="874fc-105">Questa API è disponibile come parte dell'implementazione DWriteCore di [DirectWrite.](../direct-write-portal.md)</span><span class="sxs-lookup"><span data-stu-id="874fc-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="874fc-106">DWriteCore è un'implementazione di DirectWrite, eseguibile su Windows fino alla versione 8, che offre opportunità per l'uso su più piattaforme.</span><span class="sxs-lookup"><span data-stu-id="874fc-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="874fc-107">Per altre informazioni ed esempi di codice, vedi [Panoramica di DWriteCore.](/windows/win32/DirectWrite/dwrite/dwritecore-overview)</span><span class="sxs-lookup"><span data-stu-id="874fc-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="874fc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="874fc-108">Syntax</span></span>
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_ISOLATED2
} ;
```

## <a name="constants"></a><span data-ttu-id="874fc-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="874fc-109">Constants</span></span>

| <span data-ttu-id="874fc-110">Nome</span><span class="sxs-lookup"><span data-stu-id="874fc-110">Name</span></span> | <span data-ttu-id="874fc-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="874fc-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="874fc-112">DWRITE_FACTORY_TYPE_SHARED</span><span class="sxs-lookup"><span data-stu-id="874fc-112">DWRITE_FACTORY_TYPE_SHARED</span></span> | <span data-ttu-id="874fc-113">Indica che la factory DirectWrite è una factory condivisa e che consente il riutilizzo dei dati dei tipi di carattere memorizzati nella cache tra più componenti in-process.</span><span class="sxs-lookup"><span data-stu-id="874fc-113">Indicates that the DirectWrite factory is a shared factory and that it allows for the reuse of cached font data across multiple in-process components.</span></span> <span data-ttu-id="874fc-114">Tali factory sfruttano anche i componenti di memorizzazione nella cache dei tipi di carattere tra processi per ottenere prestazioni migliori.</span><span class="sxs-lookup"><span data-stu-id="874fc-114">Such factories also take advantage of cross process font caching components for better performance.</span></span> |
| <span data-ttu-id="874fc-115">DWRITE_FACTORY_TYPE_ISOLATED</span><span class="sxs-lookup"><span data-stu-id="874fc-115">DWRITE_FACTORY_TYPE_ISOLATED</span></span> | <span data-ttu-id="874fc-116">Indica che l'oggetto factory DirectWrite è isolato.</span><span class="sxs-lookup"><span data-stu-id="874fc-116">Indicates that the DirectWrite factory object is isolated.</span></span> <span data-ttu-id="874fc-117">Gli oggetti creati dalla factory isolata non interagiscono con lo stato DirectWrite interno da altri componenti.</span><span class="sxs-lookup"><span data-stu-id="874fc-117">Objects created from the isolated factory do not interact with internal DirectWrite state from other components.</span></span> |
| <span data-ttu-id="874fc-118">DWRITE_FACTORY_TYPE_ISOLATED2</span><span class="sxs-lookup"><span data-stu-id="874fc-118">DWRITE_FACTORY_TYPE_ISOLATED2</span></span> | <span data-ttu-id="874fc-119">Indica che l'oggetto factory DirectWrite è limitato.</span><span class="sxs-lookup"><span data-stu-id="874fc-119">Indicates that the DirectWrite factory object is restricted.</span></span> <span data-ttu-id="874fc-120">Gli oggetti creati da una factory con restrizioni non usano né modificano lo stato interno o i dati memorizzati nella cache usati da altre factory.</span><span class="sxs-lookup"><span data-stu-id="874fc-120">Objects created from a restricted factory don't use nor modify internal state or cached data used by other factories.</span></span> <span data-ttu-id="874fc-121">Inoltre, la raccolta di tipi di carattere di sistema contiene solo tipi di carattere noti.</span><span class="sxs-lookup"><span data-stu-id="874fc-121">In addition, the system font collection contains only well-known fonts.</span></span>|

## <a name="examples"></a><span data-ttu-id="874fc-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="874fc-122">Examples</span></span>

<span data-ttu-id="874fc-123">Vedere [l'argomento di panoramica DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) e l'app di esempio [DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)</span><span class="sxs-lookup"><span data-stu-id="874fc-123">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="874fc-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="874fc-124">Remarks</span></span>

<span data-ttu-id="874fc-125">Un oggetto factory DirectWrite contiene informazioni sullo stato interno, ad esempio la registrazione del caricatore dei tipi di carattere e i dati dei tipi di carattere memorizzati nella cache.</span><span class="sxs-lookup"><span data-stu-id="874fc-125">A DirectWrite factory object contains information about its internal state, such as font loader registration and cached font data.</span></span> <span data-ttu-id="874fc-126">Nella maggior parte dei casi è consigliabile usare l'oggetto factory condiviso, perché consente a più componenti che usano DirectWrite di condividere informazioni interne sullo stato DirectWrite, riducendo così l'utilizzo della memoria.</span><span class="sxs-lookup"><span data-stu-id="874fc-126">In most cases you should use the shared factory object, because it allows multiple components that use DirectWrite to share internal DirectWrite state information, thereby reducing memory usage.</span></span> <span data-ttu-id="874fc-127">In alcuni casi, tuttavia, è preferibile ridurre l'impatto di un componente sul resto del processo, ad esempio un plug-in da un'origine non attendibile, tramite sandboxing e isolamento dal resto dei componenti del processo.</span><span class="sxs-lookup"><span data-stu-id="874fc-127">However, there are cases when it is desirable to reduce the impact of a component on the rest of the process, such as a plug-in from an untrusted source,  by sandboxing and isolating it from the rest of the process components.</span></span> <span data-ttu-id="874fc-128">In questi casi, è consigliabile usare una factory isolata per il componente sandbox.</span><span class="sxs-lookup"><span data-stu-id="874fc-128">In such cases, you should use an isolated factory for the sandboxed component.</span></span>

<span data-ttu-id="874fc-129">Una factory con restrizioni è più bloccata rispetto a una factory isolata.</span><span class="sxs-lookup"><span data-stu-id="874fc-129">A restricted factory is more locked down than an isolated factory.</span></span> <span data-ttu-id="874fc-130">Non interagisce in alcun modo con una cache dei caratteri multi-processo o persistente.</span><span class="sxs-lookup"><span data-stu-id="874fc-130">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="874fc-131">Inoltre, la raccolta di tipi di carattere di sistema restituita da questa factory include solo tipi di carattere noti.</span><span class="sxs-lookup"><span data-stu-id="874fc-131">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="874fc-132">Se si passa **DWRITE_FACTORY_TYPE_ISOLATED2** a una versione di DWrite precedente a DWriteCore, [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) restituisce **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="874fc-132">If you pass **DWRITE_FACTORY_TYPE_ISOLATED2** to a version of DWrite that's older than DWriteCore, then [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) returns **E_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="874fc-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="874fc-133">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="874fc-134">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="874fc-134">**Minimum supported client**</span></span> | <span data-ttu-id="874fc-135">Windows 10, Project Reunion [app Win32]</span><span class="sxs-lookup"><span data-stu-id="874fc-135">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="874fc-136">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="874fc-136">**Header**</span></span> | <span data-ttu-id="874fc-137">dwrite.h (include dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="874fc-137">dwrite.h (include dwrite_core.h)</span></span> |
