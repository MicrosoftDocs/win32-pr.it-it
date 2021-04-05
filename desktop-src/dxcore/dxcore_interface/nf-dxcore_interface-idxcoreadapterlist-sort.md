---
title: IDXCoreAdapterList::Sort
description: Ordina un oggetto elenco di adapter DXCore basato su una matrice di input fornita di criteri di ordinamento.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 6260e700053a99b531a66a5c19e15d4a32f07e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118306"
---
# <a name="idxcoreadapterlistsort-method"></a><span data-ttu-id="c1cd1-103">Metodo IDXCoreAdapterList:: Sort</span><span class="sxs-lookup"><span data-stu-id="c1cd1-103">IDXCoreAdapterList::Sort method</span></span>

## <a name="description"></a><span data-ttu-id="c1cd1-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1cd1-104">Description</span></span>

<span data-ttu-id="c1cd1-105">Ordina un oggetto elenco di adapter DXCore in base a una matrice di input fornita di criteri di ordinamento, in cui gli elementi della matrice in precedenza nella matrice di criteri hanno un peso maggiore.</span><span class="sxs-lookup"><span data-stu-id="c1cd1-105">Sorts a DXCore adapter list object based on a provided input array of sort criteria, where array items earlier in the array of criteria are given a higher weight.</span></span> <span data-ttu-id="c1cd1-106">**Ordina** consente di trovare più facilmente la scheda ideale in un elenco di adapter.</span><span class="sxs-lookup"><span data-stu-id="c1cd1-106">**Sort** helps you to more easily find your ideal adapter in an adapter list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1cd1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1cd1-107">Syntax</span></span>

```cpp
HRESULT Sort(
  uint32_t numPreferences,
  _In_reads_(numPreferences) const DXCoreAdapterPreference* preferences
);
```

## <a name="parameters"></a><span data-ttu-id="c1cd1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c1cd1-108">Parameters</span></span>

### <a name="numpreferences"></a><span data-ttu-id="c1cd1-109">numPreferences</span><span class="sxs-lookup"><span data-stu-id="c1cd1-109">numPreferences</span></span>

<span data-ttu-id="c1cd1-110">Tipo: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="c1cd1-110">Type: **uint32_t**</span></span>

<span data-ttu-id="c1cd1-111">Numero di elementi presenti nella matrice a cui punta il parametro *Preferenze* .</span><span class="sxs-lookup"><span data-stu-id="c1cd1-111">The number of elements that are in the array pointed to by the *preferences* parameter.</span></span>

### <a name="preferences-in"></a><span data-ttu-id="c1cd1-112">Preferenze [in]</span><span class="sxs-lookup"><span data-stu-id="c1cd1-112">preferences [in]</span></span>

<span data-ttu-id="c1cd1-113">Tipo: **const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) \***</span><span class="sxs-lookup"><span data-stu-id="c1cd1-113">Type: **const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)\***</span></span>

<span data-ttu-id="c1cd1-114">Puntatore a una matrice di costanti di valori [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) , che rappresenta i criteri di ordinamento.</span><span class="sxs-lookup"><span data-stu-id="c1cd1-114">A pointer to a constant array of [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) values, representing sort criteria.</span></span>

## <a name="returns"></a><span data-ttu-id="c1cd1-115">Restituisce</span><span class="sxs-lookup"><span data-stu-id="c1cd1-115">Returns</span></span>

<span data-ttu-id="c1cd1-116">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="c1cd1-116">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="c1cd1-117">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="c1cd1-117">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="c1cd1-118">In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c1cd1-118">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="c1cd1-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c1cd1-119">Return value</span></span>|<span data-ttu-id="c1cd1-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1cd1-120">Description</span></span>|
|-|-|
|<span data-ttu-id="c1cd1-121">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c1cd1-121">E_INVALIDARG</span></span>|<span data-ttu-id="c1cd1-122">L'argomento *numPreferences* è zero oppure l'argomento di *Preferenze* è `nullptr` .</span><span class="sxs-lookup"><span data-stu-id="c1cd1-122">The *numPreferences* argument is zero, or the *preferences* argument is `nullptr`.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c1cd1-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1cd1-123">Remarks</span></span>

<span data-ttu-id="c1cd1-124">Nei casi in cui un valore [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) specificato non è riconosciuto dal sistema operativo, viene ignorato e non comporta l'esito negativo dell'API.</span><span class="sxs-lookup"><span data-stu-id="c1cd1-124">In cases where a provided [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value isn't recognized by the operating system (OS), it is ignored, and won't cause the API to fail.</span></span> <span data-ttu-id="c1cd1-125">In questo caso, i valori **DXCoreAdapterPreference** noti verranno comunque considerati.</span><span class="sxs-lookup"><span data-stu-id="c1cd1-125">Known **DXCoreAdapterPreference** values will still be considered in this case.</span></span> <span data-ttu-id="c1cd1-126">Per determinare se un tipo di ordinamento viene riconosciuto dall'API, chiamare [IDXCoreAdapterList:: IsAdapterPreferenceSupported](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span><span class="sxs-lookup"><span data-stu-id="c1cd1-126">To determine whether a sort type is understood by the API, call [IDXCoreAdapterList::IsAdapterPreferenceSupported](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span></span>

<span data-ttu-id="c1cd1-127">I valori **DXCoreAdapterPreference** che si verificano in precedenza nella matrice di *Preferenze* fornita vengono trattati con priorità più elevata.</span><span class="sxs-lookup"><span data-stu-id="c1cd1-127">**DXCoreAdapterPreference** values that occur earlier in the provided *preferences* array are treated with higher priority.</span></span> 

<span data-ttu-id="c1cd1-128">Per informazioni dettagliate sulla logica applicata per ogni tipo, vedere la documentazione relativa all'enumerazione **DXCoreAdapterPreference** .</span><span class="sxs-lookup"><span data-stu-id="c1cd1-128">Refer to the **DXCoreAdapterPreference** enumeration documentation for details about what logic is applied for each type.</span></span> <span data-ttu-id="c1cd1-129">La logica interna per un tipo può svilupparsi durante lo sviluppo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c1cd1-129">The internal logic for a type may develop as the OS develops.</span></span>

<span data-ttu-id="c1cd1-130">Quando l' **ordinamento** viene restituito, gli elementi nell'elenco di adapter DXCore sono stati ordinati dal più preferibile al meno preferibile.</span><span class="sxs-lookup"><span data-stu-id="c1cd1-130">When **Sort** returns, items in the DXCore adapter list will have been sorted from most preferable to least preferable.</span></span> <span data-ttu-id="c1cd1-131">Quindi, chiamando [IDXCoreAdapterList:: GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) con indice 0, viene recuperata la scheda che corrisponde maggiormente ai tipi di preferenza di ordinamento richiesti. index 1 è la prossima corrispondenza migliore e così via.</span><span class="sxs-lookup"><span data-stu-id="c1cd1-131">So, calling [IDXCoreAdapterList::GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) with index 0 retrieves the adapter that best matches the requested sort preference types; index 1 is the next best match, and so on.</span></span>

## <a name="see-also"></a><span data-ttu-id="c1cd1-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1cd1-132">See also</span></span>

<span data-ttu-id="c1cd1-133">Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="c1cd1-133">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>