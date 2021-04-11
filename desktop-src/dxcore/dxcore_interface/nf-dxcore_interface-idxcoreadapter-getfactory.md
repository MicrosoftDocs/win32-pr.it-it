---
title: IDXCoreAdapter::GetFactory
description: "Recupera un puntatore di interfaccia [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) all'oggetto factory dell'adattatore dxcore. | IDXCoreAdapter:: GetFactory"
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 1ac3e7fccd39b9b03ecb7016494a610519d26afa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234776"
---
# <a name="idxcoreadaptergetfactory-method"></a><span data-ttu-id="7f6c5-104">Metodo IDXCoreAdapter:: GetFactory</span><span class="sxs-lookup"><span data-stu-id="7f6c5-104">IDXCoreAdapter::GetFactory method</span></span>

<span data-ttu-id="7f6c5-105">Recupera un puntatore di interfaccia [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) all'oggetto factory dell'adattatore dxcore.</span><span class="sxs-lookup"><span data-stu-id="7f6c5-105">Retrieves an [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface pointer to the DXCore adapter factory object.</span></span> <span data-ttu-id="7f6c5-106">Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="7f6c5-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f6c5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f6c5-107">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE GetFactory(
  REFIID riid,
  _COM_Outptr_ void** ppvFactory
) = 0;

template <class T>
HRESULT GetFactory(_COM_Outptr_ T** ppvFactory);
```

## <a name="parameters"></a><span data-ttu-id="7f6c5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f6c5-108">Parameters</span></span>

### <a name="riid"></a><span data-ttu-id="7f6c5-109">riid</span><span class="sxs-lookup"><span data-stu-id="7f6c5-109">riid</span></span>

<span data-ttu-id="7f6c5-110">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="7f6c5-110">Type: **REFIID**</span></span>

<span data-ttu-id="7f6c5-111">Riferimento all'identificatore univoco globale (GUID) dell'interfaccia che si desidera venga restituita in *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="7f6c5-111">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvFactory*.</span></span> <span data-ttu-id="7f6c5-112">Questo dovrebbe essere l'identificatore di interfaccia (IID) di [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md).</span><span class="sxs-lookup"><span data-stu-id="7f6c5-112">This is expected to be the interface identifier (IID) of [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md).</span></span>

### <a name="ppvfactory-out"></a><span data-ttu-id="7f6c5-113">ppvFactory [out]</span><span class="sxs-lookup"><span data-stu-id="7f6c5-113">ppvFactory [out]</span></span>

<span data-ttu-id="7f6c5-114">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="7f6c5-114">Type: **void\*\***</span></span>

<span data-ttu-id="7f6c5-115">Indirizzo di un puntatore a un'interfaccia con l'IID specificato nel parametro *riid* .</span><span class="sxs-lookup"><span data-stu-id="7f6c5-115">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="7f6c5-116">In caso di esito positivo, *\* ppvFactory* (l'indirizzo dereferenziato) contiene un puntatore all'oggetto factory dell'adapter DXCore esistente.</span><span class="sxs-lookup"><span data-stu-id="7f6c5-116">Upon successful return, *\*ppvFactory* (the dereferenced address) contains a pointer to the existing DXCore adapter factory object.</span></span> <span data-ttu-id="7f6c5-117">Prima di restituire, la funzione incrementa il conteggio dei riferimenti nell'interfaccia [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) dell'oggetto Factory.</span><span class="sxs-lookup"><span data-stu-id="7f6c5-117">Before returning, the function increments the reference count on the factory object's [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface.</span></span>

## <a name="returns"></a><span data-ttu-id="7f6c5-118">Restituisce</span><span class="sxs-lookup"><span data-stu-id="7f6c5-118">Returns</span></span>

<span data-ttu-id="7f6c5-119">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="7f6c5-119">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="7f6c5-120">Se la funzione ha esito positivo, restituisce **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="7f6c5-120">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="7f6c5-121">In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="7f6c5-121">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="7f6c5-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f6c5-122">Return value</span></span>|<span data-ttu-id="7f6c5-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f6c5-123">Description</span></span>|
|-|-|
|<span data-ttu-id="7f6c5-124">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="7f6c5-124">E_NOINTERFACE</span></span>|<span data-ttu-id="7f6c5-125">È stato specificato un valore non valido per *riid*.</span><span class="sxs-lookup"><span data-stu-id="7f6c5-125">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="7f6c5-126">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="7f6c5-126">E_POINTER</span></span>|<span data-ttu-id="7f6c5-127">`nullptr` fornito per *ppvFactory*.</span><span class="sxs-lookup"><span data-stu-id="7f6c5-127">`nullptr` was provided for *ppvFactory*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="7f6c5-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f6c5-128">Remarks</span></span>

<span data-ttu-id="7f6c5-129">Per la durata del periodo di tempo in cui è presente un riferimento in un'interfaccia [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) , un'interfaccia [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) o un'interfaccia [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) , chiamate aggiuntive a [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList:: GetFactory](./nf-dxcore_interface-idxcoreadapterlist-getfactory.md)o [IDXCoreAdapter:: GetFactory]() restituiranno puntatori allo stesso oggetto, aumentando il conteggio dei riferimenti dell'interfaccia **IDXCoreAdapterFactory** .</span><span class="sxs-lookup"><span data-stu-id="7f6c5-129">For the duration of time that a reference exists on an [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) interface, an [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) interface, or an [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) interface, additional calls to [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList::GetFactory](./nf-dxcore_interface-idxcoreadapterlist-getfactory.md), or [IDXCoreAdapter::GetFactory]() will return pointers to the same object, increasing the reference count of the **IDXCoreAdapterFactory** interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f6c5-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f6c5-130">See also</span></span>

<span data-ttu-id="7f6c5-131">Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="7f6c5-131">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>
