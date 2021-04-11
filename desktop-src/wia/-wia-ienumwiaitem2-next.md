---
description: Riempie una matrice di puntatori alle interfacce IWiaItem2.
ms.assetid: 35fd5bdf-7e6c-431f-a9c6-62a86ee05f95
title: 'Metodo IEnumWiaItem2:: Next (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Next
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e8800ead0c8f0abaddd0f055f31962d4d55d14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226329"
---
# <a name="ienumwiaitem2next-method"></a><span data-ttu-id="971ff-103">IEnumWiaItem2:: Next (metodo)</span><span class="sxs-lookup"><span data-stu-id="971ff-103">IEnumWiaItem2::Next method</span></span>

<span data-ttu-id="971ff-104">Riempie una matrice di puntatori alle interfacce [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="971ff-104">Fills an array of pointers to [**IWiaItem2**](-wia-iwiaitem2.md) interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="971ff-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="971ff-105">Syntax</span></span>


```C++
HRESULT Next(
  [in]      ULONG     cElt,
  [out]     IWiaItem2 **ppIWiaItem2,
  [in, out] ULONG     *pcEltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="971ff-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="971ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="971ff-107">*cElt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="971ff-107">*cElt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="971ff-108">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="971ff-108">Type: **ULONG**</span></span>

<span data-ttu-id="971ff-109">Specifica il numero di elementi di matrice nella matrice indicata dal parametro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="971ff-109">Specifies the number of array elements in the array indicated by the *ppIWiaItem2* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="971ff-110">*ppIWiaItem2* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="971ff-110">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="971ff-111">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="971ff-111">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="971ff-112">Riceve l'indirizzo di una matrice di puntatori di interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="971ff-112">Receives the address of an array of [**IWiaItem2**](-wia-iwiaitem2.md) interface pointers.</span></span> <span data-ttu-id="971ff-113">**IEnumWiaItem2:: Next** compila questa matrice con i puntatori di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="971ff-113">**IEnumWiaItem2::Next** fills this array with interface pointers.</span></span>

</dd> <dt>

<span data-ttu-id="971ff-114">*pcEltFetched* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="971ff-114">*pcEltFetched* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="971ff-115">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="971ff-115">Type: \**ULONG\** _</span></span>

<span data-ttu-id="971ff-116">Nell'output, questo parametro riceve il numero di puntatori di interfaccia effettivamente archiviati nella matrice indicata dal parametro _ppIWiaItem2 \*.</span><span class="sxs-lookup"><span data-stu-id="971ff-116">On output, this parameter receives the number of interface pointers actually stored in the array indicated by the _ppIWiaItem2\* parameter.</span></span> <span data-ttu-id="971ff-117">Quando l'enumerazione è completa, questo parametro contiene zero.</span><span class="sxs-lookup"><span data-stu-id="971ff-117">When the enumeration is complete, this parameter contains zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="971ff-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="971ff-118">Return value</span></span>

<span data-ttu-id="971ff-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="971ff-119">Type: **HRESULT**</span></span>

<span data-ttu-id="971ff-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="971ff-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="971ff-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="971ff-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="971ff-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="971ff-122">Remarks</span></span>

<span data-ttu-id="971ff-123">Il sistema di runtime Windows Image Acquisition (WIA) 2,0 rappresenta i dispositivi hardware WIA 2,0 come albero gerarchico di oggetti [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="971ff-123">The Windows Image Acquisition (WIA) 2.0 run-time system represents WIA 2.0 hardware devices as a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="971ff-124">Le applicazioni usano il metodo **IEnumWiaItem2:: Next** per ottenere un puntatore a interfaccia **IWiaItem2** per ogni elemento nella cartella corrente dell'albero degli oggetti **IWiaItem2** di un dispositivo hardware.</span><span class="sxs-lookup"><span data-stu-id="971ff-124">Applications use the **IEnumWiaItem2::Next** method to obtain an **IWiaItem2** interface pointer for each item in the current folder of a hardware device's **IWiaItem2** object tree.</span></span>

<span data-ttu-id="971ff-125">Per ottenere l'elenco di puntatori, l'applicazione passa una matrice di puntatori dell'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) che alloca.</span><span class="sxs-lookup"><span data-stu-id="971ff-125">To obtain the list of pointers, the application passes an array of [**IWiaItem2**](-wia-iwiaitem2.md) interface pointers that it allocates.</span></span> <span data-ttu-id="971ff-126">Passa anche il numero di elementi di matrice nel parametro *cElt*.</span><span class="sxs-lookup"><span data-stu-id="971ff-126">It also passes the number of array elements in the parameter *cElt*.</span></span> <span data-ttu-id="971ff-127">Il metodo **IEnumWiaItem2:: Next** riempie la matrice con i puntatori alle interfacce **IWiaItem2** .</span><span class="sxs-lookup"><span data-stu-id="971ff-127">The **IEnumWiaItem2::Next** method fills the array with pointers to **IWiaItem2** interfaces.</span></span>

<span data-ttu-id="971ff-128">Fino al completamento del processo di enumerazione, il metodo **IEnumWiaItem2:: Next** restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="971ff-128">Until the enumeration process completes, the **IEnumWiaItem2::Next** method returns S\_OK.</span></span> <span data-ttu-id="971ff-129">Ogni volta che esegue questa operazione, imposta il valore a cui punta *pcEltFetched* sul numero di elementi inseriti nella matrice.</span><span class="sxs-lookup"><span data-stu-id="971ff-129">Each time it does, it sets the value pointed to by *pcEltFetched* to the number of items it inserted into the array.</span></span> <span data-ttu-id="971ff-130">Quando **IEnumWiaItem2:: Next** termina il processo di enumerazione degli oggetti [**IWiaItem2**](-wia-iwiaitem2.md) , restituisce \_ false e imposta la posizione di memoria a cui punta *pcEltFetched* su zero.</span><span class="sxs-lookup"><span data-stu-id="971ff-130">When **IEnumWiaItem2::Next** finishes the process of enumerating [**IWiaItem2**](-wia-iwiaitem2.md) objects, it returns S\_FALSE and sets the memory location pointed to by *pcEltFetched* to zero.</span></span>

<span data-ttu-id="971ff-131">Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="971ff-131">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="971ff-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="971ff-132">Requirements</span></span>



| <span data-ttu-id="971ff-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="971ff-133">Requirement</span></span> | <span data-ttu-id="971ff-134">Valore</span><span class="sxs-lookup"><span data-stu-id="971ff-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="971ff-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="971ff-135">Minimum supported client</span></span><br/> | <span data-ttu-id="971ff-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="971ff-136">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="971ff-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="971ff-137">Minimum supported server</span></span><br/> | <span data-ttu-id="971ff-138">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="971ff-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="971ff-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="971ff-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="971ff-140"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="971ff-140"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="971ff-141">IDL</span><span class="sxs-lookup"><span data-stu-id="971ff-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="971ff-142"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="971ff-142"><dt>Wia.idl</dt></span></span> </dl> |



 

 
