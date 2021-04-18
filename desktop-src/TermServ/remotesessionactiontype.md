---
title: Enumerazione RemoteSessionActionType
description: Utilizzato per specificare il tipo di azione remota.
ms.assetid: C0DA0FA2-6FE0-4B40-B169-4592A1BE2AD6
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto enumerazione RemoteSessionActionType
topic_type:
- apiref
api_name:
- RemoteSessionActionType
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 291bb9fdd2cadfef3881bc27a47f9fc1bb1bce68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301296"
---
# <a name="remotesessionactiontype-enumeration"></a><span data-ttu-id="7f03b-104">Enumerazione RemoteSessionActionType</span><span class="sxs-lookup"><span data-stu-id="7f03b-104">RemoteSessionActionType enumeration</span></span>

<span data-ttu-id="7f03b-105">Utilizzato per specificare il tipo di azione remota.</span><span class="sxs-lookup"><span data-stu-id="7f03b-105">Used to specify the type of remote action.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f03b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f03b-106">Syntax</span></span>


```C++
typedef enum _RemoteSessionActionType { 
  RemoteSessionActionCharms        = 0,
  RemoteSessionActionAppbar        = 1,
  RemoteSessionActionSnap          = 2,
  RemoteSessionActionStartScreen   = 3,
  RemoteSessionActionAppSwitch     = 4,
  RemoteSessionActionActionCenter  = 4
} RemoteSessionActionType;
```



## <a name="constants"></a><span data-ttu-id="7f03b-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="7f03b-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7f03b-108"><span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**RemoteSessionActionCharms**</span><span class="sxs-lookup"><span data-stu-id="7f03b-108"><span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**RemoteSessionActionCharms**</span></span>
</dt> <dd>

<span data-ttu-id="7f03b-109">Visualizza gli accessi nella sessione remota.</span><span class="sxs-lookup"><span data-stu-id="7f03b-109">Displays the charms in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="7f03b-110"><span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**RemoteSessionActionAppbar**</span><span class="sxs-lookup"><span data-stu-id="7f03b-110"><span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**RemoteSessionActionAppbar**</span></span>
</dt> <dd>

<span data-ttu-id="7f03b-111">Visualizza la barra dell'app nella sessione remota.</span><span class="sxs-lookup"><span data-stu-id="7f03b-111">Displays the app bar in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="7f03b-112"><span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**RemoteSessionActionSnap**</span><span class="sxs-lookup"><span data-stu-id="7f03b-112"><span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**RemoteSessionActionSnap**</span></span>
</dt> <dd>

<span data-ttu-id="7f03b-113">Ancora l'applicazione nella sessione remota.</span><span class="sxs-lookup"><span data-stu-id="7f03b-113">Docks the application in the remote session.</span></span> <span data-ttu-id="7f03b-114">Questa opzione è stata deprecata e non deve essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7f03b-114">This option has been deprecated and should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="7f03b-115"><span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**RemoteSessionActionStartScreen**</span><span class="sxs-lookup"><span data-stu-id="7f03b-115"><span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**RemoteSessionActionStartScreen**</span></span>
</dt> <dd>

<span data-ttu-id="7f03b-116">Determina la visualizzazione della schermata iniziale nella sessione remota.</span><span class="sxs-lookup"><span data-stu-id="7f03b-116">Causes the start screen to be displayed in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="7f03b-117"><span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**RemoteSessionActionAppSwitch**</span><span class="sxs-lookup"><span data-stu-id="7f03b-117"><span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**RemoteSessionActionAppSwitch**</span></span>
</dt> <dd>

<span data-ttu-id="7f03b-118">Determina la visualizzazione della finestra del commutire dell'applicazione nella sessione remota.</span><span class="sxs-lookup"><span data-stu-id="7f03b-118">Causes the application switch window to be displayed in the remote session.</span></span> <span data-ttu-id="7f03b-119">Si tratta dello stesso utente che preme ALT + TAB.</span><span class="sxs-lookup"><span data-stu-id="7f03b-119">This is the same as the user pressing Alt+Tab.</span></span>

</dd> <dt>

<span data-ttu-id="7f03b-120"><span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**RemoteSessionActionActionCenter**</span><span class="sxs-lookup"><span data-stu-id="7f03b-120"><span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**RemoteSessionActionActionCenter**</span></span>
</dt> <dd>

<span data-ttu-id="7f03b-121">Determina la visualizzazione del centro operativo nella sessione remota.</span><span class="sxs-lookup"><span data-stu-id="7f03b-121">Causes the Action Center to be displayed in the remote session.</span></span> <span data-ttu-id="7f03b-122">Si tratta dello stesso utente che preme Win + A.</span><span class="sxs-lookup"><span data-stu-id="7f03b-122">This is the same as the user pressing Win+A.</span></span>

<span data-ttu-id="7f03b-123">**Windows server 2012 R2, Windows 8.1, Windows server 2012 e Windows 8:** Questo valore non è supportato prima di Windows Server 2016 e Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7f03b-123">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012 and Windows 8:** This value is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7f03b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f03b-124">Requirements</span></span>



| <span data-ttu-id="7f03b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f03b-125">Requirement</span></span> | <span data-ttu-id="7f03b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="7f03b-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f03b-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f03b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7f03b-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7f03b-128">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="7f03b-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f03b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7f03b-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7f03b-130">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="7f03b-131">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="7f03b-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="7f03b-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f03b-132"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f03b-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f03b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f03b-134">**IMsRdpClient8::SendRemoteAction**</span><span class="sxs-lookup"><span data-stu-id="7f03b-134">**IMsRdpClient8::SendRemoteAction**</span></span>](imsrdpclient8-sendremoteaction.md)
</dt> </dl>

 

 





