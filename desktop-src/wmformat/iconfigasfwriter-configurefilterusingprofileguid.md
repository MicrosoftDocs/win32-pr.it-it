---
title: Metodo IConfigAsfWriter ConfigureFilterUsingProfileGuid
description: Il metodo ConfigureFilterUsingProfileGuid configura il filtro per la scrittura di un file ASF basato sul profilo predefinito specificato. (Deprecato).
ms.assetid: 94161ee7-1b74-47af-9d77-568abe6237c3
keywords:
- Metodo ConfigureFilterUsingProfileGuid Windows Media Format
- Metodo ConfigureFilterUsingProfileGuid Windows Media Format, interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter-formato Windows Media, metodo ConfigureFilterUsingProfileGuid
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1521738af4411baa2c11f3d20722e09e2d22a83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517025"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileguid-method"></a><span data-ttu-id="dbe7e-107">Metodo IConfigAsfWriter:: ConfigureFilterUsingProfileGuid</span><span class="sxs-lookup"><span data-stu-id="dbe7e-107">IConfigAsfWriter::ConfigureFilterUsingProfileGuid method</span></span>

<span data-ttu-id="dbe7e-108">Il metodo **ConfigureFilterUsingProfileGuid** configura il filtro per la scrittura di un file ASF basato sul profilo predefinito specificato.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-108">The **ConfigureFilterUsingProfileGuid** method configures the filter to write an ASF file based on the specified predefined profile.</span></span> <span data-ttu-id="dbe7e-109">(Deprecata)</span><span class="sxs-lookup"><span data-stu-id="dbe7e-109">(Deprecated.)</span></span>

## <a name="syntax"></a><span data-ttu-id="dbe7e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dbe7e-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfileGuid(
  [in] REFGUID guidProfile
);
```



## <a name="parameters"></a><span data-ttu-id="dbe7e-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="dbe7e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbe7e-112">*guidProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dbe7e-112">*guidProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbe7e-113">**GUID** che identifica un profilo come definito nel file di intestazione Wmsysprf. h di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-113">**GUID** identifying a profile as defined in the Windows Media Format SDK header file Wmsysprf.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbe7e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dbe7e-114">Return value</span></span>

<span data-ttu-id="dbe7e-115">Restituisce uno dei seguenti valori **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dbe7e-115">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="dbe7e-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="dbe7e-116">Return code</span></span>                                                                                         | <span data-ttu-id="dbe7e-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbe7e-117">Description</span></span>                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="dbe7e-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dbe7e-118"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="dbe7e-119">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-119">The method succeeded.</span></span><br/>        |
| <dl> <span data-ttu-id="dbe7e-120"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="dbe7e-120"><dt>**E\_FAIL**</dt></span></span> </dl>              | <span data-ttu-id="dbe7e-121">Profilo non valido.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-121">The profile is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="dbe7e-122"><dt>**\_ \_ stato non corretto di VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dbe7e-122"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="dbe7e-123">Il grafico del filtro è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-123">The filter graph is stopped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dbe7e-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="dbe7e-124">Remarks</span></span>

<span data-ttu-id="dbe7e-125">A partire da Windows Media Format 9 Series SDK, non sono stati definiti nuovi profili di sistema.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-125">Beginning with the Windows Media Format 9 Series SDK, no new system profiles have been defined.</span></span> <span data-ttu-id="dbe7e-126">Con questo metodo è possibile utilizzare solo i GUID del profilo di sistema versione 8 (o versioni precedenti).</span><span class="sxs-lookup"><span data-stu-id="dbe7e-126">Only version 8 (or earlier) system profile GUIDs can be used with this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="dbe7e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dbe7e-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="dbe7e-128">[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dbe7e-128">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

