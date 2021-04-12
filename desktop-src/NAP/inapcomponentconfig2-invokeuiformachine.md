---
title: Metodo INapComponentConfig2 InvokeUIForMachine (NapCommon. h)
description: Viene implementato da convalida integrità sistema (SHV) in base alle esigenze per gestire la configurazione remota direttamente nel computer specificato. Questo metodo avvia un'interfaccia utente di gestione della configurazione.
ms.assetid: 67a6d715-250b-4b8b-9c27-8173926b7bfe
keywords:
- NAP metodo InvokeUIForMachine
- Metodo InvokeUIForMachine NAP, interfaccia INapComponentConfig2
- Interfaccia INapComponentConfig2 NAP, metodo InvokeUIForMachine
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIForMachine
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bc0c09f802a63a5bfad92b49f76fcbb4ee242d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119646"
---
# <a name="inapcomponentconfig2invokeuiformachine-method"></a><span data-ttu-id="06304-107">Metodo INapComponentConfig2:: InvokeUIForMachine</span><span class="sxs-lookup"><span data-stu-id="06304-107">INapComponentConfig2::InvokeUIForMachine method</span></span>

> [!Note]  
> <span data-ttu-id="06304-108">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="06304-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="06304-109">Il metodo **InvokeUIForMachine** viene implementato da convalida integrità sistema (SHV) in base alle esigenze per gestire la configurazione remota direttamente nel computer specificato.</span><span class="sxs-lookup"><span data-stu-id="06304-109">The **InvokeUIForMachine** method is implemented by system health validators (SHVs) as needed to manage remote configuration directly on the machine specified.</span></span> <span data-ttu-id="06304-110">Questo metodo avvia un'interfaccia utente di gestione della configurazione.</span><span class="sxs-lookup"><span data-stu-id="06304-110">This method launches a configuration management UI.</span></span>

## <a name="syntax"></a><span data-ttu-id="06304-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06304-111">Syntax</span></span>


```C++
HRESULT InvokeUIForMachine(
  [in] HWND          hwndParent,
  [in] CountedString *machineName
);
```



## <a name="parameters"></a><span data-ttu-id="06304-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="06304-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06304-113">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06304-113">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06304-114">Handle per la finestra padre o proprietario.</span><span class="sxs-lookup"><span data-stu-id="06304-114">A handle to the parent or owner window.</span></span> <span data-ttu-id="06304-115">È necessario specificare un handle di finestra valido.</span><span class="sxs-lookup"><span data-stu-id="06304-115">A valid window handle must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="06304-116">*nomecomputer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06304-116">*machineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06304-117">Puntatore a un [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) contenente il nome del computer del client di protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="06304-117">A pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) that contains the machine name of the NAP client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06304-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06304-118">Return value</span></span>

<span data-ttu-id="06304-119">Restituisce \_ OK se ha esito positivo o uno dei codici di errore standard di Windows.</span><span class="sxs-lookup"><span data-stu-id="06304-119">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="06304-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06304-120">Requirements</span></span>



| <span data-ttu-id="06304-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="06304-121">Requirement</span></span> | <span data-ttu-id="06304-122">Valore</span><span class="sxs-lookup"><span data-stu-id="06304-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="06304-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06304-123">Minimum supported client</span></span><br/> | <span data-ttu-id="06304-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="06304-124">None supported</span></span><br/>                                                                |
| <span data-ttu-id="06304-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06304-125">Minimum supported server</span></span><br/> | <span data-ttu-id="06304-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="06304-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="06304-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06304-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="06304-128"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="06304-128"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="06304-129">IDL</span><span class="sxs-lookup"><span data-stu-id="06304-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="06304-130"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="06304-130"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06304-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06304-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06304-132">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="06304-132">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





