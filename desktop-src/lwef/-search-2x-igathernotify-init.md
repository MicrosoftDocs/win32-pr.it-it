---
title: Metodo IGatherNotify init (deprecated)
description: Questo argomento dell'interfaccia di ricerca desktop di Windows è deprecato e viene sostituito dall'API di ricerca di Windows ISearchPersistentItemsChangedSink nel Windows SDK. | Metodo IGatherNotify init (deprecated)
ms.assetid: 6a5f89eb-10f4-4262-89bf-b47e345f12eb
keywords:
- Metodo Init (deprecated) ambiente Windows legacy
- Metodo Init (deprecated) Windows legacy environment features, interfaccia IGatherNotify
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IGatherNotify, metodo init (deprecated)
topic_type:
- apiref
api_name:
- IGatherNotify.Init (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81379bb4a9a7c6099912bfc9ebca170141d76cd2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321613"
---
# <a name="igathernotifyinit-deprecated-method"></a><span data-ttu-id="cf6ac-107">Metodo IGatherNotify:: init (deprecated)</span><span class="sxs-lookup"><span data-stu-id="cf6ac-107">IGatherNotify::Init (Deprecated) method</span></span>

<span data-ttu-id="cf6ac-108">\[**Init** può essere modificato o non disponibile nelle versioni successive del sistema operativo o del prodotto.\]</span><span class="sxs-lookup"><span data-stu-id="cf6ac-108">\[**Init** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="cf6ac-109">Questo argomento dell'interfaccia di ricerca desktop di Windows è deprecato e viene sostituito dall'API di ricerca di Windows [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="cf6ac-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="cf6ac-110">Inizializza l'interfaccia del Gatherer.</span><span class="sxs-lookup"><span data-stu-id="cf6ac-110">Initializes the Gatherer interface.</span></span> <span data-ttu-id="cf6ac-111">Consente inoltre di specificare l'indice da notificare e l'archivio applicazioni da monitorare.</span><span class="sxs-lookup"><span data-stu-id="cf6ac-111">Also specifies the index to notify and the application store to monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf6ac-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf6ac-112">Syntax</span></span>


```C++
void Init (Deprecated)(
  [in] BSTR    bstrApplication,
  [in] BSTR    bstrProject,
  [in] variant varScopesBstrArray
);
```



## <a name="parameters"></a><span data-ttu-id="cf6ac-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="cf6ac-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf6ac-114">*bstrApplication* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf6ac-114">*bstrApplication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf6ac-115">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cf6ac-115">Type: **BSTR**</span></span>

<span data-ttu-id="cf6ac-116">Stringa che specifica l'applicazione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cf6ac-116">A string that specifies the target application.</span></span>

</dd> <dt>

<span data-ttu-id="cf6ac-117">*bstrProject* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf6ac-117">*bstrProject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf6ac-118">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cf6ac-118">Type: **BSTR**</span></span>

<span data-ttu-id="cf6ac-119">Stringa che specifica il nome dell'indicizzatore a cui passare le informazioni del Gatherer.</span><span class="sxs-lookup"><span data-stu-id="cf6ac-119">A string that specifies the name of the indexer to pass gatherer information to.</span></span>

</dd> <dt>

<span data-ttu-id="cf6ac-120">*varScopesBstrArray* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf6ac-120">*varScopesBstrArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf6ac-121">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="cf6ac-121">Type: **variant**</span></span>

<span data-ttu-id="cf6ac-122">Parametro facoltativo che consente di passare una matrice di ambiti da inizializzare.</span><span class="sxs-lookup"><span data-stu-id="cf6ac-122">Optional parameter, that enables you to pass an array of scopes to be initialized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf6ac-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cf6ac-123">Return value</span></span>

<span data-ttu-id="cf6ac-124">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="cf6ac-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf6ac-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="cf6ac-125">Remarks</span></span>

<span data-ttu-id="cf6ac-126">Inizializzare con Application = "RSApp", Project = "SetIndex".</span><span class="sxs-lookup"><span data-stu-id="cf6ac-126">Initialize with application="RSApp", Project="MyIndex".</span></span>

 

 
