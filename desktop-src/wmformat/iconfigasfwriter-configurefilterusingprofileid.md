---
title: Metodo IConfigAsfWriter ConfigureFilterUsingProfileId
description: Il metodo ConfigureFilterUsingProfileId configura il filtro per la scrittura di un file ASF con un indice dell'identificatore del profilo (ID) dall'elenco dei profili di sistema. (Solo per i profili Windows Media Format 4,0).
ms.assetid: b0375785-83db-4540-aca9-7ba0bb81c1ef
keywords:
- Metodo ConfigureFilterUsingProfileId Windows Media Format
- Metodo ConfigureFilterUsingProfileId Windows Media Format, interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter-formato Windows Media, metodo ConfigureFilterUsingProfileId
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0226195d7657667e3947b55546b321edafa7befc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299966"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileid-method"></a><span data-ttu-id="d382a-107">Metodo IConfigAsfWriter:: ConfigureFilterUsingProfileId</span><span class="sxs-lookup"><span data-stu-id="d382a-107">IConfigAsfWriter::ConfigureFilterUsingProfileId method</span></span>

<span data-ttu-id="d382a-108">Il metodo **ConfigureFilterUsingProfileId** configura il filtro per la scrittura di un file ASF con un indice dell'identificatore del profilo (ID) dall'elenco dei profili di sistema.</span><span class="sxs-lookup"><span data-stu-id="d382a-108">The **ConfigureFilterUsingProfileId** method configures the filter to write an ASF file with a profile identifier (ID) index from the system profile list.</span></span> <span data-ttu-id="d382a-109">(Solo per i profili Windows Media Format 4,0).</span><span class="sxs-lookup"><span data-stu-id="d382a-109">(For Windows Media Format 4.0 profiles only.)</span></span>

## <a name="syntax"></a><span data-ttu-id="d382a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d382a-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfileId(
  [in] DWORD dwProfileId
);
```



## <a name="parameters"></a><span data-ttu-id="d382a-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="d382a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d382a-112">*dwProfileId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d382a-112">*dwProfileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d382a-113">ID del profilo definito nella versione 4,0 di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="d382a-113">Profile ID as defined in version 4.0 of the Windows Media Format SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d382a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d382a-114">Return value</span></span>

<span data-ttu-id="d382a-115">Restituisce uno dei seguenti valori **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d382a-115">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="d382a-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d382a-116">Return code</span></span>                                                                                         | <span data-ttu-id="d382a-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d382a-117">Description</span></span>                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="d382a-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d382a-118"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="d382a-119">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="d382a-119">The method succeeded.</span></span><br/>        |
| <dl> <span data-ttu-id="d382a-120"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="d382a-120"><dt>**E\_FAIL**</dt></span></span> </dl>              | <span data-ttu-id="d382a-121">Profilo non valido.</span><span class="sxs-lookup"><span data-stu-id="d382a-121">The profile is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="d382a-122"><dt>**\_ \_ stato non corretto di VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d382a-122"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="d382a-123">Il grafico del filtro è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="d382a-123">The filter graph is stopped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d382a-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="d382a-124">Remarks</span></span>

<span data-ttu-id="d382a-125">Questo metodo è ora obsoleto perché presuppone la versione 4,0 di profili SDK di formato Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d382a-125">This method is now obsolete because it assumes version 4.0 Windows Media Format SDK profiles.</span></span> <span data-ttu-id="d382a-126">Per configurare il filtro per i profili versione 7,0 e successive, usare [**IConfigAsfWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) o [**IConfigAsfWriter:: ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md).</span><span class="sxs-lookup"><span data-stu-id="d382a-126">To configure the filter for version 7.0 and later profiles, use [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) or [**IConfigAsfWriter::ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d382a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d382a-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="d382a-128">[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d382a-128">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

