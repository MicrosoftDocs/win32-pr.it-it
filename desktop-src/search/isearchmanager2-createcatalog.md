---
description: Crea un nuovo catalogo personalizzato nell'indicizzatore di ricerca di Windows e ne restituisce un riferimento.
ms.assetid: 2ADC48B8-87A2-4527-9AA8-9B0BA3A12462
title: 'Metodo ISearchManager2:: CreateCatalog'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchManager2.CreateCatalog
api_type:
- COM
api_location:
- searchapi.h
ms.openlocfilehash: 009e34a2d1eb4d18df1747ba01ea39c3360ec81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225944"
---
# <a name="isearchmanager2createcatalog-method"></a><span data-ttu-id="a04eb-103">Metodo ISearchManager2:: CreateCatalog</span><span class="sxs-lookup"><span data-stu-id="a04eb-103">ISearchManager2::CreateCatalog method</span></span>

<span data-ttu-id="a04eb-104">Crea un nuovo catalogo personalizzato nell'indicizzatore di ricerca di Windows e ne restituisce un riferimento.</span><span class="sxs-lookup"><span data-stu-id="a04eb-104">Creates a new custom catalog in the Windows Search indexer and returns a reference to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="a04eb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a04eb-105">Syntax</span></span>


```C++
HRESULT CreateCatalog(
  [in]  LPCWSTR               pszCatalog,
  [out] ISearchCatalogManager **ppCatalogManager
);
```



## <a name="parameters"></a><span data-ttu-id="a04eb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a04eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a04eb-107">*pszCatalog* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a04eb-107">*pszCatalog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a04eb-108">Tipo: **[ **LPCWSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a04eb-108">Type: **[**LPCWSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a04eb-109">Nome del catalogo da creare.</span><span class="sxs-lookup"><span data-stu-id="a04eb-109">Name of catalog to create.</span></span> <span data-ttu-id="a04eb-110">Può essere qualsiasi nome selezionato dal chiamante, deve contenere solo caratteri alfanumerici standard e carattere di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="a04eb-110">Can be any name selected by the caller, must contain only standard alphanumeric characters and underscore.</span></span>

</dd> <dt>

<span data-ttu-id="a04eb-111">*ppCatalogManager* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a04eb-111">*ppCatalogManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a04eb-112">Tipo: **[ **ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***</span><span class="sxs-lookup"><span data-stu-id="a04eb-112">Type: **[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***</span></span>

<span data-ttu-id="a04eb-113">In seguito all'esito positivo, un riferimento al catalogo creato viene restituito come puntatore di interfaccia [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) .</span><span class="sxs-lookup"><span data-stu-id="a04eb-113">On success a reference to the created catalog is returned as an [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) interface pointer.</span></span> <span data-ttu-id="a04eb-114">Il rilascio () deve essere chiamato su questa interfaccia dopo che l'applicazione chiamante ha terminato di utilizzarla.</span><span class="sxs-lookup"><span data-stu-id="a04eb-114">The Release() must be called on this interface after the calling application has finished using it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a04eb-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a04eb-115">Return value</span></span>

<span data-ttu-id="a04eb-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a04eb-116">Type: **HRESULT**</span></span>

<span data-ttu-id="a04eb-117">HRESULT che indica lo stato dell'operazione:</span><span class="sxs-lookup"><span data-stu-id="a04eb-117">HRESULT indicating status of operation:</span></span>



| <span data-ttu-id="a04eb-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a04eb-118">Return code</span></span>                                                                             | <span data-ttu-id="a04eb-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a04eb-119">Description</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a04eb-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a04eb-120"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="a04eb-121">Il catalogo non esisteva in precedenza ed è stato creato.</span><span class="sxs-lookup"><span data-stu-id="a04eb-121">Catalog did not previously exist and was created.</span></span> <span data-ttu-id="a04eb-122">Riferimento al catalogo restituito.</span><span class="sxs-lookup"><span data-stu-id="a04eb-122">Reference to catalog returned.</span></span><br/> |
| <dl> <span data-ttu-id="a04eb-123"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="a04eb-123"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="a04eb-124">Catalogo in precedenza esistente. riferimento al catalogo restituito.</span><span class="sxs-lookup"><span data-stu-id="a04eb-124">Catalog previously existed, reference to catalog returned.</span></span><br/>                       |



 

<span data-ttu-id="a04eb-125">HRESULT non riuscito: errore durante la creazione del catalogo o degli argomenti non validi.</span><span class="sxs-lookup"><span data-stu-id="a04eb-125">FAILED HRESULT: Failure creating catalog or invalid arguments passed.</span></span>

## <a name="remarks"></a><span data-ttu-id="a04eb-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="a04eb-126">Remarks</span></span>

<span data-ttu-id="a04eb-127">Chiamato per creare un nuovo catalogo nell'indicizzatore di ricerca di Windows.</span><span class="sxs-lookup"><span data-stu-id="a04eb-127">Called to create a new catalog in the Windows Search indexer.</span></span> <span data-ttu-id="a04eb-128">Dopo la creazione, è possibile usare i metodi del gestore [**ISearchCatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) restituito per aggiungere percorsi da indicizzare, monitorare il processo di indicizzazione e creare query da inviare all'indicizzatore e ottenere risultati.</span><span class="sxs-lookup"><span data-stu-id="a04eb-128">After creation, the methods on the returned [**ISearchCatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) manager can be used to add locations to be indexed, monitor indexing process, and construct queries to send to the indexer and get results.</span></span> <span data-ttu-id="a04eb-129">Per ulteriori informazioni, vedere la documentazione relativa alla gestione dell'indice: https://msdn.microsoft.com/library/bb266516(VS.85).aspx</span><span class="sxs-lookup"><span data-stu-id="a04eb-129">See the “Managing the Index” documentation for more info: https://msdn.microsoft.com/library/bb266516(VS.85).aspx</span></span>

## <a name="requirements"></a><span data-ttu-id="a04eb-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a04eb-130">Requirements</span></span>



| <span data-ttu-id="a04eb-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a04eb-131">Requirement</span></span> | <span data-ttu-id="a04eb-132">Valore</span><span class="sxs-lookup"><span data-stu-id="a04eb-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a04eb-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a04eb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a04eb-134">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a04eb-134">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="a04eb-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a04eb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a04eb-136">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a04eb-136">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a04eb-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a04eb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a04eb-138">**ISearchManager2**</span><span class="sxs-lookup"><span data-stu-id="a04eb-138">**ISearchManager2**</span></span>](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager2)
</dt> </dl>

 

 
