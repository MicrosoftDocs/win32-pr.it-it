---
title: Metodo IGatherNotify OnDataMove (deprecato)
description: Questo argomento dell'interfaccia di ricerca desktop di Windows è deprecato e viene sostituito dall'API di ricerca di Windows ISearchPersistentItemsChangedSink nel Windows SDK. | Metodo IGatherNotify OnDataMove (deprecato)
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- Metodo OnDataMove (deprecato) funzionalità dell'ambiente Windows legacy
- Metodo OnDataMove (deprecato) funzionalità dell'ambiente Windows legacy, interfaccia IGatherNotify
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IGatherNotify, metodo OnDataMove (deprecato)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9fe38cd11e9072981334e5b724445ea3393d4361
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353006"
---
# <a name="igathernotifyondatamove-deprecated-method"></a><span data-ttu-id="cfe6b-107">Metodo IGatherNotify:: OnDataMove (deprecato)</span><span class="sxs-lookup"><span data-stu-id="cfe6b-107">IGatherNotify::OnDataMove (Deprecated) method</span></span>

<span data-ttu-id="cfe6b-108">\[**OnDataMove** può essere modificato o non disponibile nelle versioni successive del sistema operativo o del prodotto.\]</span><span class="sxs-lookup"><span data-stu-id="cfe6b-108">\[**OnDataMove** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="cfe6b-109">Questo argomento dell'interfaccia di ricerca desktop di Windows è deprecato e viene sostituito dall'API di ricerca di Windows [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="cfe6b-110">Questo metodo notifica all'indicizzatore i dati spostati.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-110">This method notifies the indexer of data that has been moved.</span></span> <span data-ttu-id="cfe6b-111">Quando Invia la notifica all'indicizzatore, include l'indirizzo precedente, il nuovo indirizzo e l'indirizzo logico.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-111">When it sends the notification to the indexer, it includes the old address, new address, and logical address.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfe6b-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cfe6b-112">Syntax</span></span>


```C++
void OnDataMove (Deprecated)(
  [in] long eChangeAdviseSemantics,
  [in] BSTR bstrOldAddress,
  [in] BSTR bstrNewAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a><span data-ttu-id="cfe6b-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="cfe6b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfe6b-114">*eChangeAdviseSemantics* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfe6b-114">*eChangeAdviseSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe6b-115">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="cfe6b-115">Type: **long**</span></span>

<span data-ttu-id="cfe6b-116">Parametro enumerato che descrive il tipo di spostamento che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-116">An enumerated parameter that describes the type of move that occurred.</span></span>

</dd> <dt>

<span data-ttu-id="cfe6b-117">*bstrOldAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfe6b-117">*bstrOldAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe6b-118">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cfe6b-118">Type: **BSTR**</span></span>

<span data-ttu-id="cfe6b-119">Indirizzo precedente dell'elemento spostato.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-119">The old address of the item that moved.</span></span> <span data-ttu-id="cfe6b-120">Per i file normali,*eChangeAdviseSematics* è **null**.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-120">For normal files,*eChangeAdviseSematics* is **NULL**.</span></span> <span data-ttu-id="cfe6b-121">Per una cartella o una directory, impostare *eChangeAdviseSematics* su \_ gthr \_ directory semantica CA \_ .</span><span class="sxs-lookup"><span data-stu-id="cfe6b-121">For a folder or directory, set *eChangeAdviseSematics* to GTHR\_CA\_SEMANTICS\_DIRECTORY.</span></span>

</dd> <dt>

<span data-ttu-id="cfe6b-122">*bstrNewAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfe6b-122">*bstrNewAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe6b-123">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cfe6b-123">Type: **BSTR**</span></span>

<span data-ttu-id="cfe6b-124">Nuovo indirizzo dell'elemento spostato.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-124">The new address of the item that moved.</span></span>

</dd> <dt>

<span data-ttu-id="cfe6b-125">*bstrLogicalAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfe6b-125">*bstrLogicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfe6b-126">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cfe6b-126">Type: **BSTR**</span></span>

<span data-ttu-id="cfe6b-127">Indirizzo logico dell'elemento spostato.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-127">The logical address of the item that moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfe6b-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cfe6b-128">Return value</span></span>

<span data-ttu-id="cfe6b-129">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-129">This method does not return a value.</span></span>

 

 
