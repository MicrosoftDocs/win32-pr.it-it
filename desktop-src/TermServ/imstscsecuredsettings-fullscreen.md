---
title: Proprietà IMsTscSecuredSettings fullscreen
description: Specifica lo stato a schermo intero del controllo client.
ms.assetid: f65c2fa3-b2d0-4e64-bf1e-08394c91eda8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà a schermo intero
- Servizi Desktop remoto proprietà FullScreen, interfaccia IMsTscSecuredSettings
- Interfaccia IMsTscSecuredSettings Servizi Desktop remoto, proprietà FullScreen
- Servizi Desktop remoto proprietà FullScreen, interfaccia IMsRdpClientSecuredSettings
- Interfaccia IMsRdpClientSecuredSettings Servizi Desktop remoto, proprietà FullScreen
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.Fullscreen
- IMsTscSecuredSettings.get_Fullscreen
- IMsTscSecuredSettings.put_Fullscreen
- IMsRdpClientSecuredSettings.Fullscreen
- IMsRdpClientSecuredSettings.get_Fullscreen
- IMsRdpClientSecuredSettings.put_Fullscreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c3b3208edf3476fcd110d7729d97d9817cb929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302458"
---
# <a name="imstscsecuredsettingsfullscreen-property"></a><span data-ttu-id="395ff-108">Proprietà IMsTscSecuredSettings:: fullscreen</span><span class="sxs-lookup"><span data-stu-id="395ff-108">IMsTscSecuredSettings::Fullscreen property</span></span>

<span data-ttu-id="395ff-109">Specifica lo stato a schermo intero del controllo client.</span><span class="sxs-lookup"><span data-stu-id="395ff-109">Specifies the full-screen state of the client control.</span></span>

<span data-ttu-id="395ff-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="395ff-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="395ff-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="395ff-111">Syntax</span></span>


```C++
HRESULT put_Fullscreen(
  [in]  BOOL fFullScreen
);

HRESULT get_Fullscreen(
  [out] BOOL *pfFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="395ff-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="395ff-112">Property value</span></span>

<span data-ttu-id="395ff-113">Impostare questo parametro su **true** se il controllo deve utilizzare la modalità a schermo intero e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="395ff-113">Set this parameter to **TRUE** if the control should use full-screen mode and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="395ff-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="395ff-114">Error codes</span></span>

<span data-ttu-id="395ff-115">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="395ff-115">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="395ff-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="395ff-116">Remarks</span></span>

<span data-ttu-id="395ff-117">Per ulteriori informazioni su questo metodo, vedere la pagina [relativa alla sicurezza dei client RDP](providing-for-rdp-client-security.md).</span><span class="sxs-lookup"><span data-stu-id="395ff-117">For more information about this method, see [Providing for RDP Client Security](providing-for-rdp-client-security.md).</span></span>

<span data-ttu-id="395ff-118">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="395ff-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

<span data-ttu-id="395ff-119">Si noti che anche se l'uso di questa proprietà è limitato alle zone di sicurezza URL di Internet Explorer consentite, un utente può sempre passare alla modalità schermo intero dopo che la connessione è stata stabilita premendo la combinazione di [tasti di scelta rapida](terminal-services-shortcut-keys.md) per la modalità schermo intero (CTRL + ALT + INTERR).</span><span class="sxs-lookup"><span data-stu-id="395ff-119">Note that although the use of this property is restricted to the allowed Internet Explorer URL security zones, a user can always change to full-screen mode after the connection has been established by pressing the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

<span data-ttu-id="395ff-120">Questo metodo può essere chiamato mentre viene stabilita la connessione client.</span><span class="sxs-lookup"><span data-stu-id="395ff-120">This method can be called while the client connection is established.</span></span>

<span data-ttu-id="395ff-121">È necessario chiamare il metodo [**IMsRdpClientNonScriptable3::p UT \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) prima di chiamare il metodo **IMsTscSecuredSettings::P UT \_ FullScreen** o [**IMsRdpClient::p UT \_ FullScreen**](imsrdpclient-fullscreen.md) .</span><span class="sxs-lookup"><span data-stu-id="395ff-121">You must call the [**IMsRdpClientNonScriptable3::put\_ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) method before you call the **IMsTscSecuredSettings::put\_Fullscreen** method or the [**IMsRdpClient::put\_Fullscreen**](imsrdpclient-fullscreen.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="395ff-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="395ff-122">Requirements</span></span>



| <span data-ttu-id="395ff-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="395ff-123">Requirement</span></span> | <span data-ttu-id="395ff-124">Valore</span><span class="sxs-lookup"><span data-stu-id="395ff-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="395ff-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="395ff-125">Minimum supported client</span></span><br/> | <span data-ttu-id="395ff-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="395ff-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="395ff-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="395ff-127">Minimum supported server</span></span><br/> | <span data-ttu-id="395ff-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="395ff-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="395ff-129">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="395ff-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="395ff-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="395ff-130"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="395ff-131">DLL</span><span class="sxs-lookup"><span data-stu-id="395ff-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="395ff-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="395ff-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="395ff-133">IID</span><span class="sxs-lookup"><span data-stu-id="395ff-133">IID</span></span><br/>                      | <span data-ttu-id="395ff-134">IID \_ IMsTscSecuredSettings è definito come c9d65442-A0F9-45b2-8f73-d61d2db8cbb6</span><span class="sxs-lookup"><span data-stu-id="395ff-134">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="395ff-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="395ff-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="395ff-136">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="395ff-136">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="395ff-137">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="395ff-137">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





