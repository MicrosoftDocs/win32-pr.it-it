---
description: 'Il metodo FreeProps libera le risorse allocate dal metodo IPropertySetter:: GetProps. Chiamare questo metodo dopo la chiamata a GetProps, passandogli le strutture restituite da GetProps.'
ms.assetid: 5920d63d-d8eb-4fd5-b0d6-9d175e8e2c86
title: 'Metodo IPropertySetter:: FreeProps (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.FreeProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3cc90d094d3213b5b68f61585296bcb21ebbf5a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325481"
---
# <a name="ipropertysetterfreeprops-method"></a><span data-ttu-id="6337f-104">Metodo IPropertySetter:: FreeProps</span><span class="sxs-lookup"><span data-stu-id="6337f-104">IPropertySetter::FreeProps method</span></span>

> [!Note]  
> <span data-ttu-id="6337f-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="6337f-105">\[Deprecated.</span></span> <span data-ttu-id="6337f-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6337f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6337f-107">Il `FreeProps` metodo libera le risorse allocate dal metodo [**IPropertySetter:: GetProps**](ipropertysetter-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="6337f-107">The `FreeProps` method frees resources allocated by the [**IPropertySetter::GetProps**](ipropertysetter-getprops.md) method.</span></span> <span data-ttu-id="6337f-108">Chiamare questo metodo dopo la chiamata a **GetProps**, passandogli le strutture restituite da **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="6337f-108">Call this method after calling **GetProps**, passing it the structures returned by **GetProps**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6337f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6337f-109">Syntax</span></span>


```C++
void FreeProps(
  [in] LONG         cParams,
  [in] DEXTER_PARAM *paParam,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a><span data-ttu-id="6337f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6337f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6337f-111">*cParams* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6337f-111">*cParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6337f-112">Numero di elementi nella matrice *Pieri* .</span><span class="sxs-lookup"><span data-stu-id="6337f-112">The number of elements in the *paParam* array.</span></span>

</dd> <dt>

<span data-ttu-id="6337f-113">*Pieri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6337f-113">*paParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6337f-114">Puntatore a una matrice di strutture di [**\_ parametri Dexter**](dexter-param.md) .</span><span class="sxs-lookup"><span data-stu-id="6337f-114">Pointer to an array of [**DEXTER\_PARAM**](dexter-param.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="6337f-115">*paValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6337f-115">*paValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6337f-116">Puntatore a una matrice di strutture di [**\_ valori Dexter**](dexter-value.md) .</span><span class="sxs-lookup"><span data-stu-id="6337f-116">Pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6337f-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6337f-117">Return value</span></span>

<span data-ttu-id="6337f-118">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="6337f-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6337f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6337f-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6337f-120">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="6337f-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6337f-121">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6337f-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6337f-122">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6337f-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6337f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6337f-123">Requirements</span></span>



| <span data-ttu-id="6337f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6337f-124">Requirement</span></span> | <span data-ttu-id="6337f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="6337f-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6337f-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6337f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6337f-127"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6337f-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6337f-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="6337f-128">Library</span></span><br/> | <dl> <span data-ttu-id="6337f-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6337f-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6337f-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6337f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6337f-131">**Interfaccia IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="6337f-131">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="6337f-132">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="6337f-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




