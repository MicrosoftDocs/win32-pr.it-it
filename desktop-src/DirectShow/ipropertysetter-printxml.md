---
description: Il metodo PrintXML converte i dati della proprietà in una stringa XML.
ms.assetid: 24638489-b5ed-4bdd-b40e-6d61c0db1533
title: Metodo IPropertySetter::P rintXML (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.PrintXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f31d36e8642cb669f5e365d6ffe25b538268bd1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329628"
---
# <a name="ipropertysetterprintxml-method"></a><span data-ttu-id="8eece-103">IPropertySetter::P metodo rintXML</span><span class="sxs-lookup"><span data-stu-id="8eece-103">IPropertySetter::PrintXML method</span></span>

> [!Note]  
> <span data-ttu-id="8eece-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="8eece-104">\[Deprecated.</span></span> <span data-ttu-id="8eece-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8eece-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8eece-106">Il `PrintXML` metodo converte i dati della proprietà in una stringa XML.</span><span class="sxs-lookup"><span data-stu-id="8eece-106">The `PrintXML` method converts property data into an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eece-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8eece-107">Syntax</span></span>


```C++
HRESULT PrintXML(
  [out] char *pszXML,
  [in]  int  cbXML,
  [out] int  *pcbPrinted,
  [in]  int  indent
);
```



## <a name="parameters"></a><span data-ttu-id="8eece-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8eece-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8eece-109">*pszXML* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8eece-109">*pszXML* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8eece-110">Puntatore a un buffer che riceve la stringa XML.</span><span class="sxs-lookup"><span data-stu-id="8eece-110">Pointer to a buffer that receives the XML string.</span></span>

</dd> <dt>

<span data-ttu-id="8eece-111">*cbXML* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8eece-111">*cbXML* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8eece-112">Dimensioni del buffer a cui punta *pszXML* in byte.</span><span class="sxs-lookup"><span data-stu-id="8eece-112">Size of the buffer pointed to by *pszXML*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8eece-113">*pcbPrinted* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8eece-113">*pcbPrinted* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8eece-114">Puntatore a una variabile che riceve la lunghezza della stringa XML.</span><span class="sxs-lookup"><span data-stu-id="8eece-114">Pointer to a variable that receives the length of the XML string.</span></span> <span data-ttu-id="8eece-115">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="8eece-115">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8eece-116">*rientro* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8eece-116">*indent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8eece-117">Numero di livelli di rientro per il tag più esterno.</span><span class="sxs-lookup"><span data-stu-id="8eece-117">Number of indent levels for the outermost tag.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8eece-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8eece-118">Return value</span></span>

<span data-ttu-id="8eece-119">Restituisce \_ OK se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8eece-119">Returns S\_OK if successful.</span></span> <span data-ttu-id="8eece-120">In caso contrario, restituisce un valore **HRESULT** che indica la cause dell'errore.</span><span class="sxs-lookup"><span data-stu-id="8eece-120">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span> <span data-ttu-id="8eece-121">Se la stringa XML è più lunga del buffer, il metodo restituisce E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="8eece-121">If the XML string is longer than the buffer, the method returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8eece-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="8eece-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8eece-123">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="8eece-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8eece-124">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8eece-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8eece-125">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8eece-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8eece-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8eece-126">Requirements</span></span>



| <span data-ttu-id="8eece-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eece-127">Requirement</span></span> | <span data-ttu-id="8eece-128">Valore</span><span class="sxs-lookup"><span data-stu-id="8eece-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8eece-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8eece-129">Header</span></span><br/>  | <dl> <span data-ttu-id="8eece-130"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8eece-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8eece-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="8eece-131">Library</span></span><br/> | <dl> <span data-ttu-id="8eece-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8eece-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eece-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8eece-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eece-134">**Interfaccia IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="8eece-134">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="8eece-135">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="8eece-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




