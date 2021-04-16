---
title: Metodo ISoftKbd EnumSoftKeyboard (Softkbdc. h)
description: Il metodo ISoftKbd EnumSoftKeyboard enumera le possibili tastiere soft che supportano la lingua specificata.
ms.assetid: c71f99e5-c4c2-4b09-a58f-d3f4348d0c5d
keywords:
- Framework servizi di testo Metodo EnumSoftKeyboard
- Framework dei servizi di testo del metodo EnumSoftKeyboard, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo EnumSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.EnumSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecdb083684163798a68674628a8b1abc2460268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477999"
---
# <a name="isoftkbdenumsoftkeyboard-method"></a><span data-ttu-id="cfc36-106">Metodo ISoftKbd:: EnumSoftKeyboard</span><span class="sxs-lookup"><span data-stu-id="cfc36-106">ISoftKbd::EnumSoftKeyboard method</span></span>

<span data-ttu-id="cfc36-107">Il metodo **ISoftKbd:: EnumSoftKeyboard** enumera le possibili tastiere soft che supportano la lingua specificata.</span><span class="sxs-lookup"><span data-stu-id="cfc36-107">The **ISoftKbd::EnumSoftKeyboard** method enumerates the possible soft keyboards that support the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfc36-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cfc36-108">Syntax</span></span>


```C++
HRESULT EnumSoftKeyboard(
  [in]  LANGID langid,
  [out] DWORD  *lpdwKeyboard
);
```



## <a name="parameters"></a><span data-ttu-id="cfc36-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cfc36-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfc36-110">*LangID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfc36-110">*langid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc36-111">Identificatore della lingua.</span><span class="sxs-lookup"><span data-stu-id="cfc36-111">Language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="cfc36-112">*lpdwKeyboard* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cfc36-112">*lpdwKeyboard* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc36-113">Puntatore a un buffer in cui questo metodo recupera gli identificatori delle tastiere flessibili disponibili.</span><span class="sxs-lookup"><span data-stu-id="cfc36-113">Pointer to a buffer in which this method retrieves identifiers of the available soft keyboards.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfc36-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cfc36-114">Return value</span></span>

<span data-ttu-id="cfc36-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="cfc36-115">This method can return one of these values.</span></span>



| <span data-ttu-id="cfc36-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cfc36-116">Value</span></span>                                                                                        | <span data-ttu-id="cfc36-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfc36-117">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="cfc36-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cfc36-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="cfc36-119">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="cfc36-119">The method was successful.</span></span><br/>         |
| <dl> <span data-ttu-id="cfc36-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cfc36-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="cfc36-121">Il parametro *LangID* non è valido.</span><span class="sxs-lookup"><span data-stu-id="cfc36-121">The *langid* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cfc36-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfc36-122">Requirements</span></span>



| <span data-ttu-id="cfc36-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfc36-123">Requirement</span></span> | <span data-ttu-id="cfc36-124">Valore</span><span class="sxs-lookup"><span data-stu-id="cfc36-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfc36-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfc36-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cfc36-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cfc36-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cfc36-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfc36-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cfc36-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cfc36-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cfc36-129">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="cfc36-129">Redistributable</span></span><br/>          | <span data-ttu-id="cfc36-130">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cfc36-130">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="cfc36-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cfc36-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfc36-132"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfc36-132"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="cfc36-133">IDL</span><span class="sxs-lookup"><span data-stu-id="cfc36-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cfc36-134"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cfc36-134"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="cfc36-135">DLL</span><span class="sxs-lookup"><span data-stu-id="cfc36-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfc36-136"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfc36-136"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfc36-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cfc36-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfc36-138">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="cfc36-138">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





