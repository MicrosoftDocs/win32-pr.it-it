---
title: DXCoreCreateAdapterFactory
description: Crea una factory dell'adattatore DXCore, che è possibile utilizzare per generare altri oggetti DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3f5164578da87af8f4d92c3bedcecb6f3dbaa95e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963336"
---
# <a name="dxcorecreateadapterfactory-function"></a><span data-ttu-id="bcb95-103">DXCoreCreateAdapterFactory (funzione)</span><span class="sxs-lookup"><span data-stu-id="bcb95-103">DXCoreCreateAdapterFactory function</span></span>

## <a name="description"></a><span data-ttu-id="bcb95-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcb95-104">Description</span></span>

<span data-ttu-id="bcb95-105">Crea una factory dell'adattatore DXCore, che è possibile utilizzare per generare altri oggetti DXCore.</span><span class="sxs-lookup"><span data-stu-id="bcb95-105">Creates a DXCore adapter factory, which you can use to generate further DXCore objects.</span></span> <span data-ttu-id="bcb95-106">Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="bcb95-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="bcb95-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="bcb95-107">Parameters</span></span>

### <a name="riid"></a><span data-ttu-id="bcb95-108">riid</span><span class="sxs-lookup"><span data-stu-id="bcb95-108">riid</span></span>

<span data-ttu-id="bcb95-109">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="bcb95-109">Type: **REFIID**</span></span>

<span data-ttu-id="bcb95-110">Riferimento all'identificatore univoco globale (GUID) dell'interfaccia che si desidera venga restituita in *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="bcb95-110">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvFactory*.</span></span> <span data-ttu-id="bcb95-111">Questo dovrebbe essere l'identificatore di interfaccia (IID) di [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md).</span><span class="sxs-lookup"><span data-stu-id="bcb95-111">This is expected to be the interface identifier (IID) of [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md).</span></span>

### <a name="ppvfactory-out"></a><span data-ttu-id="bcb95-112">ppvFactory [out]</span><span class="sxs-lookup"><span data-stu-id="bcb95-112">ppvFactory [out]</span></span>

<span data-ttu-id="bcb95-113">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="bcb95-113">Type: **void\*\***</span></span>

<span data-ttu-id="bcb95-114">Indirizzo di un puntatore a un'interfaccia con l'IID specificato nel parametro *riid* .</span><span class="sxs-lookup"><span data-stu-id="bcb95-114">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="bcb95-115">In caso di esito positivo, *\* ppvFactory* (l'indirizzo dereferenziato) contiene un puntatore alla Factory di DXCore creata.</span><span class="sxs-lookup"><span data-stu-id="bcb95-115">Upon successful return, *\*ppvFactory* (the dereferenced address) contains a pointer to the DXCore factory created.</span></span>

## <a name="returns"></a><span data-ttu-id="bcb95-116">Restituisce</span><span class="sxs-lookup"><span data-stu-id="bcb95-116">Returns</span></span>

<span data-ttu-id="bcb95-117">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="bcb95-117">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="bcb95-118">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="bcb95-118">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="bcb95-119">In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="bcb95-119">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="bcb95-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bcb95-120">Return value</span></span>|<span data-ttu-id="bcb95-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcb95-121">Description</span></span>|
|-|-|
|<span data-ttu-id="bcb95-122">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="bcb95-122">E_NOINTERFACE</span></span>|<span data-ttu-id="bcb95-123">È stato specificato un valore non valido per *riid*.</span><span class="sxs-lookup"><span data-stu-id="bcb95-123">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="bcb95-124">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="bcb95-124">E_POINTER</span></span>|<span data-ttu-id="bcb95-125">`nullptr` fornito per *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="bcb95-125">`nullptr` was provided for *ppvFactory*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="bcb95-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="bcb95-126">Remarks</span></span>

<span data-ttu-id="bcb95-127">Per la durata del periodo di tempo in cui è presente un riferimento in un'interfaccia [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) , un'interfaccia [IDXCoreAdapterList](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) o un'interfaccia [IDXCoreAdapter](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) , chiamate aggiuntive a **DXCoreCreateAdapterFactory**, [IDXCoreAdapterList:: GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md)o [IDXCoreAdapter:: GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) restituiranno puntatori allo stesso oggetto, aumentando il conteggio dei riferimenti dell'interfaccia **IDXCoreAdapterFactory** .</span><span class="sxs-lookup"><span data-stu-id="bcb95-127">For the duration of time that a reference exists on an [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) interface, an [IDXCoreAdapterList](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) interface, or an [IDXCoreAdapter](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) interface, additional calls to **DXCoreCreateAdapterFactory**, [IDXCoreAdapterList::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md), or [IDXCoreAdapter::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) will return pointers to the same object, increasing the reference count of the **IDXCoreAdapterFactory** interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="bcb95-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bcb95-128">See also</span></span>

<span data-ttu-id="bcb95-129">Guida di [riferimento a DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="bcb95-129">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>