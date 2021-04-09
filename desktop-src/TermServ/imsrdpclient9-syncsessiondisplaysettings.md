---
title: Metodo IMsRdpClient9 SyncSessionDisplaySettings
description: Sincronizza le impostazioni di visualizzazione della sessione.
ms.assetid: cc2c497f-665a-458d-895b-21dd21977890
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SyncSessionDisplaySettings
- Metodo SyncSessionDisplaySettings Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo SyncSessionDisplaySettings
- Metodo SyncSessionDisplaySettings Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, metodo SyncSessionDisplaySettings
topic_type:
- apiref
api_name:
- IMsRdpClient9.SyncSessionDisplaySettings
- IMsRdpClient10.SyncSessionDisplaySettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4429f966c00fb608416d541bec229defeca3e5b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963776"
---
# <a name="imsrdpclient9syncsessiondisplaysettings-method"></a><span data-ttu-id="b9910-108">Metodo IMsRdpClient9:: SyncSessionDisplaySettings</span><span class="sxs-lookup"><span data-stu-id="b9910-108">IMsRdpClient9::SyncSessionDisplaySettings method</span></span>

<span data-ttu-id="b9910-109">Sincronizza le impostazioni di visualizzazione della sessione.</span><span class="sxs-lookup"><span data-stu-id="b9910-109">Synchronizes session display settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9910-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9910-110">Syntax</span></span>


```C++
HRESULT SyncSessionDisplaySettings();
```



## <a name="parameters"></a><span data-ttu-id="b9910-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9910-111">Parameters</span></span>

<span data-ttu-id="b9910-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b9910-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b9910-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9910-113">Return value</span></span>

<span data-ttu-id="b9910-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b9910-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b9910-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b9910-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9910-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9910-116">Requirements</span></span>



| <span data-ttu-id="b9910-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9910-117">Requirement</span></span> | <span data-ttu-id="b9910-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b9910-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9910-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9910-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b9910-120">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b9910-120">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="b9910-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9910-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b9910-122">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b9910-122">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="b9910-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="b9910-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="b9910-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9910-124"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="b9910-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b9910-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9910-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9910-126"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="b9910-127">IID</span><span class="sxs-lookup"><span data-stu-id="b9910-127">IID</span></span><br/>                      | <span data-ttu-id="b9910-128">CLSID \_ MsRdpClient9 è definito come 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="b9910-128">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="b9910-129">CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4c24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="b9910-129">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="b9910-130">IID \_ IMsRdpClient9 è definito come 28904001-04B6-436c-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="b9910-130">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b9910-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9910-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9910-132">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="b9910-132">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="b9910-133">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="b9910-133">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





