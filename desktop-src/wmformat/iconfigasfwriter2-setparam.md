---
title: IConfigAsfWriter2 (metodo separat)
description: Il metodo separat imposta il valore del parametro di configurazione del filtro specificato.
ms.assetid: b8067fb2-c379-4b26-b4f7-c790604e3edc
keywords:
- Metodo separat Windows Media Format
- Metodo Separator formato Windows Media, interfaccia IConfigAsfWriter2
- Interfaccia IConfigAsfWriter2-formato Windows Media, metodo separat
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.SetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f123bf11c8297f3a7ce0d4b0047874d8d7b31b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300112"
---
# <a name="iconfigasfwriter2setparam-method"></a><span data-ttu-id="e9018-106">Metodo IConfigAsfWriter2:: separat</span><span class="sxs-lookup"><span data-stu-id="e9018-106">IConfigAsfWriter2::SetParam method</span></span>

<span data-ttu-id="e9018-107">Il metodo **separat** imposta il valore del parametro di configurazione del filtro specificato.</span><span class="sxs-lookup"><span data-stu-id="e9018-107">The **SetParam** method sets the value of the specified filter configuration parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9018-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9018-108">Syntax</span></span>


```C++
HRESULT SetParam(
  [in] DWORD dwParam,
  [in] DWORD dwParam1,
  [in] DWORD dwParam2
);
```



## <a name="parameters"></a><span data-ttu-id="e9018-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9018-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9018-110">*dwParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9018-110">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9018-111">Specifica il parametro da impostare.</span><span class="sxs-lookup"><span data-stu-id="e9018-111">Specifies the parameter to set.</span></span> <span data-ttu-id="e9018-112">Deve essere un valore definito nell'enumerazione [ \_ \_ \_ param ASFWRITERCONFIG](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e9018-112">It must be a value defined in the [\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="e9018-113">*dwParam1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9018-113">*dwParam1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9018-114">Specifica il valore da assegnare al parametro *dwParam* .</span><span class="sxs-lookup"><span data-stu-id="e9018-114">Specifies the value to assign to the *dwParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e9018-115">*dwParam2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9018-115">*dwParam2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9018-116">Non utilizzato; deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="e9018-116">Not used; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9018-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9018-117">Return value</span></span>

<span data-ttu-id="e9018-118">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e9018-118">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="e9018-119">Se ha esito negativo, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e9018-119">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="e9018-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9018-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="e9018-121">[**Interfaccia IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e9018-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e9018-122">**IConfigAsfWriter2:: GetParam**</span><span class="sxs-lookup"><span data-stu-id="e9018-122">**IConfigAsfWriter2::GetParam**</span></span>](iconfigasfwriter2-getparam.md)
</dt> </dl>

 

 