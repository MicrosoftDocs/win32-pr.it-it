---
description: Riprende i processi del pacchetto se sono attualmente sospesi.
ms.assetid: c5376e00-b4b7-4a81-a84c-3a46758fe130
title: 'Metodo IPackageDebugSettings:: Resume'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Resume
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 2d36b11baffdc3f587924acd1732cbdfdb43d37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307075"
---
# <a name="ipackagedebugsettingsresume-method"></a><span data-ttu-id="ab6b2-103">Metodo IPackageDebugSettings:: Resume</span><span class="sxs-lookup"><span data-stu-id="ab6b2-103">IPackageDebugSettings::Resume method</span></span>

<span data-ttu-id="ab6b2-104">Riprende i processi del pacchetto se sono attualmente sospesi.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-104">Resumes the processes of the package if they are currently suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab6b2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab6b2-105">Syntax</span></span>


```C++
HRESULT Resume(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a><span data-ttu-id="ab6b2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab6b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab6b2-107">*PackageFullName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab6b2-107">*packageFullName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab6b2-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="ab6b2-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="ab6b2-109">Nome completo del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-109">The package full name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab6b2-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab6b2-110">Return value</span></span>

<span data-ttu-id="ab6b2-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ab6b2-111">Type: **HRESULT**</span></span>

<span data-ttu-id="ab6b2-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ab6b2-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ab6b2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab6b2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab6b2-114">Remarks</span></span>

<span data-ttu-id="ab6b2-115">Ogni processo riceve l'evento di [**ripresa**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="ab6b2-115">Each process receives the [**Resuming**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) event.</span></span> <span data-ttu-id="ab6b2-116">Può essere utile per gli sviluppatori esaminare il modo in cui le app rispondono a questo evento.</span><span class="sxs-lookup"><span data-stu-id="ab6b2-116">It can be useful for developers to step through how their apps respond to this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab6b2-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab6b2-117">Requirements</span></span>



| <span data-ttu-id="ab6b2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab6b2-118">Requirement</span></span> | <span data-ttu-id="ab6b2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ab6b2-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab6b2-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab6b2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ab6b2-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ab6b2-121">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="ab6b2-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab6b2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ab6b2-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ab6b2-123">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="ab6b2-124">IDL</span><span class="sxs-lookup"><span data-stu-id="ab6b2-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ab6b2-125"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ab6b2-125"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab6b2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab6b2-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="ab6b2-127">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ab6b2-127">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span></span>
</dt> </dl>

 

 
