---
title: Metodo IConfigAsfWriter GetCurrentProfileId
description: Il metodo GetCurrentProfileId recupera l'ID del profilo corrente. (Solo per i profili Windows Media Format 4,0).
ms.assetid: a5162bb1-5fcb-449e-b8d3-624b863e656d
keywords:
- Metodo GetCurrentProfileId Windows Media Format
- Metodo GetCurrentProfileId Windows Media Format, interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter-formato Windows Media, metodo GetCurrentProfileId
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416ac2c48f6ec8836a7390f18f38eca3dca35274
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299964"
---
# <a name="iconfigasfwritergetcurrentprofileid-method"></a><span data-ttu-id="cca49-107">Metodo IConfigAsfWriter:: GetCurrentProfileId</span><span class="sxs-lookup"><span data-stu-id="cca49-107">IConfigAsfWriter::GetCurrentProfileId method</span></span>

<span data-ttu-id="cca49-108">Il metodo **GetCurrentProfileId** recupera l'ID del profilo corrente.</span><span class="sxs-lookup"><span data-stu-id="cca49-108">The **GetCurrentProfileId** method retrieves the current profile ID.</span></span> <span data-ttu-id="cca49-109">(Solo per i profili Windows Media Format 4,0).</span><span class="sxs-lookup"><span data-stu-id="cca49-109">(For Windows Media Format 4.0 profiles only.)</span></span>

## <a name="syntax"></a><span data-ttu-id="cca49-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cca49-110">Syntax</span></span>


```C++
HRESULT GetCurrentProfileId(
  [out] DWORD *pdwProfileId
);
```



## <a name="parameters"></a><span data-ttu-id="cca49-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="cca49-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cca49-112">*pdwProfileId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cca49-112">*pdwProfileId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cca49-113">Puntatore a una variabile di tipo **DWORD** che riceve l'ID del profilo corrente.</span><span class="sxs-lookup"><span data-stu-id="cca49-113">Pointer to a variable of type **DWORD** that receives the current profile ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cca49-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cca49-114">Return value</span></span>

<span data-ttu-id="cca49-115">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cca49-115">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="cca49-116">Se ha esito negativo, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cca49-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cca49-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="cca49-117">Remarks</span></span>

<span data-ttu-id="cca49-118">Questo metodo è ora obsoleto perché presuppone la versione 4,0 di profili SDK di formato Windows Media.</span><span class="sxs-lookup"><span data-stu-id="cca49-118">This method is now obsolete because it assumes version 4.0 Windows Media Format SDK profiles.</span></span> <span data-ttu-id="cca49-119">Usare invece [**IConfigAsfWriter:: GetCurrentProfile**](iconfigasfwriter-getcurrentprofile.md) o [**IConfigAsfWriter:: GetCurrentProfileGuid**](iconfigasfwriter-getcurrentprofileguid.md) per identificare correttamente un profilo per la versione 7,0 e successive.</span><span class="sxs-lookup"><span data-stu-id="cca49-119">Use [**IConfigAsfWriter::GetCurrentProfile**](iconfigasfwriter-getcurrentprofile.md) or [**IConfigAsfWriter::GetCurrentProfileGuid**](iconfigasfwriter-getcurrentprofileguid.md) instead to correctly identify a profile for version 7.0 and later.</span></span>

## <a name="see-also"></a><span data-ttu-id="cca49-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cca49-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="cca49-121">[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cca49-121">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 