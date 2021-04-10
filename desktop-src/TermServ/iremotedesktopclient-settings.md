---
title: Proprietà delle impostazioni IRemoteDesktopClient
description: Recupera l'oggetto impostazioni per il client contenitore di app Remote Desktop Protocol (RDP).
ms.assetid: 59999489-9ad0-4b85-9643-3b8355b817c2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto della proprietà Settings
- Servizi Desktop remoto delle proprietà Settings, interfaccia IRemoteDesktopClient
- Servizi Desktop remoto di interfaccia IRemoteDesktopClient, proprietà Settings
topic_type:
- apiref
api_name:
- IRemoteDesktopClient.Settings
- IRemoteDesktopClient.get_Settings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e84324eaa12610d7ab898cbcb181e7712bc021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964504"
---
# <a name="iremotedesktopclientsettings-property"></a><span data-ttu-id="2cb33-106">Proprietà IRemoteDesktopClient:: Settings</span><span class="sxs-lookup"><span data-stu-id="2cb33-106">IRemoteDesktopClient::Settings property</span></span>

<span data-ttu-id="2cb33-107">Recupera l'oggetto impostazioni per il client contenitore di app Remote Desktop Protocol (RDP).</span><span class="sxs-lookup"><span data-stu-id="2cb33-107">Retrieves the settings object for the Remote Desktop Protocol (RDP) app container client.</span></span>

<span data-ttu-id="2cb33-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2cb33-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cb33-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2cb33-109">Syntax</span></span>


```C++
HRESULT get_Settings(
  [out, retval] IRemoteDesktopClientSettings **Settings
);
```



## <a name="property-value"></a><span data-ttu-id="2cb33-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2cb33-110">Property value</span></span>

<span data-ttu-id="2cb33-111">Oggetto impostazioni per il client RDP.</span><span class="sxs-lookup"><span data-stu-id="2cb33-111">The settings object for the RDP client.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cb33-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cb33-112">Requirements</span></span>



| <span data-ttu-id="2cb33-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cb33-113">Requirement</span></span> | <span data-ttu-id="2cb33-114">Valore</span><span class="sxs-lookup"><span data-stu-id="2cb33-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cb33-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cb33-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2cb33-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2cb33-116">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="2cb33-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cb33-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2cb33-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2cb33-118">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="2cb33-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2cb33-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="2cb33-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cb33-120"><dt>MsTscAx.dll</dt></span></span> </dl>  |
| <span data-ttu-id="2cb33-121">DLL</span><span class="sxs-lookup"><span data-stu-id="2cb33-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cb33-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cb33-122"><dt>MsTscAx.dll</dt></span></span> </dl>  |
| <span data-ttu-id="2cb33-123">IID</span><span class="sxs-lookup"><span data-stu-id="2cb33-123">IID</span></span><br/>                      | <span data-ttu-id="2cb33-124">IID \_ IRemoteDesktopClient è definito come 57D25668-625A-4905-BE4E-304CAA13F89C</span><span class="sxs-lookup"><span data-stu-id="2cb33-124">IID\_IRemoteDesktopClient is defined as 57D25668-625A-4905-BE4E-304CAA13F89C</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2cb33-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2cb33-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cb33-126">**IRemoteDesktopClient**</span><span class="sxs-lookup"><span data-stu-id="2cb33-126">**IRemoteDesktopClient**</span></span>](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
</dt> </dl>

 

