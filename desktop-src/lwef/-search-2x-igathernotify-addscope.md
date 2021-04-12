---
title: Metodo IGatherNotify AddScope (deprecato)
description: Questo argomento dell'interfaccia di ricerca desktop di Windows è deprecato e viene sostituito dall'API di ricerca di Windows ISearchPersistentItemsChangedSink nel Windows SDK. | Metodo IGatherNotify AddScope (deprecato)
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- Metodo AddScope (deprecato) funzionalità dell'ambiente Windows legacy
- Metodo AddScope (deprecato) funzionalità dell'ambiente Windows legacy, interfaccia IGatherNotify
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IGatherNotify, metodo AddScope (deprecato)
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 967dc4f30acee2f8d8adbcfec04f0508e53bba15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353011"
---
# <a name="igathernotifyaddscope-deprecated-method"></a><span data-ttu-id="a8f99-107">Metodo IGatherNotify:: AddScope (deprecato)</span><span class="sxs-lookup"><span data-stu-id="a8f99-107">IGatherNotify::AddScope (Deprecated) method</span></span>

<span data-ttu-id="a8f99-108">\[**AddScope** può essere modificato o non disponibile nelle versioni successive del sistema operativo o del prodotto.\]</span><span class="sxs-lookup"><span data-stu-id="a8f99-108">\[**AddScope** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="a8f99-109">Questo argomento dell'interfaccia di ricerca desktop di Windows è deprecato e viene sostituito dall'API di ricerca di Windows [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="a8f99-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="a8f99-110">Aggiunge la pagina iniziale o l'URL che si sta monitorando.</span><span class="sxs-lookup"><span data-stu-id="a8f99-110">Adds the start page or URL you are monitoring.</span></span> <span data-ttu-id="a8f99-111">Viene avviata una ricerca per indicizzazione incrementale quando si esegue la connessione e si presuppone che tutte le altre modifiche apportate all'URL siano notificate</span><span class="sxs-lookup"><span data-stu-id="a8f99-111">This initiates an incremental crawl when you connect, and then assumes all further URL changes are by notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f99-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8f99-112">Syntax</span></span>


```C++
void AddScope (Deprecated)(
  [in] BSTR bstrScope
);
```



## <a name="parameters"></a><span data-ttu-id="a8f99-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8f99-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8f99-114">*bstrScope* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8f99-114">*bstrScope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f99-115">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a8f99-115">Type: **BSTR**</span></span>

<span data-ttu-id="a8f99-116">Stringa che specifica la pagina iniziale o URL che si sta monitorando.</span><span class="sxs-lookup"><span data-stu-id="a8f99-116">A string that specifies the start page or URLthat you are monitoring.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8f99-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8f99-117">Return value</span></span>

<span data-ttu-id="a8f99-118">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a8f99-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8f99-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8f99-119">Remarks</span></span>

<span data-ttu-id="a8f99-120">La chiamata a questo metodo avvia una ricerca per indicizzazione incrementale quando si è connessi all'archivio.</span><span class="sxs-lookup"><span data-stu-id="a8f99-120">Calling this method starts an incremental crawl when connected to the store.</span></span> <span data-ttu-id="a8f99-121">In seguito si presuppone che tutte le modifiche apportate all'URL siano notificate dopo l'aggiornamento iniziale.</span><span class="sxs-lookup"><span data-stu-id="a8f99-121">Thereafter, it is assumed that all URL changes are by notification after the initial update.</span></span>

 

 
