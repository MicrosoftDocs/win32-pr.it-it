---
description: Il \_ metodo Get Invert recupera un valore booleano che indica se l'operazione del tasto è invertita. Questa proprietà si applica a tutti i tipi di chiave ad eccezione di DXTKEY \_ alfa.
ms.assetid: 2ccf2066-3d9c-493b-bc54-a03e7d075531
title: 'Metodo IDxtKey:: get_Invert (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 51b95758adf6690f6d4fa479ac1cc2c585fa9352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326921"
---
# <a name="idxtkeyget_invert-method"></a><span data-ttu-id="30191-104">Metodo IDxtKey:: Get \_ Invert</span><span class="sxs-lookup"><span data-stu-id="30191-104">IDxtKey::get\_Invert method</span></span>

> [!Note]  
> <span data-ttu-id="30191-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="30191-105">\[Deprecated.</span></span> <span data-ttu-id="30191-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="30191-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="30191-107">Il `get_Invert` metodo recupera un valore booleano che indica se l'operazione del tasto è invertita.</span><span class="sxs-lookup"><span data-stu-id="30191-107">The `get_Invert` method retrieves a Boolean value indicating whether the key operation is inverted.</span></span> <span data-ttu-id="30191-108">Questa proprietà si applica a tutti i tipi di chiave ad eccezione di DXTKEY \_ alfa.</span><span class="sxs-lookup"><span data-stu-id="30191-108">This property applies to all key types except DXTKEY\_ALPHA.</span></span>

## <a name="syntax"></a><span data-ttu-id="30191-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30191-109">Syntax</span></span>


```C++
HRESULT get_Invert(
  [out, retval] BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="30191-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="30191-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30191-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="30191-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="30191-112">Riceve uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="30191-112">Receives one of the following values.</span></span>



| <span data-ttu-id="30191-113">Valore</span><span class="sxs-lookup"><span data-stu-id="30191-113">Value</span></span>     | <span data-ttu-id="30191-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30191-114">Description</span></span>                                                                       |
|-----------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="30191-115">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="30191-115">**TRUE**</span></span>  | <span data-ttu-id="30191-116">I pixel nell'immagine sovrastante vengono invertiti rispetto all'operazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="30191-116">Pixels in the overlying image are inverted with respect to the default operation.</span></span> |
| <span data-ttu-id="30191-117">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="30191-117">**FALSE**</span></span> | <span data-ttu-id="30191-118">I pixel nell'immagine di sovrastanti vengono resi trasparenti nel modo predefinito.</span><span class="sxs-lookup"><span data-stu-id="30191-118">Pixels in the overlying image are made transparent in the default manner.</span></span>         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30191-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30191-119">Return value</span></span>

<span data-ttu-id="30191-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="30191-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="30191-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="30191-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="30191-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="30191-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="30191-123">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="30191-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="30191-124">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="30191-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="30191-125">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="30191-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="30191-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30191-126">Requirements</span></span>



| <span data-ttu-id="30191-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="30191-127">Requirement</span></span> | <span data-ttu-id="30191-128">Valore</span><span class="sxs-lookup"><span data-stu-id="30191-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30191-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30191-129">Header</span></span><br/>  | <dl> <span data-ttu-id="30191-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="30191-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="30191-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="30191-131">Library</span></span><br/> | <dl> <span data-ttu-id="30191-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30191-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30191-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30191-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30191-134">**Interfaccia IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="30191-134">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="30191-135">**Tipo di IDxtKey:: Get \_**</span><span class="sxs-lookup"><span data-stu-id="30191-135">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




