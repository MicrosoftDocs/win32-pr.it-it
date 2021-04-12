---
description: Archivia le informazioni chiave su un'interfaccia LAN wireless gestita dal servizio di configurazione wireless.
ms.assetid: 5e689fd0-27d9-48eb-8983-96d7918be1cd
title: Struttura INTF_KEY_ENTRY (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_KEY_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: 91f25708e79be4f85c4200bd690404ff39f567d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343896"
---
# <a name="intf_key_entry-structure"></a><span data-ttu-id="29f6f-103">Struttura della voce della \_ chiave INTF \_</span><span class="sxs-lookup"><span data-stu-id="29f6f-103">INTF\_KEY\_ENTRY structure</span></span>

<span data-ttu-id="29f6f-104">\[**INTF \_ La \_ voce chiave** non è più supportata a partire da Windows Vista e windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="29f6f-104">\[**INTF\_KEY\_ENTRY** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="29f6f-105">Usare invece l' [API WiFi nativa](native-wifi-reference.md), che fornisce funzionalità simili.</span><span class="sxs-lookup"><span data-stu-id="29f6f-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="29f6f-106">Per ulteriori informazioni, vedere [informazioni sull'API WiFi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="29f6f-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="29f6f-107">La struttura della **\_ \_ voce della chiave INTF** archivia le informazioni chiave su un'interfaccia LAN wireless gestita dal servizio di configurazione wireless.</span><span class="sxs-lookup"><span data-stu-id="29f6f-107">The **INTF\_KEY\_ENTRY** structure stores the key information about a wireless LAN interface managed by the Wireless Configuration Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="29f6f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29f6f-108">Syntax</span></span>


```C++
typedef struct {
  LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;
```



## <a name="members"></a><span data-ttu-id="29f6f-109">Members</span><span class="sxs-lookup"><span data-stu-id="29f6f-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="29f6f-110">**wszGuid**</span><span class="sxs-lookup"><span data-stu-id="29f6f-110">**wszGuid**</span></span>
</dt> <dd>

<span data-ttu-id="29f6f-111">Puntatore al GUID dell'interfaccia rappresentato come stringa Unicode nel formato seguente: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span><span class="sxs-lookup"><span data-stu-id="29f6f-111">A pointer to the interface GUID represented as a Unicode string in the following format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29f6f-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="29f6f-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="29f6f-113">Il file di intestazione *wzcsapi. h* non è disponibile nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="29f6f-113">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="29f6f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29f6f-114">Requirements</span></span>



| <span data-ttu-id="29f6f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="29f6f-115">Requirement</span></span> | <span data-ttu-id="29f6f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="29f6f-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="29f6f-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29f6f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="29f6f-118">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="29f6f-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="29f6f-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29f6f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="29f6f-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="29f6f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="29f6f-121">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="29f6f-121">End of client support</span></span><br/>    | <span data-ttu-id="29f6f-122">Windows XP con SP3</span><span class="sxs-lookup"><span data-stu-id="29f6f-122">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="29f6f-123">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="29f6f-123">End of server support</span></span><br/>    | <span data-ttu-id="29f6f-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="29f6f-124">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="29f6f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29f6f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="29f6f-126"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="29f6f-126"><dt>Wzcsapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29f6f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29f6f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29f6f-128">**\_tabella della chiave INTFS \_**</span><span class="sxs-lookup"><span data-stu-id="29f6f-128">**INTFS\_KEY\_TABLE**</span></span>](intfs-key-table.md)
</dt> <dt>

[<span data-ttu-id="29f6f-129">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="29f6f-129">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> </dl>

 

 




