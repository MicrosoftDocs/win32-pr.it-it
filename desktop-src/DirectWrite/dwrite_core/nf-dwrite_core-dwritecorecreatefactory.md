---
UID: NE:dwrite_core.DWriteCoreCreateFactory
title: DWriteCoreCreateFactory (dwrite_core.h)
description: Crea un oggetto factory utilizzato per la creazione successiva di singoli oggetti DWriteCore.
tech.root: DirectWrite
ms.date: 04/21/2021
ms.topic: reference
req.header: dwrite_core.h
req.include-header: ''
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
- DWriteCoreCreateFactory
- dwrite_core/DWriteCoreCreateFactory
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_core.h
api_name:
- DWriteCoreCreateFactory
ms.openlocfilehash: 6606ad884fd65195e9922d348cc4fe565b95f2ee
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107882138"
---
# <a name="dwritecorecreatefactory-function-dwrite_coreh"></a><span data-ttu-id="81081-103">Funzione DWriteCoreCreateFactory (dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="81081-103">DWriteCoreCreateFactory function (dwrite_core.h)</span></span>

<span data-ttu-id="81081-104">Crea un oggetto factory utilizzato per la creazione successiva di singoli oggetti DWriteCore.</span><span class="sxs-lookup"><span data-stu-id="81081-104">Creates a factory object that is used for subsequent creation of individual DWriteCore objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="81081-105">Questa API è disponibile come parte dell'implementazione DWriteCore di [DirectWrite.](../direct-write-portal.md)</span><span class="sxs-lookup"><span data-stu-id="81081-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="81081-106">DWriteCore è un'implementazione di DirectWrite, eseguibile su Windows fino alla versione 8, che offre opportunità per l'uso su più piattaforme.</span><span class="sxs-lookup"><span data-stu-id="81081-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="81081-107">Per altre informazioni ed esempi di codice, vedere [Panoramica di DWriteCore.](/windows/win32/DirectWrite/dwrite/dwritecore-overview)</span><span class="sxs-lookup"><span data-stu-id="81081-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="81081-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81081-108">Syntax</span></span>
```cpp
HRESULT DWRITE_EXPORT DWriteCoreCreateFactory(
    _In_ DWRITE_FACTORY_TYPE factoryType,
    _In_ REFIID iid,
    _COM_Outptr_ IUnknown** factory
);
```

## <a name="parameters"></a><span data-ttu-id="81081-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="81081-109">Parameters</span></span>

`factoryType`

<span data-ttu-id="81081-110">Tipo: <b> <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b></span><span class="sxs-lookup"><span data-stu-id="81081-110">Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b></span></span>

<span data-ttu-id="81081-111">Valore che specifica se l'oggetto factory verrà condiviso, isolato o limitato.</span><span class="sxs-lookup"><span data-stu-id="81081-111">A value that specifies whether the factory object will be shared, isolated, or restricted.</span></span>

`iid`

<span data-ttu-id="81081-112">Tipo: <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="81081-112">Type: <b>REFIID</b></span></span>

<span data-ttu-id="81081-113">Valore GUID che identifica l'interfaccia factory DirectWrite, ad esempio __uuidof(<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).</span><span class="sxs-lookup"><span data-stu-id="81081-113">A GUID value that identifies the DirectWrite factory interface, such as __uuidof(<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).</span></span>

`factory`

<span data-ttu-id="81081-114">Tipo: <b>IUnknown\*\*</b></span><span class="sxs-lookup"><span data-stu-id="81081-114">Type: <b>IUnknown\*\*</b></span></span>

<span data-ttu-id="81081-115">Indirizzo di un puntatore all'oggetto factory DirectWrite appena creato.</span><span class="sxs-lookup"><span data-stu-id="81081-115">An address of a pointer to the newly created DirectWrite factory object.</span></span>

## <a name="return-value"></a><span data-ttu-id="81081-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81081-116">Return value</span></span>

<span data-ttu-id="81081-117">Tipo: <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="81081-117">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="81081-118">Se questo metodo ha esito positivo, <b xmlns:loc="http://microsoft.com/wdcml/l10n">restituisce</b>S_OK .</span><span class="sxs-lookup"><span data-stu-id="81081-118">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="81081-119">In caso contrario, restituisce un <b xmlns:loc="http://microsoft.com/wdcml/l10n">codice di errore HRESULT.</b></span><span class="sxs-lookup"><span data-stu-id="81081-119">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="81081-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="81081-120">Examples</span></span>

<span data-ttu-id="81081-121">Vedere [l'argomento di panoramica di DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) e l'app di esempio [DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)</span><span class="sxs-lookup"><span data-stu-id="81081-121">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="81081-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="81081-122">Remarks</span></span>

<span data-ttu-id="81081-123">Funziona come la funzione [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) esportata dalla versione di sistema di DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="81081-123">This is functionally the same as the [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function exported by the system version of DirectWrite.</span></span> <span data-ttu-id="81081-124">La funzione DWriteCore ha un nome diverso per evitare ambiguità.</span><span class="sxs-lookup"><span data-stu-id="81081-124">The DWriteCore function has a different name to avoid ambiguity.</span></span>

## <a name="requirements"></a><span data-ttu-id="81081-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81081-125">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="81081-126">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="81081-126">**Minimum supported client**</span></span> | <span data-ttu-id="81081-127">Windows 10, Project Reunion [app Win32]</span><span class="sxs-lookup"><span data-stu-id="81081-127">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="81081-128">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="81081-128">**Header**</span></span> | <span data-ttu-id="81081-129">dwrite.h (include dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="81081-129">dwrite.h (include dwrite_core.h)</span></span> |
