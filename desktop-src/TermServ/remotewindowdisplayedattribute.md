---
title: Enumerazione RemoteWindowDisplayedAttribute
description: Utilizzato con il metodo per specificare le informazioni sull'evento.
ms.assetid: 22549063-6979-48F2-AEA5-94BFC848C707
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto enumerazione RemoteWindowDisplayedAttribute
topic_type:
- apiref
api_name:
- RemoteWindowDisplayedAttribute
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a137d0ba0b6b692c949ab6c2a0c7b59b0d1fb341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301976"
---
# <a name="remotewindowdisplayedattribute-enumeration"></a><span data-ttu-id="1386d-104">Enumerazione RemoteWindowDisplayedAttribute</span><span class="sxs-lookup"><span data-stu-id="1386d-104">RemoteWindowDisplayedAttribute enumeration</span></span>

<span data-ttu-id="1386d-105">Utilizzato con il metodo per specificare le informazioni sull'evento.</span><span class="sxs-lookup"><span data-stu-id="1386d-105">Used with the method to specify information about the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="1386d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1386d-106">Syntax</span></span>


```C++
typedef enum  { 
  remoteAppWindowNone          = 0,
  remoteAppWindowDisplayed     = 1,
  remoteAppShellIconDisplayed  = 2
} RemoteWindowDisplayedAttribute;
```



## <a name="constants"></a><span data-ttu-id="1386d-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="1386d-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1386d-108"><span id="remoteAppWindowNone"></span><span id="remoteappwindownone"></span><span id="REMOTEAPPWINDOWNONE"></span>**remoteAppWindowNone**</span><span class="sxs-lookup"><span data-stu-id="1386d-108"><span id="remoteAppWindowNone"></span><span id="remoteappwindownone"></span><span id="REMOTEAPPWINDOWNONE"></span>**remoteAppWindowNone**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1386d-109"><span id="remoteAppWindowDisplayed"></span><span id="remoteappwindowdisplayed"></span><span id="REMOTEAPPWINDOWDISPLAYED"></span>**remoteAppWindowDisplayed**</span><span class="sxs-lookup"><span data-stu-id="1386d-109"><span id="remoteAppWindowDisplayed"></span><span id="remoteappwindowdisplayed"></span><span id="REMOTEAPPWINDOWDISPLAYED"></span>**remoteAppWindowDisplayed**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1386d-110"><span id="remoteAppShellIconDisplayed"></span><span id="remoteappshellicondisplayed"></span><span id="REMOTEAPPSHELLICONDISPLAYED"></span>**remoteAppShellIconDisplayed**</span><span class="sxs-lookup"><span data-stu-id="1386d-110"><span id="remoteAppShellIconDisplayed"></span><span id="remoteappshellicondisplayed"></span><span id="REMOTEAPPSHELLICONDISPLAYED"></span>**remoteAppShellIconDisplayed**</span></span>
<span data-ttu-id="1386d-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1386d-111"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="1386d-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1386d-112">Requirements</span></span>



| <span data-ttu-id="1386d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1386d-113">Requirement</span></span> | <span data-ttu-id="1386d-114">Valore</span><span class="sxs-lookup"><span data-stu-id="1386d-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1386d-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1386d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1386d-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1386d-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="1386d-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1386d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1386d-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1386d-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="1386d-119">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="1386d-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="1386d-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1386d-120"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1386d-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1386d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1386d-122">**OnRemoteWindowDisplayed**</span><span class="sxs-lookup"><span data-stu-id="1386d-122">**OnRemoteWindowDisplayed**</span></span>](imstscaxevents-onremotewindowdisplayed.md)
</dt> </dl>

 

 





