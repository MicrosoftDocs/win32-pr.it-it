---
description: Il \_ metodo Put size imposta le dimensioni di output e la modalità di estensione.
ms.assetid: 1186eee4-b5c1-4216-abb3-86ea03b2da40
title: 'IResize: metodo:p ut_Size (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 579cee086798e64abd07b25cc4f7bb14405157dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326991"
---
# <a name="iresizeput_size-method"></a><span data-ttu-id="8352d-103">IResize: metodo di \_ dimensioni ut:p</span><span class="sxs-lookup"><span data-stu-id="8352d-103">IResize::put\_Size method</span></span>

> [!Note]  
> <span data-ttu-id="8352d-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="8352d-104">\[Deprecated.</span></span> <span data-ttu-id="8352d-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8352d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8352d-106">Il `put_Size` metodo imposta le dimensioni di output e la modalità di estensione.</span><span class="sxs-lookup"><span data-stu-id="8352d-106">The `put_Size` method sets the output size and stretch mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="8352d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8352d-107">Syntax</span></span>


```C++
HRESULT put_Size(
  [in] int Height,
  [in] int Width,
  [in] int Flags
);
```



## <a name="parameters"></a><span data-ttu-id="8352d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8352d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8352d-109">*Altezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8352d-109">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8352d-110">Altezza del video in pixel.</span><span class="sxs-lookup"><span data-stu-id="8352d-110">The video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="8352d-111">*Larghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8352d-111">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8352d-112">Larghezza del video in pixel.</span><span class="sxs-lookup"><span data-stu-id="8352d-112">The video width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="8352d-113">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8352d-113">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8352d-114">Modalità di estensione.</span><span class="sxs-lookup"><span data-stu-id="8352d-114">The stretch mode.</span></span> <span data-ttu-id="8352d-115">Per i valori possibili, vedere [**ridimensionare i flag**](resize-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="8352d-115">See [**Resize Flags**](resize-flags.md) for possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8352d-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8352d-116">Return value</span></span>

<span data-ttu-id="8352d-117">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8352d-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8352d-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="8352d-118">Remarks</span></span>

<span data-ttu-id="8352d-119">DES può chiamare questo metodo prima o dopo la chiamata di **put \_ mediaType**.</span><span class="sxs-lookup"><span data-stu-id="8352d-119">DES may call this method before or after calling **put\_MediaType**.</span></span> <span data-ttu-id="8352d-120">Se DES chiama questo metodo prima di chiamare **put \_ mediaType**, il filtro deve selezionare un valore predefinito per la profondità del bit e usare i valori delle dimensioni per costruire un tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="8352d-120">If DES calls this method before calling **put\_MediaType**, the filter should select a default value for the bit depth and use the size values to construct an output media type.</span></span> <span data-ttu-id="8352d-121">Se DES chiama questo metodo dopo avere chiamato **put \_ mediaType**, il filtro deve modificare il tipo di output corrente con le nuove dimensioni.</span><span class="sxs-lookup"><span data-stu-id="8352d-121">If DES calls this method after calling **put\_MediaType**, the filter should modify its current output type with the new sizes.</span></span>

<span data-ttu-id="8352d-122">DES può anche chiamare questo metodo dopo la connessione del PIN di output.</span><span class="sxs-lookup"><span data-stu-id="8352d-122">DES may also call this method after the output pin is connected.</span></span> <span data-ttu-id="8352d-123">In tal caso, modificare il tipo di output e riconnettere il pin di output con il nuovo tipo.</span><span class="sxs-lookup"><span data-stu-id="8352d-123">In that case, modify the output type and reconnect the output pin with the new type.</span></span> <span data-ttu-id="8352d-124">Per ulteriori informazioni, vedere [riconnessione dei pin](reconnecting-pins.md) .</span><span class="sxs-lookup"><span data-stu-id="8352d-124">See [Reconnecting Pins](reconnecting-pins.md) for more information.</span></span>

<span data-ttu-id="8352d-125">Il parametro *Flags* specifica il modo in cui il filtro deve eseguire l'operazione di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="8352d-125">The *Flags* parameter specifies how the filter should perform the resizing operation.</span></span>

> [!Note]  
> <span data-ttu-id="8352d-126">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="8352d-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8352d-127">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8352d-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8352d-128">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8352d-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8352d-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8352d-129">Requirements</span></span>



| <span data-ttu-id="8352d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8352d-130">Requirement</span></span> | <span data-ttu-id="8352d-131">Valore</span><span class="sxs-lookup"><span data-stu-id="8352d-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8352d-132">Versione</span><span class="sxs-lookup"><span data-stu-id="8352d-132">Version</span></span><br/> | <span data-ttu-id="8352d-133">DirectX 9,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8352d-133">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="8352d-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8352d-134">Header</span></span><br/>  | <dl> <span data-ttu-id="8352d-135"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8352d-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8352d-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="8352d-136">Library</span></span><br/> | <dl> <span data-ttu-id="8352d-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8352d-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8352d-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8352d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8352d-139">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="8352d-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="8352d-140">**Interfaccia IResize**</span><span class="sxs-lookup"><span data-stu-id="8352d-140">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




