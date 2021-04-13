---
title: Metodo IConfigAsfWriter GetCurrentProfileGuid
description: Il metodo GetCurrentProfileGuid Recupera il GUID del profilo di sistema Windows Media corrente.
ms.assetid: e7a2ecc0-48d4-446c-852a-0d7677cbbe71
keywords:
- Metodo GetCurrentProfileGuid Windows Media Format
- Metodo GetCurrentProfileGuid Windows Media Format, interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter-formato Windows Media, metodo GetCurrentProfileGuid
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49282ed6ea33db8052e167568e5b5fa70cda9e01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338798"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a><span data-ttu-id="de04a-106">Metodo IConfigAsfWriter:: GetCurrentProfileGuid</span><span class="sxs-lookup"><span data-stu-id="de04a-106">IConfigAsfWriter::GetCurrentProfileGuid method</span></span>

<span data-ttu-id="de04a-107">Il metodo **GetCurrentProfileGuid** Recupera il GUID del profilo di sistema Windows Media corrente.</span><span class="sxs-lookup"><span data-stu-id="de04a-107">The **GetCurrentProfileGuid** method retrieves the current Windows Media system profile GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="de04a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de04a-108">Syntax</span></span>


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
);
```



## <a name="parameters"></a><span data-ttu-id="de04a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="de04a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de04a-110">*pProfileGuid* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="de04a-110">*pProfileGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de04a-111">Puntatore a una variabile di tipo **GUID** che identifica il profilo di sistema corrente utilizzato dal filtro.</span><span class="sxs-lookup"><span data-stu-id="de04a-111">Pointer to a variable of type **GUID** that identifies the current system profile being used by the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de04a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de04a-112">Return value</span></span>

<span data-ttu-id="de04a-113">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="de04a-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="de04a-114">Se ha esito negativo, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de04a-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="de04a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="de04a-115">Remarks</span></span>

<span data-ttu-id="de04a-116">Questo metodo non viene usato con i profili personalizzati (inclusi tutti i profili che includono flussi che usano i codec Windows Media Audio e video) perché tutti questi profili vengono creati dalle applicazioni e non hanno un identificatore GUID.</span><span class="sxs-lookup"><span data-stu-id="de04a-116">This method is not used with custom profiles (including all profiles that include streams that use the Windows Media Audio and Video codecs) because all such profiles are created by applications and have no GUID identifier.</span></span> <span data-ttu-id="de04a-117">Se non viene caricato alcun profilo di sistema, *pProfileGuid* verrà impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="de04a-117">If no system profile is loaded, *pProfileGuid* will be set to **NULL**.</span></span>

## <a name="see-also"></a><span data-ttu-id="de04a-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de04a-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="de04a-119">[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="de04a-119">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 