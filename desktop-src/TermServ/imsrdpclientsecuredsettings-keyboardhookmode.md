---
title: Proprietà KeyboardHookMode di IMsRdpClientSecuredSettings
description: Specifica le impostazioni di Reindirizzamento da tastiera, che specificano come e quando applicare il tasto di scelta rapida di Windows, ad esempio ALT + TAB.
ms.assetid: 16734580-9be9-476b-b8e7-1eca3ba24d61
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà KeyboardHookMode
- Servizi Desktop remoto proprietà KeyboardHookMode, interfaccia IMsRdpClientSecuredSettings
- Interfaccia IMsRdpClientSecuredSettings Servizi Desktop remoto, proprietà KeyboardHookMode
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.KeyboardHookMode
- IMsRdpClientSecuredSettings.get_KeyboardHookMode
- IMsRdpClientSecuredSettings.put_KeyboardHookMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 948069b689d8799a98805148017a204b719d7645
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400442"
---
# <a name="imsrdpclientsecuredsettingskeyboardhookmode-property"></a><span data-ttu-id="01060-106">Proprietà IMsRdpClientSecuredSettings:: KeyboardHookMode</span><span class="sxs-lookup"><span data-stu-id="01060-106">IMsRdpClientSecuredSettings::KeyboardHookMode property</span></span>

<span data-ttu-id="01060-107">Specifica le impostazioni di Reindirizzamento da tastiera, che specificano come e quando applicare il tasto di scelta rapida di Windows, ad esempio ALT + TAB.</span><span class="sxs-lookup"><span data-stu-id="01060-107">Specifies the keyboard redirection settings, which specify how and when to apply Windows keyboard shortcut (for example, ALT+TAB).</span></span>

<span data-ttu-id="01060-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="01060-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="01060-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01060-109">Syntax</span></span>


```C++
HRESULT put_KeyboardHookMode(
  [in]  LONG keyboardHookMode
);

HRESULT get_KeyboardHookMode(
  [out] LONG *pkeyboardHookMode
);
```



## <a name="property-value"></a><span data-ttu-id="01060-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="01060-110">Property value</span></span>

<span data-ttu-id="01060-111">Nuove impostazioni.</span><span class="sxs-lookup"><span data-stu-id="01060-111">The new settings.</span></span> <span data-ttu-id="01060-112">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="01060-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="01060-113">0</span><span class="sxs-lookup"><span data-stu-id="01060-113">0</span></span>
</dt> <dd>

<span data-ttu-id="01060-114">Applicare le combinazioni di tasti solo localmente nel computer client.</span><span class="sxs-lookup"><span data-stu-id="01060-114">Apply key combinations only locally at the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="01060-115">1</span><span class="sxs-lookup"><span data-stu-id="01060-115">1</span></span>
</dt> <dd>

<span data-ttu-id="01060-116">Applicare le combinazioni di tasti al server remoto.</span><span class="sxs-lookup"><span data-stu-id="01060-116">Apply key combinations at the remote server.</span></span>

</dd> <dt>

<span data-ttu-id="01060-117">2</span><span class="sxs-lookup"><span data-stu-id="01060-117">2</span></span>
</dt> <dd>

<span data-ttu-id="01060-118">Applicare le combinazioni di tasti al server remoto solo quando il client è in esecuzione in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="01060-118">Apply key combinations to the remote server only when the client is running in full-screen mode.</span></span> <span data-ttu-id="01060-119">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="01060-119">This is the default value.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="01060-120">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="01060-120">Error codes</span></span>

<span data-ttu-id="01060-121">Restituisce **\_ OK** se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="01060-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="01060-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="01060-122">Remarks</span></span>

<span data-ttu-id="01060-123">Non è possibile impostare queste proprietà quando il controllo è connesso.</span><span class="sxs-lookup"><span data-stu-id="01060-123">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="01060-124">Per ulteriori informazioni, vedere [la pagina relativa alla sicurezza dei client RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="01060-124">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="01060-125">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="01060-125">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01060-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01060-126">Requirements</span></span>



| <span data-ttu-id="01060-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="01060-127">Requirement</span></span> | <span data-ttu-id="01060-128">Valore</span><span class="sxs-lookup"><span data-stu-id="01060-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01060-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01060-129">Minimum supported client</span></span><br/> | <span data-ttu-id="01060-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01060-130">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="01060-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01060-131">Minimum supported server</span></span><br/> | <span data-ttu-id="01060-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01060-132">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="01060-133">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="01060-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="01060-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01060-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="01060-135">DLL</span><span class="sxs-lookup"><span data-stu-id="01060-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01060-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01060-136"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="01060-137">IID</span><span class="sxs-lookup"><span data-stu-id="01060-137">IID</span></span><br/>                      | <span data-ttu-id="01060-138">IID \_ IMsRdpClientSecuredSettings è definito come 605befcf-39c1-45cc-A811-068fb7be346d</span><span class="sxs-lookup"><span data-stu-id="01060-138">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01060-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01060-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01060-140">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="01060-140">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





