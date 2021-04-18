---
description: Il metodo AddProp aggiunge una proprietà al setter della proprietà, con una matrice di coppie di valori temporali che definiscono il valore della proprietà in un intervallo di tempo.
ms.assetid: bf49e6ed-110d-4851-ace9-04d025f1d21f
title: 'Metodo IPropertySetter:: AddProp (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.AddProp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 230d97a3bcd5ac97359130755abd96742ae5340e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325485"
---
# <a name="ipropertysetteraddprop-method"></a><span data-ttu-id="c66c0-103">Metodo IPropertySetter:: AddProp</span><span class="sxs-lookup"><span data-stu-id="c66c0-103">IPropertySetter::AddProp method</span></span>

> [!Note]  
> <span data-ttu-id="c66c0-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c66c0-104">\[Deprecated.</span></span> <span data-ttu-id="c66c0-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c66c0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c66c0-106">Il `AddProp` metodo aggiunge una proprietà al setter della proprietà, con una matrice di coppie di valori temporali che definiscono il valore della proprietà in un intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="c66c0-106">The `AddProp` method adds a property to the property setter, with an array of time-value pairs defining the value of the property over a range of time.</span></span>

## <a name="syntax"></a><span data-ttu-id="c66c0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c66c0-107">Syntax</span></span>


```C++
HRESULT AddProp(
  [in] DEXTER_PARAM Param,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a><span data-ttu-id="c66c0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c66c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c66c0-109">*Param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c66c0-109">*Param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c66c0-110">[**Dexter \_ Struttura PARAM**](dexter-param.md) che specifica la proprietà.</span><span class="sxs-lookup"><span data-stu-id="c66c0-110">[**DEXTER\_PARAM**](dexter-param.md) structure that specifies the property.</span></span> <span data-ttu-id="c66c0-111">Il membro **nValori** della struttura deve essere uguale alla dimensione della matrice specificata nel parametro *paValue* .</span><span class="sxs-lookup"><span data-stu-id="c66c0-111">The **nValues** member of the structure must equal the size of the array given in the *paValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c66c0-112">*paValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c66c0-112">*paValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c66c0-113">Puntatore a una matrice di strutture del [**\_ valore Dexter**](dexter-value.md) che contengono coppie di valori temporali.</span><span class="sxs-lookup"><span data-stu-id="c66c0-113">Pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures that contain time-value pairs.</span></span> <span data-ttu-id="c66c0-114">La matrice deve essere in ordine di tempo crescente.</span><span class="sxs-lookup"><span data-stu-id="c66c0-114">The array must be in ascending time order.</span></span> <span data-ttu-id="c66c0-115">Gli orari sono relativi all'ora di inizio dell'effetto o della transizione.</span><span class="sxs-lookup"><span data-stu-id="c66c0-115">The times are relative to the starting time of the effect or transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c66c0-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c66c0-116">Return value</span></span>

<span data-ttu-id="c66c0-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c66c0-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c66c0-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c66c0-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c66c0-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c66c0-119">Remarks</span></span>

<span data-ttu-id="c66c0-120">La prima struttura del [**\_ valore Dexter**](dexter-value.md) deve specificare un'ora di riferimento pari a zero e un flag di interpolazione (**dwInterp**) di **DEXTERF \_ Jump** oppure il metodo restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="c66c0-120">The first [**DEXTER\_VALUE**](dexter-value.md) structure must specify a reference time of zero and an interpolation flag (**dwInterp**) of **DEXTERF\_JUMP**, or the method returns an error.</span></span>

> [!Note]  
> <span data-ttu-id="c66c0-121">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="c66c0-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c66c0-122">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c66c0-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c66c0-123">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c66c0-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c66c0-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c66c0-124">Requirements</span></span>



| <span data-ttu-id="c66c0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c66c0-125">Requirement</span></span> | <span data-ttu-id="c66c0-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c66c0-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c66c0-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c66c0-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c66c0-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c66c0-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c66c0-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="c66c0-129">Library</span></span><br/> | <dl> <span data-ttu-id="c66c0-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c66c0-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c66c0-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c66c0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c66c0-132">**Interfaccia IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="c66c0-132">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="c66c0-133">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="c66c0-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




