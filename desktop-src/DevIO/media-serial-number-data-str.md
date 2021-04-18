---
description: Contiene il numero di serie di un dispositivo USB. Viene usato dal codice di controllo del numero di serie del supporto per l' \_ archiviazione IOCTL \_ \_ \_ \_ .
ms.assetid: a7df4528-a3b7-4ffa-b595-7ac918371582
title: Struttura MEDIA_SERIAL_NUMBER_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SERIAL_NUMBER_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 843c445a29bcce9e6dc26b66b0c6738831e9b79c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320543"
---
# <a name="media_serial_number_data-structure"></a><span data-ttu-id="1db02-104">\_ \_ Struttura dei dati del numero di serie dei supporti \_</span><span class="sxs-lookup"><span data-stu-id="1db02-104">MEDIA\_SERIAL\_NUMBER\_DATA structure</span></span>

<span data-ttu-id="1db02-105">Contiene il numero di serie di un dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="1db02-105">Contains the serial number of a USB device.</span></span> <span data-ttu-id="1db02-106">Viene usato dal codice di controllo del [**\_ numero di \_ \_ \_ serie \_ del supporto per l'archiviazione IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) .</span><span class="sxs-lookup"><span data-stu-id="1db02-106">It is used by the [**IOCTL\_STORAGE\_GET\_MEDIA\_SERIAL\_NUMBER**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1db02-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1db02-107">Syntax</span></span>


```C++
typedef struct _MEDIA_SERIAL_NUMBER_DATA {
  ULONG SerialNumberLength;
  ULONG Result;
  ULONG Reserved[2];
  UCHAR SerialNumberData[];
} MEDIA_SERIAL_NUMBER_DATA, *PMEDIA_SERIAL_NUMBER_DATA;
```



## <a name="members"></a><span data-ttu-id="1db02-108">Members</span><span class="sxs-lookup"><span data-stu-id="1db02-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1db02-109">**SerialNumberLength**</span><span class="sxs-lookup"><span data-stu-id="1db02-109">**SerialNumberLength**</span></span>
</dt> <dd>

<span data-ttu-id="1db02-110">Dimensioni in byte della stringa **SerialNumberData** .</span><span class="sxs-lookup"><span data-stu-id="1db02-110">The size of the **SerialNumberData** string, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1db02-111">**Risultato**</span><span class="sxs-lookup"><span data-stu-id="1db02-111">**Result**</span></span>
</dt> <dd>

<span data-ttu-id="1db02-112">Lo stato della richiesta.</span><span class="sxs-lookup"><span data-stu-id="1db02-112">The status of the request.</span></span>

</dd> <dt>

<span data-ttu-id="1db02-113">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="1db02-113">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="1db02-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="1db02-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="1db02-115">**SerialNumberData**</span><span class="sxs-lookup"><span data-stu-id="1db02-115">**SerialNumberData**</span></span>
</dt> <dd>

<span data-ttu-id="1db02-116">Numero di serie del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1db02-116">The serial number of the device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1db02-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="1db02-117">Remarks</span></span>

<span data-ttu-id="1db02-118">Non è disponibile alcun file di intestazione per la struttura **\_ \_ \_ dei dati del numero di serie dei supporti** .</span><span class="sxs-lookup"><span data-stu-id="1db02-118">No header file is available for the **MEDIA\_SERIAL\_NUMBER\_DATA** structure.</span></span> <span data-ttu-id="1db02-119">Includere la definizione della struttura nella parte superiore di questa pagina nel codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="1db02-119">Include the structure definition at the top of this page in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1db02-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1db02-120">Requirements</span></span>



| <span data-ttu-id="1db02-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1db02-121">Requirement</span></span> | <span data-ttu-id="1db02-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1db02-122">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1db02-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1db02-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1db02-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1db02-124">Windows XP</span></span><br/>          |
| <span data-ttu-id="1db02-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1db02-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1db02-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1db02-126">Windows Server 2003</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1db02-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1db02-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1db02-128">**\_numero di \_ \_ serie supporti \_ \_ per archiviazione IOCTL**</span><span class="sxs-lookup"><span data-stu-id="1db02-128">**IOCTL\_STORAGE\_GET\_MEDIA\_SERIAL\_NUMBER**</span></span>](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)
</dt> </dl>

 

 




