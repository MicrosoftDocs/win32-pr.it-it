---
description: Il \_ metodo Get Hue Recupera il valore Hue su cui eseguire la chiave. Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ Hue.
ms.assetid: d37fedd6-f29f-4f16-821b-c5f8520c4e12
title: 'Metodo IDxtKey:: get_Hue (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Hue
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72058076e87f1a8738f3153ee8095eefb4ebce8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326922"
---
# <a name="idxtkeyget_hue-method"></a><span data-ttu-id="bf9c4-104">Metodo IDxtKey:: Get \_ Hue</span><span class="sxs-lookup"><span data-stu-id="bf9c4-104">IDxtKey::get\_Hue method</span></span>

> [!Note]  
> <span data-ttu-id="bf9c4-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="bf9c4-105">\[Deprecated.</span></span> <span data-ttu-id="bf9c4-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bf9c4-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bf9c4-107">Il `get_Hue` metodo recupera il valore Hue su cui eseguire la chiave.</span><span class="sxs-lookup"><span data-stu-id="bf9c4-107">The `get_Hue` method retrieves the hue value on which to key.</span></span> <span data-ttu-id="bf9c4-108">Questa proprietà si applica solo quando il tipo di chiave è DXTKEY \_ Hue.</span><span class="sxs-lookup"><span data-stu-id="bf9c4-108">This property applies only when the key type is DXTKEY\_HUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf9c4-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf9c4-109">Syntax</span></span>


```C++
HRESULT get_Hue(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="bf9c4-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf9c4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf9c4-111">*pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="bf9c4-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bf9c4-112">Riceve il valore Hue per il quale eseguire la chiave.</span><span class="sxs-lookup"><span data-stu-id="bf9c4-112">Receives the hue value on which to key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf9c4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf9c4-113">Return value</span></span>

<span data-ttu-id="bf9c4-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bf9c4-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bf9c4-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bf9c4-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf9c4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf9c4-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bf9c4-117">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="bf9c4-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bf9c4-118">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="bf9c4-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bf9c4-119">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="bf9c4-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bf9c4-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf9c4-120">Requirements</span></span>



| <span data-ttu-id="bf9c4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf9c4-121">Requirement</span></span> | <span data-ttu-id="bf9c4-122">Valore</span><span class="sxs-lookup"><span data-stu-id="bf9c4-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf9c4-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf9c4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="bf9c4-124"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf9c4-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bf9c4-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="bf9c4-125">Library</span></span><br/> | <dl> <span data-ttu-id="bf9c4-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf9c4-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf9c4-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf9c4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf9c4-128">**Interfaccia IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="bf9c4-128">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="bf9c4-129">**Tipo di IDxtKey:: Get \_**</span><span class="sxs-lookup"><span data-stu-id="bf9c4-129">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




