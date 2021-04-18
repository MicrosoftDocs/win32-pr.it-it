---
description: Contiene la tabella delle informazioni chiave per tutte le interfacce LAN wireless gestite dal servizio di configurazione wireless.
ms.assetid: 5d5fe222-6ca1-4778-9f64-1c6a63467a6c
title: Struttura INTFS_KEY_TABLE (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTFS_KEY_TABLE
api_type:
- HeaderDef
api_location:
- Wzcsapi.h
ms.openlocfilehash: 4ef38f2317c763eaa6c7e0379be5c8b00c0ed6b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307835"
---
# <a name="intfs_key_table-structure"></a><span data-ttu-id="670b5-103">Struttura della tabella della \_ chiave INTFS \_</span><span class="sxs-lookup"><span data-stu-id="670b5-103">INTFS\_KEY\_TABLE structure</span></span>

<span data-ttu-id="670b5-104">\[**INTFS \_ La \_ tabella delle chiavi** non è più supportata a partire da Windows Vista e windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="670b5-104">\[**INTFS\_KEY\_TABLE** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="670b5-105">Usare invece l' [API WiFi nativa](native-wifi-reference.md), che fornisce funzionalità simili.</span><span class="sxs-lookup"><span data-stu-id="670b5-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="670b5-106">Per ulteriori informazioni, vedere [informazioni sull'API WiFi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="670b5-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="670b5-107">La struttura della **\_ \_ tabella della chiave INTFS** contiene la tabella delle informazioni chiave per tutte le interfacce LAN wireless gestite dal servizio di configurazione wireless.</span><span class="sxs-lookup"><span data-stu-id="670b5-107">The **INTFS\_KEY\_TABLE** structure contains the table of key information for all wireless LAN interfaces managed by the Wireless Configuration Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="670b5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="670b5-108">Syntax</span></span>


```C++
typedef struct {
  DWORD           dwNumIntfs;
  PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;
```



## <a name="members"></a><span data-ttu-id="670b5-109">Members</span><span class="sxs-lookup"><span data-stu-id="670b5-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="670b5-110">**dwNumIntfs**</span><span class="sxs-lookup"><span data-stu-id="670b5-110">**dwNumIntfs**</span></span>
</dt> <dd>

<span data-ttu-id="670b5-111">Numero totale di interfacce.</span><span class="sxs-lookup"><span data-stu-id="670b5-111">Total number of interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="670b5-112">**pIntfs**</span><span class="sxs-lookup"><span data-stu-id="670b5-112">**pIntfs**</span></span>
</dt> <dd>

<span data-ttu-id="670b5-113">Puntatore alla struttura [**della \_ \_ voce della chiave INTF**](intf-key-entry.md) .</span><span class="sxs-lookup"><span data-stu-id="670b5-113">Pointer to the [**INTF\_KEY\_ENTRY**](intf-key-entry.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="670b5-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="670b5-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="670b5-115">Il file di intestazione *wzcsapi. h* non è disponibile nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="670b5-115">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="670b5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="670b5-116">Requirements</span></span>



| <span data-ttu-id="670b5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="670b5-117">Requirement</span></span> | <span data-ttu-id="670b5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="670b5-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="670b5-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="670b5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="670b5-120">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="670b5-120">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="670b5-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="670b5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="670b5-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="670b5-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="670b5-123">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="670b5-123">End of client support</span></span><br/>    | <span data-ttu-id="670b5-124">Windows XP con SP3</span><span class="sxs-lookup"><span data-stu-id="670b5-124">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="670b5-125">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="670b5-125">End of server support</span></span><br/>    | <span data-ttu-id="670b5-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="670b5-126">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="670b5-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="670b5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="670b5-128"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="670b5-128"><dt>Wzcsapi.h</dt></span></span> </dl> |



 

 




