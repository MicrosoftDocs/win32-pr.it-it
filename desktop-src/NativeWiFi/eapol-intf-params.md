---
description: Contiene i parametri di configurazione avvio EAPOL.
ms.assetid: 4157a643-86f2-4f6f-8517-6207b11ea9a1
title: Struttura EAPOL_INTF_PARAMS (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPOL_INTF_PARAMS
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: dd9e0664fe41b471162beccd31bf2c22fbfa1640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313762"
---
# <a name="eapol_intf_params-structure"></a><span data-ttu-id="4e504-103">\_Struttura avvio EAPOL INTF \_ params</span><span class="sxs-lookup"><span data-stu-id="4e504-103">EAPOL\_INTF\_PARAMS structure</span></span>

<span data-ttu-id="4e504-104">\[**Avvio EAPOL \_ INTF \_ params** non è più supportato a partire da Windows Vista e windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="4e504-104">\[**EAPOL\_INTF\_PARAMS** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="4e504-105">Usare invece l' [API WiFi nativa](native-wifi-reference.md), che fornisce funzionalità simili.</span><span class="sxs-lookup"><span data-stu-id="4e504-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="4e504-106">Per ulteriori informazioni, vedere [informazioni sull'API WiFi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="4e504-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="4e504-107">Contiene i parametri di configurazione avvio EAPOL.</span><span class="sxs-lookup"><span data-stu-id="4e504-107">Contains EAPOL configuration parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e504-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e504-108">Syntax</span></span>


```C++
typedef struct _EAPOL_INTF_PARAMS {
  DWORD dwVersion;
  DWORD dwReserved2;
  DWORD dwEapFlags;
  DWORD dwEapType;
  DWORD dwSizeOfSSID;
  BYTE  bSSID[MAX_NETWORK_NAME_LENGTH];
} EAPOL_INTF_PARAMS, *PEAPOL_INTF_PARAMS;
```



## <a name="members"></a><span data-ttu-id="4e504-109">Members</span><span class="sxs-lookup"><span data-stu-id="4e504-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="4e504-110">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="4e504-110">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="4e504-111">Versione del chiamante.</span><span class="sxs-lookup"><span data-stu-id="4e504-111">Version of the caller.</span></span> <span data-ttu-id="4e504-112">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="4e504-112">Default is 0.</span></span>

</dd> <dt>

<span data-ttu-id="4e504-113">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="4e504-113">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="4e504-114">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="4e504-114">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="4e504-115">**dwEapFlags**</span><span class="sxs-lookup"><span data-stu-id="4e504-115">**dwEapFlags**</span></span>
</dt> <dd>

<span data-ttu-id="4e504-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4e504-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4e504-117">**dwEapType**</span><span class="sxs-lookup"><span data-stu-id="4e504-117">**dwEapType**</span></span>
</dt> <dd>

<span data-ttu-id="4e504-118">Tipo di estensione EAP da usare.</span><span class="sxs-lookup"><span data-stu-id="4e504-118">The EAP extension type to be used.</span></span> <span data-ttu-id="4e504-119">Impostare su 0x00000013 per EAP-TLS e 0x00000026 per PEAP.</span><span class="sxs-lookup"><span data-stu-id="4e504-119">Set to 0x00000013 for EAP-TLS and 0x00000026 for PEAP.</span></span>

</dd> <dt>

<span data-ttu-id="4e504-120">**dwSizeOfSSID**</span><span class="sxs-lookup"><span data-stu-id="4e504-120">**dwSizeOfSSID**</span></span>
</dt> <dd>

<span data-ttu-id="4e504-121">Dimensioni dell'identificatore di rete.</span><span class="sxs-lookup"><span data-stu-id="4e504-121">Size of network identifier.</span></span>

</dd> <dt>

<span data-ttu-id="4e504-122">**bSSID**</span><span class="sxs-lookup"><span data-stu-id="4e504-122">**bSSID**</span></span>
</dt> <dd>

<span data-ttu-id="4e504-123">Identificatore di rete.</span><span class="sxs-lookup"><span data-stu-id="4e504-123">Network identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e504-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e504-124">Remarks</span></span>

<span data-ttu-id="4e504-125">Il file di intestazione wzcsapi. h non è disponibile nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4e504-125">The header file wzcsapi.h is not available in the Windows SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e504-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e504-126">Requirements</span></span>



| <span data-ttu-id="4e504-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e504-127">Requirement</span></span> | <span data-ttu-id="4e504-128">Valore</span><span class="sxs-lookup"><span data-stu-id="4e504-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4e504-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e504-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4e504-130">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4e504-130">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4e504-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e504-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4e504-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4e504-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4e504-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4e504-133">End of client support</span></span><br/>    | <span data-ttu-id="4e504-134">Windows XP con SP3</span><span class="sxs-lookup"><span data-stu-id="4e504-134">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="4e504-135">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="4e504-135">End of server support</span></span><br/>    | <span data-ttu-id="4e504-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4e504-136">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="4e504-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e504-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e504-138"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e504-138"><dt>Wzcsapi.h</dt></span></span> </dl> |



 

 




