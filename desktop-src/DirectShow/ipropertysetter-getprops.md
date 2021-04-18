---
description: Il metodo GetProps recupera le proprietà impostate per questo oggetto con i valori corrispondenti.
ms.assetid: 2a2ac262-f5a4-4bbe-9cd2-aa7c7d359917
title: 'Metodo IPropertySetter:: GetProps (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.GetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f512ce672cbbaca6556ad644f21c684130eb28e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325480"
---
# <a name="ipropertysettergetprops-method"></a><span data-ttu-id="27253-103">Metodo IPropertySetter:: GetProps</span><span class="sxs-lookup"><span data-stu-id="27253-103">IPropertySetter::GetProps method</span></span>

> [!Note]  
> <span data-ttu-id="27253-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="27253-104">\[Deprecated.</span></span> <span data-ttu-id="27253-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="27253-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="27253-106">Il `GetProps` metodo recupera le proprietà impostate su questo oggetto con i valori corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="27253-106">The `GetProps` method retrieves the properties set on this object, with their corresponding values.</span></span>

## <a name="syntax"></a><span data-ttu-id="27253-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27253-107">Syntax</span></span>


```C++
HRESULT GetProps(
  [out] LONG         *pcParams,
  [out] DEXTER_PARAM **paParam,
  [out] DEXTER_VALUE **paValue
);
```



## <a name="parameters"></a><span data-ttu-id="27253-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="27253-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27253-109">*pcParams* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="27253-109">*pcParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27253-110">Riceve il numero di strutture restituite in *Pieri*.</span><span class="sxs-lookup"><span data-stu-id="27253-110">Receives the number of structures returned in *paParam*.</span></span>

</dd> <dt>

<span data-ttu-id="27253-111">*Pieri* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="27253-111">*paParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27253-112">Indirizzo di un puntatore a una matrice di strutture di [**\_ parametri Dexter**](dexter-param.md) .</span><span class="sxs-lookup"><span data-stu-id="27253-112">Address of a pointer to an array of [**DEXTER\_PARAM**](dexter-param.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="27253-113">*paValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="27253-113">*paValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27253-114">Indirizzo di un puntatore a una matrice di strutture di [**\_ valori Dexter**](dexter-value.md) .</span><span class="sxs-lookup"><span data-stu-id="27253-114">Address of a pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27253-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27253-115">Return value</span></span>

<span data-ttu-id="27253-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="27253-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="27253-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="27253-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="27253-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="27253-118">Remarks</span></span>

<span data-ttu-id="27253-119">Per ogni proprietà restituita in *Pieri*, il membro **nValori** indica il numero di strutture del [**\_ valore Dexter**](dexter-value.md) associate alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="27253-119">For each property returned in *paParam*, the **nValues** member indicates the number of [**DEXTER\_VALUE**](dexter-value.md) structures associated with the property.</span></span> <span data-ttu-id="27253-120">Le coppie vengono restituite in ordine di tempo crescente per ogni proprietà.</span><span class="sxs-lookup"><span data-stu-id="27253-120">The pairs are returned in ascending time order for each property.</span></span>

<span data-ttu-id="27253-121">Al termine dell'utilizzo delle strutture restituite, chiamare [**IPropertySetter:: FreeProps**](ipropertysetter-freeprops.md) per liberare le risorse allocate da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="27253-121">When you are finished using the returned structures, call [**IPropertySetter::FreeProps**](ipropertysetter-freeprops.md) to free the resources allocated by this method.</span></span>

> [!Note]  
> <span data-ttu-id="27253-122">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="27253-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="27253-123">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="27253-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="27253-124">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="27253-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="examples"></a><span data-ttu-id="27253-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="27253-125">Examples</span></span>

<span data-ttu-id="27253-126">Nell'esempio di codice seguente viene illustrato come scorrere tutti i valori di un'istanza del setter della proprietà:</span><span class="sxs-lookup"><span data-stu-id="27253-126">The following code example shows how to iterate through all the values on an instance of the property setter:</span></span>


```C++
IPropertySetter *pSetter = NULL;
// Get a valid IPropertySetter pointer (not shown).

DEXTER_PARAM *pParam;
DEXTER_VALUE *pValue;
LONG count;

hr = pSetter->GetProps(&count, &pParam, &pValue);

LONG num = 0;
for (LONG i = 0; i < count; i++)
{
    for (LONG j = 0; j < pParam[i].nValues; j++)
    {
        // pValue[num] is the next value in the sequence for pParam[i]
    }
    num += pParam[i].nValues;
}
```



## <a name="requirements"></a><span data-ttu-id="27253-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27253-127">Requirements</span></span>



| <span data-ttu-id="27253-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="27253-128">Requirement</span></span> | <span data-ttu-id="27253-129">Valore</span><span class="sxs-lookup"><span data-stu-id="27253-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27253-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27253-130">Header</span></span><br/>  | <dl> <span data-ttu-id="27253-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="27253-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="27253-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="27253-132">Library</span></span><br/> | <dl> <span data-ttu-id="27253-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27253-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27253-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27253-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27253-135">**Interfaccia IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="27253-135">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="27253-136">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="27253-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




