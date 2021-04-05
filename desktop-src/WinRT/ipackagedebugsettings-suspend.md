---
description: Sospende i processi del pacchetto se sono attualmente in esecuzione.
ms.assetid: 83f44285-46ed-4968-b0af-7964dfacf602
title: 'Metodo IPackageDebugSettings:: Suspend'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Suspend
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 385ddc856661090caec4345df6651605b67fe883
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751495"
---
# <a name="ipackagedebugsettingssuspend-method"></a><span data-ttu-id="1c0ad-103">Metodo IPackageDebugSettings:: Suspend</span><span class="sxs-lookup"><span data-stu-id="1c0ad-103">IPackageDebugSettings::Suspend method</span></span>

<span data-ttu-id="1c0ad-104">Sospende i processi del pacchetto se sono attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1c0ad-104">Suspends the processes of the package if they are currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c0ad-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c0ad-105">Syntax</span></span>


```C++
HRESULT Suspend(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a><span data-ttu-id="1c0ad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c0ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c0ad-107">*PackageFullName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c0ad-107">*packageFullName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c0ad-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="1c0ad-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="1c0ad-109">Nome completo del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="1c0ad-109">The package full name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c0ad-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c0ad-110">Return value</span></span>

<span data-ttu-id="1c0ad-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1c0ad-111">Type: **HRESULT**</span></span>

<span data-ttu-id="1c0ad-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="1c0ad-112">This method can return one of these values.</span></span>



| <span data-ttu-id="1c0ad-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1c0ad-113">Return code</span></span>                                                                                            | <span data-ttu-id="1c0ad-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c0ad-114">Description</span></span>                                      |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="1c0ad-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0ad-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="1c0ad-116">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="1c0ad-116">The operation succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="1c0ad-117"><dt>**E \_ STATECHANGE non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0ad-117"><dt>**E\_ILLEGAL\_STATECHANGE**</dt></span></span> </dl> | <span data-ttu-id="1c0ad-118">Il processo non è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1c0ad-118">The process is not currently running.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1c0ad-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c0ad-119">Remarks</span></span>

<span data-ttu-id="1c0ad-120">Ogni processo riceve l'evento di [**sospensione**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="1c0ad-120">Each process receives the [**Suspending**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) event.</span></span> <span data-ttu-id="1c0ad-121">Può essere utile per gli sviluppatori esaminare il modo in cui le app rispondono a questo evento.</span><span class="sxs-lookup"><span data-stu-id="1c0ad-121">It can be useful for developers to step through how their apps respond to this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c0ad-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c0ad-122">Requirements</span></span>



| <span data-ttu-id="1c0ad-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c0ad-123">Requirement</span></span> | <span data-ttu-id="1c0ad-124">Valore</span><span class="sxs-lookup"><span data-stu-id="1c0ad-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c0ad-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c0ad-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1c0ad-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1c0ad-126">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="1c0ad-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c0ad-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1c0ad-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1c0ad-128">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="1c0ad-129">IDL</span><span class="sxs-lookup"><span data-stu-id="1c0ad-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1c0ad-130"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1c0ad-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c0ad-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c0ad-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="1c0ad-132">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1c0ad-132">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span></span>
</dt> </dl>

 

 
