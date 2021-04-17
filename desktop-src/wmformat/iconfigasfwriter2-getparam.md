---
title: Metodo getparat IConfigAsfWriter2
description: Il metodo getparat Recupera il valore corrente del parametro di configurazione del filtro specificato.
ms.assetid: 81d915a1-6190-46e3-a5cb-7f5fc242b8dd
keywords:
- Metodo getparat Windows Media Format
- Metodo getparat Windows Media Format, interfaccia IConfigAsfWriter2
- Interfaccia IConfigAsfWriter2-formato Windows Media, metodo getparat
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.GetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d72b8011072424679729686dd5a14c92bae90f66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300256"
---
# <a name="iconfigasfwriter2getparam-method"></a><span data-ttu-id="cc3ed-106">Metodo IConfigAsfWriter2:: getparat</span><span class="sxs-lookup"><span data-stu-id="cc3ed-106">IConfigAsfWriter2::GetParam method</span></span>

<span data-ttu-id="cc3ed-107">Il metodo **Getparat** Recupera il valore corrente del parametro di configurazione del filtro specificato.</span><span class="sxs-lookup"><span data-stu-id="cc3ed-107">The **GetParam** method retrieves the current value of the specified filter configuration parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc3ed-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc3ed-108">Syntax</span></span>


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
);
```



## <a name="parameters"></a><span data-ttu-id="cc3ed-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc3ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc3ed-110">*dwParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc3ed-110">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc3ed-111">Specifica il parametro da recuperare.</span><span class="sxs-lookup"><span data-stu-id="cc3ed-111">Specifies the parameter to retrieve.</span></span> <span data-ttu-id="cc3ed-112">Deve essere un valore definito nell'enumerazione [ \_ \_ \_ param ASFWRITERCONFIG](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="cc3ed-112">It must be a value defined in the [\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="cc3ed-113">*pdwParam1* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cc3ed-113">*pdwParam1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc3ed-114">Puntatore a una variabile che recupera il valore del parametro specificato in *dwParam*.</span><span class="sxs-lookup"><span data-stu-id="cc3ed-114">Pointer to a variable that retrieves the value of the parameter specified in *dwParam*.</span></span>

</dd> <dt>

<span data-ttu-id="cc3ed-115">*pdwParam2* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cc3ed-115">*pdwParam2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc3ed-116">Non utilizzato, deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="cc3ed-116">Not used, must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc3ed-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc3ed-117">Return value</span></span>

<span data-ttu-id="cc3ed-118">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cc3ed-118">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="cc3ed-119">Se ha esito negativo, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cc3ed-119">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="cc3ed-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc3ed-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="cc3ed-121">[**Interfaccia IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cc3ed-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="cc3ed-122">**IConfigAsfWriter2:: separat**</span><span class="sxs-lookup"><span data-stu-id="cc3ed-122">**IConfigAsfWriter2::SetParam**</span></span>](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 