---
description: Proprietà PKEY \_ deviceinterface \_ FriendlyName.
ms.assetid: beef2153-489f-4ff5-a161-b4e2cd4ac1fa
title: PKEY_DeviceInterface_FriendlyName (Functiondiscoverykeys \_ devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7590e9254e336bf9dbfe0fdeb3349bf19c0b8c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125757"
---
# <a name="pkey_deviceinterface_friendlyname"></a><span data-ttu-id="c216f-103">PKEY \_ deviceinterface \_ FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c216f-103">PKEY\_DeviceInterface\_FriendlyName</span></span>

<span data-ttu-id="c216f-104">La proprietà **pkey \_ deviceinterface \_ FriendlyName** contiene il nome descrittivo della scheda audio a cui è collegato il dispositivo endpoint (ad esempio, "scheda audio XYZ").</span><span class="sxs-lookup"><span data-stu-id="c216f-104">The **PKEY\_DeviceInterface\_FriendlyName** property contains the friendly name of the audio adapter to which the endpoint device is attached (for example, "XYZ Audio Adapter").</span></span>

<span data-ttu-id="c216f-105">Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="c216f-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="c216f-106">Il membro **pwszVal** della struttura **PROPVARIANT** punta a una stringa di caratteri wide con terminazione null che contiene il nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="c216f-106">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains the friendly name.</span></span>

## <a name="requirements"></a><span data-ttu-id="c216f-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c216f-107">Requirements</span></span>



| <span data-ttu-id="c216f-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="c216f-108">Requirement</span></span> | <span data-ttu-id="c216f-109">Valore</span><span class="sxs-lookup"><span data-stu-id="c216f-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c216f-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c216f-110">Minimum supported client</span></span><br/> | <span data-ttu-id="c216f-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c216f-111">Windows Vista \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c216f-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c216f-112">Minimum supported server</span></span><br/> | <span data-ttu-id="c216f-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c216f-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="c216f-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c216f-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="c216f-115"><dt>Functiondiscoverykeys \_ devpkey. h</dt></span><span class="sxs-lookup"><span data-stu-id="c216f-115"><dt>Functiondiscoverykeys\_devpkey.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c216f-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c216f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c216f-117">Proprietà audio principali</span><span class="sxs-lookup"><span data-stu-id="c216f-117">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="c216f-118">Proprietà dispositivo</span><span class="sxs-lookup"><span data-stu-id="c216f-118">Device Properties</span></span>](device-properties.md)
</dt> </dl>

 

 




