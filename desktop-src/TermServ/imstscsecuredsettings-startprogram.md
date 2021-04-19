---
title: Proprietà StartProgram di IMsTscSecuredSettings
description: Specifica il programma da avviare sul server remoto alla connessione.
ms.assetid: bd2a5ced-468b-48db-ad51-9940577a0310
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Proprietà StartProgram
- Servizi Desktop remoto Proprietà StartProgram, interfaccia IMsTscSecuredSettings
- Interfaccia IMsTscSecuredSettings Servizi Desktop remoto, proprietà StartProgram
- Servizi Desktop remoto Proprietà StartProgram, interfaccia IMsRdpClientSecuredSettings
- Interfaccia IMsRdpClientSecuredSettings Servizi Desktop remoto, proprietà StartProgram
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.StartProgram
- IMsTscSecuredSettings.get_StartProgram
- IMsTscSecuredSettings.put_StartProgram
- IMsRdpClientSecuredSettings.StartProgram
- IMsRdpClientSecuredSettings.get_StartProgram
- IMsRdpClientSecuredSettings.put_StartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e79612855117f48e629e9a06246f3fad922d37f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302611"
---
# <a name="imstscsecuredsettingsstartprogram-property"></a><span data-ttu-id="d3f3e-108">Proprietà IMsTscSecuredSettings:: StartProgram</span><span class="sxs-lookup"><span data-stu-id="d3f3e-108">IMsTscSecuredSettings::StartProgram property</span></span>

<span data-ttu-id="d3f3e-109">Specifica il programma da avviare sul server remoto alla connessione.</span><span class="sxs-lookup"><span data-stu-id="d3f3e-109">Specifies the program to be started on the remote server upon connection.</span></span>

<span data-ttu-id="d3f3e-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d3f3e-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3f3e-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3f3e-111">Syntax</span></span>


```C++
HRESULT put_StartProgram(
  [in]  BSTR newVal
);

HRESULT get_StartProgram(
  [out] BSTR *pStartProgram
);
```



## <a name="property-value"></a><span data-ttu-id="d3f3e-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d3f3e-112">Property value</span></span>

<span data-ttu-id="d3f3e-113">Nome del nuovo programma di avvio.</span><span class="sxs-lookup"><span data-stu-id="d3f3e-113">The name of the new start program.</span></span> <span data-ttu-id="d3f3e-114">La lunghezza massima di questa stringa è **Max \_ path**-1 caratteri.</span><span class="sxs-lookup"><span data-stu-id="d3f3e-114">The maximum length of this string is **MAX\_PATH**-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d3f3e-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d3f3e-115">Error codes</span></span>

<span data-ttu-id="d3f3e-116">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d3f3e-116">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3f3e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3f3e-117">Remarks</span></span>

<span data-ttu-id="d3f3e-118">Se il valore di questa proprietà non è impostato, verrà eseguito il comando della shell dell'utente della sessione.</span><span class="sxs-lookup"><span data-stu-id="d3f3e-118">If the value of this property is not set, the session user's shell command will be run.</span></span> <span data-ttu-id="d3f3e-119">Il comando della shell verrà letto dal seguente valore del registro di sistema nel server:</span><span class="sxs-lookup"><span data-stu-id="d3f3e-119">The shell command will be read from the following registry value on the server:</span></span>

<span data-ttu-id="d3f3e-120">**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **Shell**</span><span class="sxs-lookup"><span data-stu-id="d3f3e-120">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**WinLogon**\\**Shell**</span></span>

<span data-ttu-id="d3f3e-121">Per ulteriori informazioni, vedere [la pagina relativa alla sicurezza dei client RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="d3f3e-121">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="d3f3e-122">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d3f3e-122">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3f3e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3f3e-123">Requirements</span></span>



| <span data-ttu-id="d3f3e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3f3e-124">Requirement</span></span> | <span data-ttu-id="d3f3e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d3f3e-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f3e-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3f3e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d3f3e-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3f3e-127">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="d3f3e-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3f3e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d3f3e-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3f3e-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d3f3e-130">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d3f3e-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="d3f3e-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3f3e-131"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="d3f3e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d3f3e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3f3e-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3f3e-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="d3f3e-134">IID</span><span class="sxs-lookup"><span data-stu-id="d3f3e-134">IID</span></span><br/>                      | <span data-ttu-id="d3f3e-135">IID \_ IMsTscSecuredSettings è definito come c9d65442-A0F9-45b2-8f73-d61d2db8cbb6</span><span class="sxs-lookup"><span data-stu-id="d3f3e-135">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3f3e-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3f3e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3f3e-137">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="d3f3e-137">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d3f3e-138">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="d3f3e-138">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





