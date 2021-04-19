---
description: Verifica se un generatore deve essere associato a una particolare proprietà.
ms.assetid: 8fab2dc2-3549-4559-b704-6783d929274e
title: 'Metodo IProvidePropertyBuilder:: MapPropertyToBuilder'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder.MapPropertyToBuilder
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: 5fa755449bfb97940235fe45f9e299aa828e6faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325214"
---
# <a name="iprovidepropertybuildermappropertytobuilder-method"></a><span data-ttu-id="848e2-103">Metodo IProvidePropertyBuilder:: MapPropertyToBuilder</span><span class="sxs-lookup"><span data-stu-id="848e2-103">IProvidePropertyBuilder::MapPropertyToBuilder method</span></span>

<span data-ttu-id="848e2-104">Verifica se un generatore deve essere associato a una particolare proprietà.</span><span class="sxs-lookup"><span data-stu-id="848e2-104">Checks whether a builder should be associated with a particular property.</span></span>

## <a name="syntax"></a><span data-ttu-id="848e2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="848e2-105">Syntax</span></span>


```C++
void MapPropertyToBuilder(
  [in]          LONG   dispid,
  [out]         DWORD  *pdwCtlBldType,
  [out]         LPBSTR pbstrGuidBldr,
  [out, retval] LPBOOL builderAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="848e2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="848e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="848e2-107">*DISPID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="848e2-107">*dispid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="848e2-108">DISPID della proprietà in questione.</span><span class="sxs-lookup"><span data-stu-id="848e2-108">The DISPID of the property in question.</span></span>

</dd> <dt>

<span data-ttu-id="848e2-109">*pdwCtlBldType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="848e2-109">*pdwCtlBldType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="848e2-110">Generatore di cui eseguire il mapping.</span><span class="sxs-lookup"><span data-stu-id="848e2-110">The builder to be mapped.</span></span> <span data-ttu-id="848e2-111">Questo parametro può essere una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="848e2-111">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="848e2-112">Valore</span><span class="sxs-lookup"><span data-stu-id="848e2-112">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="848e2-113">Significato</span><span class="sxs-lookup"><span data-stu-id="848e2-113">Meaning</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="CTLBLDTYPE_FSTDPROPBUILDER"></span><span id="ctlbldtype_fstdpropbuilder"></span><dl> <span data-ttu-id="848e2-114"><dt>**CTLBLDTYPE \_ FSTDPROPBUILDER**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="848e2-114"><dt>**CTLBLDTYPE\_FSTDPROPBUILDER**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="848e2-115">Richiama un generatore di sistema standard (non supportato in Visual Studio).</span><span class="sxs-lookup"><span data-stu-id="848e2-115">Invoke a standard system builder (not supported in Visual Studio).</span></span><br/> |
| <span id="CTLBLDTYPE_FINTERNALBUILDER"></span><span id="ctlbldtype_finternalbuilder"></span><dl> <span data-ttu-id="848e2-116"><dt>**CTLBLDTYPE \_ FINTERNALBUILDER**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="848e2-116"><dt>**CTLBLDTYPE\_FINTERNALBUILDER**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="848e2-117">Richiamare un generatore personalizzato.</span><span class="sxs-lookup"><span data-stu-id="848e2-117">Invoke a custom builder.</span></span><br/>                                           |
| <span id="CTLBLDTYPE_EDITSOBJDIRECTLY"></span><span id="ctlbldtype_editsobjdirectly"></span><dl> <span data-ttu-id="848e2-118"><dt>**CTLBLDTYPE \_ EDITSOBJDIRECTLY**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="848e2-118"><dt>**CTLBLDTYPE\_EDITSOBJDIRECTLY**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="848e2-119">Il compilatore modifica l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="848e2-119">Builder modifies the object.</span></span> <span data-ttu-id="848e2-120">Si tratta di un comportamento comune.</span><span class="sxs-lookup"><span data-stu-id="848e2-120">This is common behavior.</span></span><br/>              |



 

</dd> <dt>

<span data-ttu-id="848e2-121">*pbstrGuidBldr* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="848e2-121">*pbstrGuidBldr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="848e2-122">GUID che identifica il generatore per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="848e2-122">The GUID that identifies the builder for this property.</span></span>

</dd> <dt>

<span data-ttu-id="848e2-123">*builderAvailable* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="848e2-123">*builderAvailable* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="848e2-124">Questo parametro è **true** se questa proprietà supporta attualmente un generatore.</span><span class="sxs-lookup"><span data-stu-id="848e2-124">This parameter is **TRUE** if this property currently supports a builder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="848e2-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="848e2-125">Return value</span></span>

<span data-ttu-id="848e2-126">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="848e2-126">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="848e2-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="848e2-127">Requirements</span></span>



| <span data-ttu-id="848e2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="848e2-128">Requirement</span></span> | <span data-ttu-id="848e2-129">Valore</span><span class="sxs-lookup"><span data-stu-id="848e2-129">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="848e2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="848e2-130">DLL</span></span><br/> | <dl> <span data-ttu-id="848e2-131"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="848e2-131"><dt>Vsp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="848e2-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="848e2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="848e2-133">**IProvidePropertyBuilder**</span><span class="sxs-lookup"><span data-stu-id="848e2-133">**IProvidePropertyBuilder**</span></span>](iprovidepropertybuilder.md)
</dt> </dl>

 

 




