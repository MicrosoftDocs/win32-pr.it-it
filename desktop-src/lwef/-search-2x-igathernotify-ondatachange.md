---
title: Metodo IGatherNotify OnDataChange (deprecato)
description: Questo argomento dell'interfaccia di ricerca desktop di Windows è deprecato e viene sostituito dall'API di ricerca di Windows ISearchPersistentItemsChangedSink nel Windows SDK. | Metodo IGatherNotify OnDataChange (deprecato)
ms.assetid: 0cbfa6b7-44f0-41f0-93a3-d5941b5822de
keywords:
- Metodo OnDataChange (deprecato) funzionalità dell'ambiente Windows legacy
- Metodo OnDataChange (deprecato) funzionalità dell'ambiente Windows legacy, interfaccia IGatherNotify
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IGatherNotify, Metodo OnDataChange (deprecato)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataChange (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d41edeaa591a7f3cbc9494064906af1815597737
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321611"
---
# <a name="igathernotifyondatachange-deprecated-method"></a><span data-ttu-id="1355c-107">Metodo IGatherNotify:: OnDataChange (deprecato)</span><span class="sxs-lookup"><span data-stu-id="1355c-107">IGatherNotify::OnDataChange (Deprecated) method</span></span>

<span data-ttu-id="1355c-108">\[**OnDataChange** può essere modificato o non disponibile nelle versioni successive del sistema operativo o del prodotto.\]</span><span class="sxs-lookup"><span data-stu-id="1355c-108">\[**OnDataChange** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="1355c-109">Questo argomento dell'interfaccia di ricerca desktop di Windows è deprecato e viene sostituito dall'API di ricerca di Windows [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="1355c-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="1355c-110">Questo metodo notifica all'indicizzatore i dati che sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="1355c-110">This method notifies the indexer of data that has changed.</span></span> <span data-ttu-id="1355c-111">Quando Invia la notifica all'indicizzatore, include il tipo di modifica, l'indirizzo fisico e l'indirizzo logico.</span><span class="sxs-lookup"><span data-stu-id="1355c-111">When it sends the notification to the indexer, it includes the type of change, physical address, and logical address.</span></span>

## <a name="syntax"></a><span data-ttu-id="1355c-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1355c-112">Syntax</span></span>


```C++
void OnDataChange (Deprecated)(
  [in] long eChangeAdvise,
  [in] BSTR bstrPhysicalAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a><span data-ttu-id="1355c-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="1355c-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1355c-114">*eChangeAdvise* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1355c-114">*eChangeAdvise* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1355c-115">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="1355c-115">Type: **long**</span></span>

<span data-ttu-id="1355c-116">Valore enumerato che specifica il tipo di modifica.</span><span class="sxs-lookup"><span data-stu-id="1355c-116">An enumerated value that specifies the type of change.</span></span>

</dd> <dt>

<span data-ttu-id="1355c-117">*bstrPhysicalAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1355c-117">*bstrPhysicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1355c-118">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1355c-118">Type: **BSTR**</span></span>

<span data-ttu-id="1355c-119">Indirizzo fisico dell'elemento modificato.</span><span class="sxs-lookup"><span data-stu-id="1355c-119">The physical address of the item that changed.</span></span>

</dd> <dt>

<span data-ttu-id="1355c-120">*bstrLogicalAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1355c-120">*bstrLogicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1355c-121">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="1355c-121">Type: **BSTR**</span></span>

<span data-ttu-id="1355c-122">Indirizzo logico dell'elemento modificato.</span><span class="sxs-lookup"><span data-stu-id="1355c-122">The logical address of the item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1355c-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1355c-123">Return value</span></span>

<span data-ttu-id="1355c-124">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="1355c-124">This method does not return a value.</span></span>

 

 
