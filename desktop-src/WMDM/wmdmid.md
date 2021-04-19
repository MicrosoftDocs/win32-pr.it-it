---
title: Struttura WMDMID
description: La struttura WMDMID descrive i numeri di serie e gli ID di gruppo.
ms.assetid: eaa5786e-a2a1-42d7-b527-be83d944cb20
keywords:
- Struttura WMDMID Windows Media Gestione dispositivi
- Puntatore alla struttura PWMDMID Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDMID
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8edc2a364bf29ead6aaf4fad8ad3a56fe80d7176
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332689"
---
# <a name="wmdmid-structure"></a><span data-ttu-id="7d269-105">Struttura WMDMID</span><span class="sxs-lookup"><span data-stu-id="7d269-105">WMDMID structure</span></span>

<span data-ttu-id="7d269-106">La struttura **WMDMID** descrive i numeri di serie e gli ID di gruppo.</span><span class="sxs-lookup"><span data-stu-id="7d269-106">The **WMDMID** structure describes serial numbers and group IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d269-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d269-107">Syntax</span></span>


```C++
typedef struct __WMDMID {
  UINT  cbSize;
  DWORD dwVendorID;
  BYTE  pID[WMDMID_LENGTH];
  UINT  SerialNumberLength;
} WMDMID, *PWMDMID;
```



## <a name="members"></a><span data-ttu-id="7d269-108">Members</span><span class="sxs-lookup"><span data-stu-id="7d269-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7d269-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="7d269-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="7d269-110">Dimensione della struttura **WMDMID** in byte.</span><span class="sxs-lookup"><span data-stu-id="7d269-110">Size of the **WMDMID** structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7d269-111">**dwVendorID**</span><span class="sxs-lookup"><span data-stu-id="7d269-111">**dwVendorID**</span></span>
</dt> <dd>

<span data-ttu-id="7d269-112">**DWORD** contenente il numero ID registrato del fornitore.</span><span class="sxs-lookup"><span data-stu-id="7d269-112">**DWORD** containing the registered ID number of the vendor.</span></span> <span data-ttu-id="7d269-113">Contiene zero se non è in uso.</span><span class="sxs-lookup"><span data-stu-id="7d269-113">Contains zero if not in use.</span></span>

</dd> <dt>

<span data-ttu-id="7d269-114">**\[lunghezza WMDMID \_ PID\]**</span><span class="sxs-lookup"><span data-stu-id="7d269-114">**pID\[WMDMID\_LENGTH\]**</span></span>
</dt> <dd>

<span data-ttu-id="7d269-115">Puntatore a una matrice di byte che contiene il numero di serie.</span><span class="sxs-lookup"><span data-stu-id="7d269-115">Pointer to an array of bytes containing the serial number.</span></span> <span data-ttu-id="7d269-116">Il numero di serie è una stringa di valori di byte privi di formato standard.</span><span class="sxs-lookup"><span data-stu-id="7d269-116">The serial number is a string of byte values that have no standard format.</span></span> <span data-ttu-id="7d269-117">Si noti che non si tratta di un valore a caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="7d269-117">Note that this is not a wide-character value.</span></span> <span data-ttu-id="7d269-118">**WMDMID \_ LENGTH** è un valore costante definito in mswmdm. h.</span><span class="sxs-lookup"><span data-stu-id="7d269-118">**WMDMID\_LENGTH** is a constant value defined in mswmdm.h.</span></span>

</dd> <dt>

<span data-ttu-id="7d269-119">**SerialNumberLength**</span><span class="sxs-lookup"><span data-stu-id="7d269-119">**SerialNumberLength**</span></span>
</dt> <dd>

<span data-ttu-id="7d269-120">Lunghezza effettiva del numero di serie restituito, in byte.</span><span class="sxs-lookup"><span data-stu-id="7d269-120">Actual length of the serial number returned, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d269-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d269-121">Requirements</span></span>



| <span data-ttu-id="7d269-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d269-122">Requirement</span></span> | <span data-ttu-id="7d269-123">Valore</span><span class="sxs-lookup"><span data-stu-id="7d269-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7d269-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d269-124">Header</span></span><br/> | <dl> <span data-ttu-id="7d269-125"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7d269-125"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d269-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d269-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d269-127">**IMDSPDevice:: GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="7d269-127">**IMDSPDevice::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getserialnumber)
</dt> <dt>

[<span data-ttu-id="7d269-128">**IMDSPStorageGlobals:: GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="7d269-128">**IMDSPStorageGlobals::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)
</dt> <dt>

[<span data-ttu-id="7d269-129">**IWMDMDevice:: GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="7d269-129">**IWMDMDevice::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getserialnumber)
</dt> <dt>

[<span data-ttu-id="7d269-130">**IWMDMStorageGlobals:: GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="7d269-130">**IWMDMStorageGlobals::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber)
</dt> <dt>

[<span data-ttu-id="7d269-131">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="7d269-131">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





