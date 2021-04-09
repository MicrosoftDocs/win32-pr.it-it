---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: DWRITE_FACTORY_TYPE (DWrite. h)
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
ms.openlocfilehash: 603b2ae525ddc6472a3b8581627f2877e06d1aac
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/11/2020
ms.locfileid: "104047784"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a><span data-ttu-id="df8b2-103">Enumerazione DWRITE_FACTORY_TYPE (DWrite. h)</span><span class="sxs-lookup"><span data-stu-id="df8b2-103">DWRITE_FACTORY_TYPE enumeration (dwrite.h)</span></span>

<span data-ttu-id="df8b2-104">Specifica il tipo di oggetto factory DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="df8b2-104">Specifies the type of DirectWrite factory object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="df8b2-105">Questa API è disponibile come parte dell'implementazione di DWriteCore di [DirectWrite](../direct-write-portal.md).</span><span class="sxs-lookup"><span data-stu-id="df8b2-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="df8b2-106">DWriteCore è un'implementazione di DirectWrite, eseguibile su Windows fino alla versione 8, che offre opportunità per l'uso su più piattaforme.</span><span class="sxs-lookup"><span data-stu-id="df8b2-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="df8b2-107">Per altre informazioni ed esempi di codice, vedere [Panoramica di DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="df8b2-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="df8b2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df8b2-108">Syntax</span></span>
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_RESTRICTED
} ;
```

## <a name="constants"></a><span data-ttu-id="df8b2-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="df8b2-109">Constants</span></span>

| <span data-ttu-id="df8b2-110">Nome</span><span class="sxs-lookup"><span data-stu-id="df8b2-110">Name</span></span> | <span data-ttu-id="df8b2-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df8b2-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="df8b2-112">DWRITE_FACTORY_TYPE_SHARED</span><span class="sxs-lookup"><span data-stu-id="df8b2-112">DWRITE_FACTORY_TYPE_SHARED</span></span> | <span data-ttu-id="df8b2-113">Indica che la factory DirectWrite è una factory condivisa e che consente il riutilizzo dei dati del tipo di carattere memorizzati nella cache tra più componenti in-process.</span><span class="sxs-lookup"><span data-stu-id="df8b2-113">Indicates that the DirectWrite factory is a shared factory and that it allows for the reuse of cached font data across multiple in-process components.</span></span> <span data-ttu-id="df8b2-114">Tali Factory sfruttano inoltre i componenti di caching dei tipi di carattere tra processi per ottenere prestazioni migliori.</span><span class="sxs-lookup"><span data-stu-id="df8b2-114">Such factories also take advantage of cross process font caching components for better performance.</span></span> |
| <span data-ttu-id="df8b2-115">DWRITE_FACTORY_TYPE_ISOLATED</span><span class="sxs-lookup"><span data-stu-id="df8b2-115">DWRITE_FACTORY_TYPE_ISOLATED</span></span> | <span data-ttu-id="df8b2-116">Indica che l'oggetto factory DirectWrite è isolato.</span><span class="sxs-lookup"><span data-stu-id="df8b2-116">Indicates that the DirectWrite factory object is isolated.</span></span> <span data-ttu-id="df8b2-117">Gli oggetti creati dalla factory isolata non interagiscono con lo stato DirectWrite interno da altri componenti.</span><span class="sxs-lookup"><span data-stu-id="df8b2-117">Objects created from the isolated factory do not interact with internal DirectWrite state from other components.</span></span> |
| <span data-ttu-id="df8b2-118">DWRITE_FACTORY_TYPE_RESTRICTED</span><span class="sxs-lookup"><span data-stu-id="df8b2-118">DWRITE_FACTORY_TYPE_RESTRICTED</span></span> | <span data-ttu-id="df8b2-119">Gli oggetti creati da una factory con restrizioni non usano né modificano lo stato interno o i dati memorizzati nella cache usati da altre Factory.</span><span class="sxs-lookup"><span data-stu-id="df8b2-119">Objects created from a restricted factory don't use nor modify internal state or cached data used by other factories.</span></span> <span data-ttu-id="df8b2-120">Inoltre, la raccolta di tipi di carattere del sistema contiene solo tipi di carattere noti.</span><span class="sxs-lookup"><span data-stu-id="df8b2-120">In addition, the system font collection contains only well-known fonts.</span></span>|

## <a name="examples"></a><span data-ttu-id="df8b2-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="df8b2-121">Examples</span></span>

<span data-ttu-id="df8b2-122">Vedere l'argomento [Panoramica di DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) e l'app di esempio [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="df8b2-122">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="df8b2-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="df8b2-123">Remarks</span></span>

<span data-ttu-id="df8b2-124">Un oggetto factory DirectWrite contiene informazioni sullo stato interno, ad esempio la registrazione del caricatore del tipo di carattere e i dati del tipo di carattere memorizzati nella cache.</span><span class="sxs-lookup"><span data-stu-id="df8b2-124">A DirectWrite factory object contains information about its internal state, such as font loader registration and cached font data.</span></span> <span data-ttu-id="df8b2-125">Nella maggior parte dei casi è consigliabile usare l'oggetto Factory condiviso, perché consente a più componenti che usano DirectWrite di condividere informazioni sullo stato DirectWrite interno, riducendo così l'utilizzo della memoria.</span><span class="sxs-lookup"><span data-stu-id="df8b2-125">In most cases you should use the shared factory object, because it allows multiple components that use DirectWrite to share internal DirectWrite state information, thereby reducing memory usage.</span></span> <span data-ttu-id="df8b2-126">Tuttavia, esistono casi in cui è consigliabile ridurre l'effetto di un componente sul resto del processo, ad esempio un plug-in da un'origine non attendibile, mediante sandboxing e isolamento dal resto dei componenti del processo.</span><span class="sxs-lookup"><span data-stu-id="df8b2-126">However, there are cases when it is desirable to reduce the impact of a component on the rest of the process, such as a plug-in from an untrusted source,  by sandboxing and isolating it from the rest of the process components.</span></span> <span data-ttu-id="df8b2-127">In questi casi, è necessario utilizzare una factory isolata per il componente creato mediante sandbox.</span><span class="sxs-lookup"><span data-stu-id="df8b2-127">In such cases, you should use an isolated factory for the sandboxed component.</span></span>

<span data-ttu-id="df8b2-128">Una factory con restrizioni è più bloccata rispetto A una factory isolata.</span><span class="sxs-lookup"><span data-stu-id="df8b2-128">A restricted factory is more locked down than an isolated factory.</span></span> <span data-ttu-id="df8b2-129">Non interagisce in alcun modo con una cache dei tipi di carattere incrociata o persistente.</span><span class="sxs-lookup"><span data-stu-id="df8b2-129">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="df8b2-130">Inoltre, la raccolta di tipi di carattere del sistema restituita da questa Factory include solo tipi di carattere noti.</span><span class="sxs-lookup"><span data-stu-id="df8b2-130">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="df8b2-131">Se si passa **DWRITE_FACTORY_TYPE_RESTRICTED** a una versione di DWrite precedente a DWriteCore, [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) restituisce **E_INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="df8b2-131">If you pass **DWRITE_FACTORY_TYPE_RESTRICTED** to a version of DWrite that's older than DWriteCore, then [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) returns **E_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="df8b2-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df8b2-132">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="df8b2-133">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="df8b2-133">**Minimum supported client**</span></span> | <span data-ttu-id="df8b2-134">Windows 10, Project Reunion 0,1 versione provvisoria [app Win32]</span><span class="sxs-lookup"><span data-stu-id="df8b2-134">Windows 10, Project Reunion 0.1 Prerelease [Win32 apps]</span></span> |
| <span data-ttu-id="df8b2-135">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="df8b2-135">**Header**</span></span> | <span data-ttu-id="df8b2-136">DWrite. h (include dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="df8b2-136">dwrite.h (include dwrite_core.h)</span></span> |
