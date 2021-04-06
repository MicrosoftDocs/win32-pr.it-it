---
title: Metodo INapComponentConfig2 InvokeUIFromConfigBlob (NapCommon. h)
description: Viene implementato da convalida integrità sistema (SHV) in base alle esigenze per caricare la configurazione di un computer locale o remoto in memoria e visualizzare un'interfaccia utente che consente la manipolazione dei dati di configurazione.
ms.assetid: 9c012690-6751-4a47-8683-74abac610c77
keywords:
- NAP metodo InvokeUIFromConfigBlob
- Metodo InvokeUIFromConfigBlob NAP, interfaccia INapComponentConfig2
- Interfaccia INapComponentConfig2 NAP, metodo InvokeUIFromConfigBlob
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIFromConfigBlob
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54cc1efaf7da3434e1aff10d57c2e175481a3d2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873566"
---
# <a name="inapcomponentconfig2invokeuifromconfigblob-method"></a><span data-ttu-id="92597-106">Metodo INapComponentConfig2:: InvokeUIFromConfigBlob</span><span class="sxs-lookup"><span data-stu-id="92597-106">INapComponentConfig2::InvokeUIFromConfigBlob method</span></span>

> [!Note]  
> <span data-ttu-id="92597-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="92597-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="92597-108">Il metodo **InvokeUIFromConfigBlob** viene implementato da convalida integrità sistema (SHV) in base alle esigenze per caricare la configurazione di un computer locale o remoto in memoria e visualizzare un'interfaccia utente che consente la manipolazione dei dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="92597-108">The **InvokeUIFromConfigBlob** method is implemented by system health validators (SHVs) as needed to load the configuration of a remote or local machine in memory and display a UI that allows manipulation of the configuration data.</span></span> <span data-ttu-id="92597-109">Il componente di configurazione deve supportare l'utilizzo di [**INapComponentConfig**](inapcomponentconfig.md) tramite DCOM.</span><span class="sxs-lookup"><span data-stu-id="92597-109">The configuration component must support the usage of [**INapComponentConfig**](inapcomponentconfig.md) through DCOM.</span></span>

## <a name="syntax"></a><span data-ttu-id="92597-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92597-110">Syntax</span></span>


```C++
HRESULT InvokeUIFromConfigBlob(
  [in, unique] HWND   hwndParent,
  [in]         UINT16 inbCount,
  [in]         BYTE   *inData,
  [out]        UINT16 *outbCount,
  [out]        BYTE   **outdata,
  [out]        BOOL   *fConfigChanged
);
```



## <a name="parameters"></a><span data-ttu-id="92597-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="92597-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92597-112">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92597-112">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92597-113">Handle per la finestra padre o proprietario.</span><span class="sxs-lookup"><span data-stu-id="92597-113">A handle to the parent or owner window.</span></span> <span data-ttu-id="92597-114">È necessario specificare un handle di finestra valido.</span><span class="sxs-lookup"><span data-stu-id="92597-114">A valid window handle must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="92597-115">*inbCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92597-115">*inbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92597-116">Dimensione in byte di *indata*.</span><span class="sxs-lookup"><span data-stu-id="92597-116">The size, in bytes, of *inData*.</span></span>

</dd> <dt>

<span data-ttu-id="92597-117">*indata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92597-117">*inData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92597-118">Puntatore a un buffer che archivia i dati di configurazione iniziali.</span><span class="sxs-lookup"><span data-stu-id="92597-118">A pointer to a buffer that stores the initial configuration data.</span></span> <span data-ttu-id="92597-119">Questi dati vengono esportati dal computer locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="92597-119">This data is exported from the remote or local machine.</span></span>

</dd> <dt>

<span data-ttu-id="92597-120">*outbCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="92597-120">*outbCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92597-121">Dimensioni, in byte, dei *dati di OutData*.</span><span class="sxs-lookup"><span data-stu-id="92597-121">The size, in bytes, of *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="92597-122">*dati OutData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="92597-122">*outdata* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92597-123">Puntatore a un buffer che archivia i dati di configurazione modificati dall'interfaccia utente di configurazione di convalida integrità di sistema.</span><span class="sxs-lookup"><span data-stu-id="92597-123">A pointer to a buffer that stores configuration data changed by the SHV configuration user interface.</span></span> <span data-ttu-id="92597-124">Questi dati vengono importati dal computer locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="92597-124">This data is imported by the remote or local machine.</span></span>

</dd> <dt>

<span data-ttu-id="92597-125">*fConfigChanged* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="92597-125">*fConfigChanged* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92597-126">Puntatore a un **bool** che è impostato su **true** se la configurazione è stata modificata durante l'operazione dell'interfaccia utente e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="92597-126">A pointer to a **BOOL** that is set to **TRUE** if the configuration was changed during the UI operation and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92597-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="92597-127">Return value</span></span>

<span data-ttu-id="92597-128">Restituisce \_ OK se ha esito positivo o uno dei codici di errore standard di Windows.</span><span class="sxs-lookup"><span data-stu-id="92597-128">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="92597-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="92597-129">Remarks</span></span>

<span data-ttu-id="92597-130">Se usato per un computer locale, questa funzione può essere usata per la configurazione di convalida integrità di sistema per criterio.</span><span class="sxs-lookup"><span data-stu-id="92597-130">If used for a local machine, this function can be used for per policy SHV configuration.</span></span> <span data-ttu-id="92597-131">Consente di richiamare un'interfaccia utente di convalida integrità sistema e modificare una configurazione di convalida integrità di sistema esistente.</span><span class="sxs-lookup"><span data-stu-id="92597-131">It provides a way to invoke an SHV UI and edit an existing SHV configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="92597-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92597-132">Requirements</span></span>



| <span data-ttu-id="92597-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="92597-133">Requirement</span></span> | <span data-ttu-id="92597-134">Valore</span><span class="sxs-lookup"><span data-stu-id="92597-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="92597-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92597-135">Minimum supported client</span></span><br/> | <span data-ttu-id="92597-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="92597-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="92597-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92597-137">Minimum supported server</span></span><br/> | <span data-ttu-id="92597-138">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="92597-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="92597-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92597-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="92597-140"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="92597-140"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="92597-141">IDL</span><span class="sxs-lookup"><span data-stu-id="92597-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="92597-142"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="92597-142"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92597-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92597-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92597-144">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="92597-144">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





