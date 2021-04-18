---
title: Metodo IConfigAsfWriter GetCurrentProfile
description: Il metodo GetCurrentProfile Recupera il profilo definito dall'applicazione.
ms.assetid: 7f6e7085-982b-4234-b890-950efdcdb559
keywords:
- Metodo GetCurrentProfile Windows Media Format
- Metodo GetCurrentProfile Windows Media Format, interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter-formato Windows Media, metodo GetCurrentProfile
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88931d83674ffa84288b4bec10e3c9dba15c812a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299965"
---
# <a name="iconfigasfwritergetcurrentprofile-method"></a><span data-ttu-id="9561c-106">Metodo IConfigAsfWriter:: GetCurrentProfile</span><span class="sxs-lookup"><span data-stu-id="9561c-106">IConfigAsfWriter::GetCurrentProfile method</span></span>

<span data-ttu-id="9561c-107">Il metodo **GetCurrentProfile** Recupera il profilo definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9561c-107">The **GetCurrentProfile** method retrieves the application-defined profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="9561c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9561c-108">Syntax</span></span>


```C++
HRESULT GetCurrentProfile(
  [out] IWMProfile **ppProfile
);
```



## <a name="parameters"></a><span data-ttu-id="9561c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9561c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9561c-110">*ppProfile* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9561c-110">*ppProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9561c-111">Indirizzo di un puntatore che riceve l'interfaccia [**IWMProfile**](iwmprofile.md) del profilo definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9561c-111">Address of a pointer that receives the [**IWMProfile**](iwmprofile.md) interface of the application-defined profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9561c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9561c-112">Return value</span></span>

<span data-ttu-id="9561c-113">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9561c-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="9561c-114">Se ha esito negativo, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9561c-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9561c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="9561c-115">Remarks</span></span>

<span data-ttu-id="9561c-116">Se il metodo ha esito positivo, il puntatore **IWMProfile** restituito ha un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="9561c-116">If the method succeeds, the **IWMProfile** pointer that it returns has an outstanding reference count.</span></span> <span data-ttu-id="9561c-117">Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="9561c-117">Be sure to release the interface when you are finished using it.</span></span>

## <a name="see-also"></a><span data-ttu-id="9561c-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9561c-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="9561c-119">[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9561c-119">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 