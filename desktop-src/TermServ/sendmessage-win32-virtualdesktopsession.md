---
title: Metodo SendMessage della classe Win32_VirtualDesktopSession
description: Inviare un messaggio all'utente tramite la sessione desktop virtuale.
ms.assetid: 4bb9183e-c016-48f2-8e8c-0d5fb395c435
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SendMessage
- Servizi Desktop remoto del metodo SendMessage, classe Win32_VirtualDesktopSession
- Classe Win32_VirtualDesktopSession Servizi Desktop remoto, metodo SendMessage
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.SendMessage
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e3e72f5c401b8cbb0e5e5de45f594d61af6275
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400581"
---
# <a name="sendmessage-method-of-the-win32_virtualdesktopsession-class"></a><span data-ttu-id="8edd3-106">Metodo SendMessage della \_ classe VirtualDesktopSession Win32</span><span class="sxs-lookup"><span data-stu-id="8edd3-106">SendMessage method of the Win32\_VirtualDesktopSession class</span></span>

<span data-ttu-id="8edd3-107">Inviare un messaggio all'utente tramite la sessione desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="8edd3-107">Send a message to the user through the virtual desktop session.</span></span>

## <a name="syntax"></a><span data-ttu-id="8edd3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8edd3-108">Syntax</span></span>


```mof
uint32 SendMessage(
  [in] string Title,
  [in] string Message
);
```



## <a name="parameters"></a><span data-ttu-id="8edd3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8edd3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8edd3-110">*Titolo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8edd3-110">*Title* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8edd3-111">Titolo del dei.</span><span class="sxs-lookup"><span data-stu-id="8edd3-111">The title of the messge.</span></span>

</dd> <dt>

<span data-ttu-id="8edd3-112">*Messaggio* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8edd3-112">*Message* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8edd3-113">Contenuto del messaggio.</span><span class="sxs-lookup"><span data-stu-id="8edd3-113">The content of the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8edd3-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8edd3-114">Return value</span></span>

<span data-ttu-id="8edd3-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="8edd3-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8edd3-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8edd3-116">Requirements</span></span>



| <span data-ttu-id="8edd3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8edd3-117">Requirement</span></span> | <span data-ttu-id="8edd3-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8edd3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8edd3-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8edd3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8edd3-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8edd3-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="8edd3-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8edd3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8edd3-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8edd3-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="8edd3-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8edd3-123">Namespace</span></span><br/>                | <span data-ttu-id="8edd3-124">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="8edd3-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="8edd3-125">MOF</span><span class="sxs-lookup"><span data-stu-id="8edd3-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8edd3-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8edd3-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="8edd3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8edd3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8edd3-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8edd3-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="8edd3-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8edd3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8edd3-130">**\_VirtualDesktopSession Win32**</span><span class="sxs-lookup"><span data-stu-id="8edd3-130">**Win32\_VirtualDesktopSession**</span></span>](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





