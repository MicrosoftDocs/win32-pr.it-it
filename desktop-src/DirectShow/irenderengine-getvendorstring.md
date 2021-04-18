---
description: Il metodo GetVendorString Recupera il nome del fornitore. Per gli oggetti del motore di rendering forniti da DirectShow, la stringa del fornitore è &\# 0034; Microsoft Corporation&\# 0034;.
ms.assetid: d0a4c525-67dc-419a-b4d6-8cd51888fd8a
title: 'Metodo IRenderEngine:: GetVendorString (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetVendorString
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: abf339b73fa058c6554965c16428774ad1fdd32c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330795"
---
# <a name="irenderenginegetvendorstring-method"></a><span data-ttu-id="d9b6e-104">Metodo IRenderEngine:: GetVendorString</span><span class="sxs-lookup"><span data-stu-id="d9b6e-104">IRenderEngine::GetVendorString method</span></span>

> [!Note]  
> <span data-ttu-id="d9b6e-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="d9b6e-105">\[Deprecated.</span></span> <span data-ttu-id="d9b6e-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d9b6e-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d9b6e-107">Il `GetVendorString` metodo recupera il nome del fornitore.</span><span class="sxs-lookup"><span data-stu-id="d9b6e-107">The `GetVendorString` method retrieves the name of the vendor.</span></span> <span data-ttu-id="d9b6e-108">Per gli oggetti del motore di rendering forniti da DirectShow, la stringa del fornitore è "Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="d9b6e-108">For the render engine objects that are provided by DirectShow, the vendor string is "Microsoft Corporation".</span></span>

## <a name="syntax"></a><span data-ttu-id="d9b6e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9b6e-109">Syntax</span></span>


```C++
HRESULT GetVendorString(
  [out, retval] BSTR *pVendorID
);
```



## <a name="parameters"></a><span data-ttu-id="d9b6e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9b6e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9b6e-111">*pVendorID* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d9b6e-111">*pVendorID* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b6e-112">Riceve un **BSTR** contenente la stringa del fornitore.</span><span class="sxs-lookup"><span data-stu-id="d9b6e-112">Receives a **BSTR** containing the vendor string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9b6e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9b6e-113">Return value</span></span>

<span data-ttu-id="d9b6e-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d9b6e-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d9b6e-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d9b6e-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9b6e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9b6e-116">Remarks</span></span>

<span data-ttu-id="d9b6e-117">Il metodo alloca memoria per la stringa.</span><span class="sxs-lookup"><span data-stu-id="d9b6e-117">The method allocates memory for the string.</span></span> <span data-ttu-id="d9b6e-118">Per liberare la memoria, l'applicazione deve chiamare **SysFreeString** .</span><span class="sxs-lookup"><span data-stu-id="d9b6e-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="d9b6e-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="d9b6e-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d9b6e-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d9b6e-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d9b6e-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d9b6e-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d9b6e-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9b6e-122">Requirements</span></span>



| <span data-ttu-id="d9b6e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9b6e-123">Requirement</span></span> | <span data-ttu-id="d9b6e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d9b6e-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9b6e-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9b6e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d9b6e-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9b6e-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d9b6e-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="d9b6e-127">Library</span></span><br/> | <dl> <span data-ttu-id="d9b6e-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9b6e-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9b6e-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9b6e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9b6e-130">**Interfaccia IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="d9b6e-130">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="d9b6e-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="d9b6e-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




