---
title: Punto di ingresso di VirtualChannelGetInstance
description: Chiamato per fare in modo che il plug-in crei un'istanza dell'interfaccia IWTSPlugin per tutti i plug-in implementati dalla DLL.
ms.assetid: B81BD61E-1F43-42C9-8839-30F4F4C3973C
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto punto di ingresso di VirtualChannelGetInstance
topic_type:
- apiref
api_name:
- VirtualChannelGetInstance
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 535ebdc8928cceb282dd62de56f8c6fbadc94e90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400430"
---
# <a name="virtualchannelgetinstance-entry-point"></a><span data-ttu-id="0c525-104">Punto di ingresso di VirtualChannelGetInstance</span><span class="sxs-lookup"><span data-stu-id="0c525-104">VirtualChannelGetInstance entry point</span></span>

<span data-ttu-id="0c525-105">Chiamato per fare in modo che il plug-in crei un'istanza dell'interfaccia [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) per tutti i plug-in implementati dalla dll.</span><span class="sxs-lookup"><span data-stu-id="0c525-105">Called to have the plug-in create an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for all plug-ins implemented by the DLL.</span></span>

> [!Note]
>
> <span data-ttu-id="0c525-106">Questa funzione viene implementata dal plug-in e deve essere esportata in base al nome in modo che un'applicazione possa usare le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi in modo dinamico alla funzione.</span><span class="sxs-lookup"><span data-stu-id="0c525-106">This function is implemented by the plug-in and must be exported by name such that an application can use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to the function.</span></span>
>
> <span data-ttu-id="0c525-107">Il prototipo per questa funzione non è contenuto in un file di intestazione pubblico, quindi è necessario dichiararlo esattamente come illustrato.</span><span class="sxs-lookup"><span data-stu-id="0c525-107">The prototype for this function is not contained in any public header file, so you must declare it exactly as shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0c525-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c525-108">Syntax</span></span>


```C++
HRESULT VCAPITYPE VirtualChannelGetInstance(
  _In_    REFIID refiid,
  _Inout_ ULONG  *pNumObjs,
  _Out_   VOID   **ppObjArray
);
```



## <a name="parameters"></a><span data-ttu-id="0c525-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0c525-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c525-110">*REFIID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c525-110">*refiid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c525-111">Specifica il tipo di interfaccia da restituire.</span><span class="sxs-lookup"><span data-stu-id="0c525-111">Specifies the type of interface to return.</span></span> <span data-ttu-id="0c525-112">Deve essere un **IID \_ IWTSPlugin**.</span><span class="sxs-lookup"><span data-stu-id="0c525-112">This must be **IID\_IWTSPlugin**.</span></span>

</dd> <dt>

<span data-ttu-id="0c525-113">*pNumObjs* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="0c525-113">*pNumObjs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c525-114">Indirizzo di una variabile **ULONG** che riceve il numero di interfacce recuperate.</span><span class="sxs-lookup"><span data-stu-id="0c525-114">The address of a **ULONG** variable that receives the number of interfaces retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="0c525-115">*ppObjArray* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0c525-115">*ppObjArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c525-116">Indirizzo di una matrice di puntatori che riceve i puntatori di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="0c525-116">The address of an array of pointers that receives the interface pointers.</span></span> <span data-ttu-id="0c525-117">Se questo parametro è **null**, l'implementazione deve inserire il numero di plug-in implementati dalla dll nel parametro *pNumObjs* .</span><span class="sxs-lookup"><span data-stu-id="0c525-117">If this parameter is **NULL**, the implementation must put the number of plug-ins implemented by the DLL in the *pNumObjs* parameter.</span></span> <span data-ttu-id="0c525-118">Ciò consente al chiamante di allocare la matrice di dimensioni appropriate per *ppObjArray*.</span><span class="sxs-lookup"><span data-stu-id="0c525-118">This allows the caller to allocate the proper size array for *ppObjArray*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c525-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0c525-119">Return value</span></span>

<span data-ttu-id="0c525-120">Se il punto di ingresso ha esito positivo, viene restituito **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0c525-120">If this entry point succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0c525-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0c525-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c525-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c525-122">Requirements</span></span>



| <span data-ttu-id="0c525-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c525-123">Requirement</span></span> | <span data-ttu-id="0c525-124">Valore</span><span class="sxs-lookup"><span data-stu-id="0c525-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0c525-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c525-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0c525-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c525-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0c525-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c525-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0c525-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c525-128">Windows Server 2008</span></span><br/> |



 

