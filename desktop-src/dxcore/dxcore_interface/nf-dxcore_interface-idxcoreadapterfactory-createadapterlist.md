---
title: IDXCoreAdapterFactory::CreateAdapterList
description: Genera un elenco di oggetti adapter che rappresentano lo stato corrente dell'adapter del sistema e soddisfano i criteri specificati.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0a35d4dd9a481880d66988b6ade079534d1297c1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473747"
---
# <a name="idxcoreadapterfactorycreateadapterlist-method"></a><span data-ttu-id="ec772-103">Metodo IDXCoreAdapterFactory:: CreateAdapterList</span><span class="sxs-lookup"><span data-stu-id="ec772-103">IDXCoreAdapterFactory::CreateAdapterList method</span></span>

<span data-ttu-id="ec772-104">Genera un elenco di oggetti adapter che rappresentano lo stato corrente dell'adapter del sistema e soddisfano i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="ec772-104">Generates a list of adapter objects representing the current adapter state of the system, and meeting the criteria specified.</span></span> <span data-ttu-id="ec772-105">Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="ec772-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ec772-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec772-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapterList) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  _COM_Outptr_ T **ppvAdapterList);
```

## <a name="parameters"></a><span data-ttu-id="ec772-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec772-107">Parameters</span></span>

### <a name="numattributes"></a><span data-ttu-id="ec772-108">numAttributes</span><span class="sxs-lookup"><span data-stu-id="ec772-108">numAttributes</span></span>

<span data-ttu-id="ec772-109">Tipo: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="ec772-109">Type: **uint32_t**</span></span>

<span data-ttu-id="ec772-110">Numero di elementi nella matrice a cui punta l'argomento *FilterAttributes* .</span><span class="sxs-lookup"><span data-stu-id="ec772-110">The number of elements in the array pointed to by the *filterAttributes* argument.</span></span>

### <a name="filterattributes-in"></a><span data-ttu-id="ec772-111">filterAttributes [in]</span><span class="sxs-lookup"><span data-stu-id="ec772-111">filterAttributes [in]</span></span>

<span data-ttu-id="ec772-112">Tipo: **GUID \* const**</span><span class="sxs-lookup"><span data-stu-id="ec772-112">Type: **const GUID\***</span></span>

<span data-ttu-id="ec772-113">Puntatore a una matrice di GUID dell'attributo dell'adattatore.</span><span class="sxs-lookup"><span data-stu-id="ec772-113">A pointer to an array of adapter attribute GUIDs.</span></span> <span data-ttu-id="ec772-114">Per un elenco di GUID di attributo, vedere i [GUID dell'attributo della scheda DXCore](../dxcore-adapter-attribute-guids.md).</span><span class="sxs-lookup"><span data-stu-id="ec772-114">For a list of attribute GUIDs, see [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md).</span></span> <span data-ttu-id="ec772-115">È necessario fornire almeno un GUID.</span><span class="sxs-lookup"><span data-stu-id="ec772-115">At least one GUID must be provided.</span></span> <span data-ttu-id="ec772-116">Nel caso in cui sia specificato più di un GUID nella matrice, solo gli adapter che soddisfano *tutti* gli attributi richiesti verranno inclusi nell'elenco restituito.</span><span class="sxs-lookup"><span data-stu-id="ec772-116">In the case that more than one GUID is provided in the array, only adapters that meet *all* of the requested attributes will be included in the returned list.</span></span>

### <a name="riid"></a><span data-ttu-id="ec772-117">riid</span><span class="sxs-lookup"><span data-stu-id="ec772-117">riid</span></span>

<span data-ttu-id="ec772-118">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="ec772-118">Type: **REFIID**</span></span>

<span data-ttu-id="ec772-119">Riferimento all'identificatore univoco globale (GUID) dell'interfaccia che si desidera venga restituita in *ppvAdapterList*.</span><span class="sxs-lookup"><span data-stu-id="ec772-119">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapterList*.</span></span> <span data-ttu-id="ec772-120">Questo dovrebbe essere l'identificatore di interfaccia (IID) di [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md).</span><span class="sxs-lookup"><span data-stu-id="ec772-120">This is expected to be the interface identifier (IID) of [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md).</span></span>

### <a name="ppvadapterlist-out"></a><span data-ttu-id="ec772-121">ppvAdapterList [out]</span><span class="sxs-lookup"><span data-stu-id="ec772-121">ppvAdapterList [out]</span></span>

<span data-ttu-id="ec772-122">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="ec772-122">Type: **void\*\***</span></span>

<span data-ttu-id="ec772-123">Indirizzo di un puntatore a un'interfaccia con l'IID specificato nel parametro *riid* .</span><span class="sxs-lookup"><span data-stu-id="ec772-123">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="ec772-124">In caso di esito positivo, *\* ppvAdapterList* (l'indirizzo dereferenziato) contiene un puntatore all'elenco di adapter creato.</span><span class="sxs-lookup"><span data-stu-id="ec772-124">Upon successful return, *\*ppvAdapterList* (the dereferenced address) contains a pointer to the adapter list created.</span></span>

## <a name="returns"></a><span data-ttu-id="ec772-125">Restituisce</span><span class="sxs-lookup"><span data-stu-id="ec772-125">Returns</span></span>

<span data-ttu-id="ec772-126">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="ec772-126">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="ec772-127">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="ec772-127">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="ec772-128">In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="ec772-128">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="ec772-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec772-129">Return value</span></span>|<span data-ttu-id="ec772-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec772-130">Description</span></span>|
|-|-|
|<span data-ttu-id="ec772-131">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ec772-131">E_INVALIDARG</span></span>|<span data-ttu-id="ec772-132">`nullptr` è stato specificato per *FilterAttributes* oppure è stato specificato 0 per *numAttributes*.</span><span class="sxs-lookup"><span data-stu-id="ec772-132">`nullptr` was provided for *filterAttributes*, or 0 was provided for *numAttributes*.</span></span>|
|<span data-ttu-id="ec772-133">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="ec772-133">E_NOINTERFACE</span></span>|<span data-ttu-id="ec772-134">È stato specificato un valore non valido per *riid*.</span><span class="sxs-lookup"><span data-stu-id="ec772-134">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="ec772-135">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="ec772-135">E_POINTER</span></span>|<span data-ttu-id="ec772-136">`nullptr` fornito per *ppvAdapterList*.</span><span class="sxs-lookup"><span data-stu-id="ec772-136">`nullptr` was provided for *ppvAdapterList*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ec772-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec772-137">Remarks</span></span>

<span data-ttu-id="ec772-138">Anche se non viene trovato alcun adapter, finché gli argomenti sono validi, **CreateAdapterList** crea un oggetto [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) valido e restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="ec772-138">Even if no adapters are found, as long as the arguments are valid, **CreateAdapterList** creates a valid [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) object, and returns **S_OK**.</span></span> <span data-ttu-id="ec772-139">Una volta generati, le schede in questo elenco specifico non cambiano.</span><span class="sxs-lookup"><span data-stu-id="ec772-139">Once generated, the adapters in this specific list won't change.</span></span> <span data-ttu-id="ec772-140">Tuttavia, l'elenco verrà considerato non aggiornato se una delle schede in un secondo momento diventa non valida o se arriva un nuovo adapter che soddisfa i criteri di filtro forniti.</span><span class="sxs-lookup"><span data-stu-id="ec772-140">But the list will be considered stale if one of the adapters later becomes invalid, or if a new adapter arrives that meets the provided filter criteria.</span></span> <span data-ttu-id="ec772-141">L'elenco restituito da **CreateAdapterList** non è ordinato in alcun modo specifico, ma l'ordine di un elenco è coerente tra più chiamate e anche tra i riavvii del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ec772-141">The list returned by **CreateAdapterList** is not ordered in any particular way, but the ordering of a list is consistent across multiple calls, and even across operating system restarts.</span></span> <span data-ttu-id="ec772-142">L'ordinamento può variare in base alle modifiche apportate alla configurazione del sistema, ad esempio l'aggiunta o la rimozione di un adapter o l'aggiornamento di un driver in una scheda esistente.</span><span class="sxs-lookup"><span data-stu-id="ec772-142">The ordering may change upon system configuration changes, including the addition or removal of an adapter, or a driver update on an existing adapter.</span></span> <span data-ttu-id="ec772-143">È possibile eseguire la registrazione per queste modifiche con [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) usando il tipo di notifica **DXCoreNotificationType. AdapterListStale**.</span><span class="sxs-lookup"><span data-stu-id="ec772-143">You can register for these changes with [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) using the notification type **DXCoreNotificationType.AdapterListStale**.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec772-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec772-144">See also</span></span>

<span data-ttu-id="ec772-145">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [riferimento a DXCore](../dxcore-reference.md), [GUID dell'attributo della scheda DXCore](../dxcore-adapter-attribute-guids.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="ec772-145">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>