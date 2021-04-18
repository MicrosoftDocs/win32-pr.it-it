---
title: Metodo ITSRemoteProgram3 ServerStartApp
description: Specifica un'app da avviare nella sessione remota.
ms.assetid: 55a05d05-66d5-48a1-b3a6-f087aeb62925
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ServerStartApp
- Metodo ServerStartApp Servizi Desktop remoto, interfaccia ITSRemoteProgram3
- Interfaccia ITSRemoteProgram3 Servizi Desktop remoto, metodo ServerStartApp
topic_type:
- apiref
api_name:
- ITSRemoteProgram3.ServerStartApp
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1822fa98094870ebebe607528cdc69a8a201f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302455"
---
# <a name="itsremoteprogram3serverstartapp-method"></a><span data-ttu-id="36984-106">Metodo ITSRemoteProgram3:: ServerStartApp</span><span class="sxs-lookup"><span data-stu-id="36984-106">ITSRemoteProgram3::ServerStartApp method</span></span>

<span data-ttu-id="36984-107">Specifica un'app da avviare nella sessione remota.</span><span class="sxs-lookup"><span data-stu-id="36984-107">Specifies an App to start in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="36984-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36984-108">Syntax</span></span>


```C++
HRESULT ServerStartApp(
  [in] BSTR         bstrAppUserModelId,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a><span data-ttu-id="36984-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="36984-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36984-110">*bstrAppUserModelId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36984-110">*bstrAppUserModelId* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="36984-111">*bstrArguments* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36984-111">*bstrArguments* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="36984-112">*vbExpandEnvVarInArgumentsOnServer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36984-112">*vbExpandEnvVarInArgumentsOnServer* \[in\]</span></span>
<span data-ttu-id="36984-113"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="36984-113"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="36984-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="36984-114">Return value</span></span>

<span data-ttu-id="36984-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="36984-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="36984-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="36984-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="36984-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36984-117">Requirements</span></span>



| <span data-ttu-id="36984-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="36984-118">Requirement</span></span> | <span data-ttu-id="36984-119">Valore</span><span class="sxs-lookup"><span data-stu-id="36984-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36984-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36984-120">Minimum supported client</span></span><br/> | <span data-ttu-id="36984-121">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="36984-121">Windows 10 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="36984-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36984-122">Minimum supported server</span></span><br/> | <span data-ttu-id="36984-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="36984-123">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="36984-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="36984-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="36984-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36984-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="36984-126">DLL</span><span class="sxs-lookup"><span data-stu-id="36984-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36984-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36984-127"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36984-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36984-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36984-129">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="36984-129">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> </dl>

 

 





