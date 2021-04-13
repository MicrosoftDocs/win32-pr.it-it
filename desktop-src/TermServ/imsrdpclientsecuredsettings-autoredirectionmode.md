---
title: Proprietà AudioRedirectionMode di IMsRdpClientSecuredSettings
description: Specifica le impostazioni di reindirizzamento audio, che specificano se reindirizzare i suoni o riprodurre suoni nel server host sessione Desktop remoto (host sessione Desktop remoto).
ms.assetid: 6aa63a50-a714-4a9b-a4ec-c0551920467a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà AudioRedirectionMode
- Servizi Desktop remoto proprietà AudioRedirectionMode, interfaccia IMsRdpClientSecuredSettings
- Interfaccia IMsRdpClientSecuredSettings Servizi Desktop remoto, proprietà AudioRedirectionMode
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.AudioRedirectionMode
- IMsRdpClientSecuredSettings.get_AudioRedirectionMode
- IMsRdpClientSecuredSettings.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 858342811ec97def95031ebed0605b5a81cf80fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519229"
---
# <a name="imsrdpclientsecuredsettingsaudioredirectionmode-property"></a><span data-ttu-id="2d8d2-106">Proprietà IMsRdpClientSecuredSettings:: AudioRedirectionMode</span><span class="sxs-lookup"><span data-stu-id="2d8d2-106">IMsRdpClientSecuredSettings::AudioRedirectionMode property</span></span>

<span data-ttu-id="2d8d2-107">Specifica le impostazioni di reindirizzamento audio, che specificano se reindirizzare i suoni o riprodurre suoni nel server host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="2d8d2-107">Specifies the audio redirection settings, which specify whether to redirect sounds or play sounds at the Remote Desktop Session Host (RD Session Host) server.</span></span>

<span data-ttu-id="2d8d2-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2d8d2-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d8d2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d8d2-109">Syntax</span></span>


```C++
HRESULT put_AudioRedirectionMode(
  [in]  LONG audioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] LONG *paudioRedirectionMode
);
```



## <a name="property-value"></a><span data-ttu-id="2d8d2-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2d8d2-110">Property value</span></span>

<span data-ttu-id="2d8d2-111">Nuove impostazioni.</span><span class="sxs-lookup"><span data-stu-id="2d8d2-111">The new settings.</span></span> <span data-ttu-id="2d8d2-112">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2d8d2-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="2d8d2-113">0</span><span class="sxs-lookup"><span data-stu-id="2d8d2-113">0</span></span>
</dt> <dd>

<span data-ttu-id="2d8d2-114">Reindirizza i suoni al client.</span><span class="sxs-lookup"><span data-stu-id="2d8d2-114">Redirect sounds to the client.</span></span> <span data-ttu-id="2d8d2-115">Rappresenta il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="2d8d2-115">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="2d8d2-116">1</span><span class="sxs-lookup"><span data-stu-id="2d8d2-116">1</span></span>
</dt> <dd>

<span data-ttu-id="2d8d2-117">Riprodurre suoni nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="2d8d2-117">Play sounds at the remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="2d8d2-118">2</span><span class="sxs-lookup"><span data-stu-id="2d8d2-118">2</span></span>
</dt> <dd>

<span data-ttu-id="2d8d2-119">Disabilitare il reindirizzamento del suono; non riprodurre suoni sul server.</span><span class="sxs-lookup"><span data-stu-id="2d8d2-119">Disable sound redirection; do not play sounds at the server.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="2d8d2-120">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="2d8d2-120">Error codes</span></span>

<span data-ttu-id="2d8d2-121">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2d8d2-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d8d2-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d8d2-122">Remarks</span></span>

<span data-ttu-id="2d8d2-123">Non è possibile impostare queste proprietà quando il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="2d8d2-123">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="2d8d2-124">Per ulteriori informazioni, vedere [la pagina relativa alla sicurezza dei client RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="2d8d2-124">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="2d8d2-125">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="2d8d2-125">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d8d2-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d8d2-126">Requirements</span></span>



| <span data-ttu-id="2d8d2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d8d2-127">Requirement</span></span> | <span data-ttu-id="2d8d2-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2d8d2-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d8d2-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d8d2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2d8d2-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d8d2-130">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="2d8d2-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d8d2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2d8d2-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d8d2-132">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="2d8d2-133">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2d8d2-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="2d8d2-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d8d2-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="2d8d2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2d8d2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d8d2-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d8d2-136"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="2d8d2-137">IID</span><span class="sxs-lookup"><span data-stu-id="2d8d2-137">IID</span></span><br/>                      | <span data-ttu-id="2d8d2-138">IID \_ IMsRdpClientSecuredSettings è definito come 605befcf-39c1-45cc-A811-068fb7be346d</span><span class="sxs-lookup"><span data-stu-id="2d8d2-138">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2d8d2-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d8d2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d8d2-140">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="2d8d2-140">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





