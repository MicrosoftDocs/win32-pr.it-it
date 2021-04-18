---
description: "Il WiaTransferParams viene trasmesso a un'applicazione durante il trasferimento dei dati dal sistema di runtime di acquisizione immagini Windows (WIA) al metodo IWiaTransferCallback:: TransferCallback."
ms.assetid: 4f1bbacf-e9fd-4129-ab05-3edaeecfaf43
title: Struttura WiaTransferParams (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaTransferParams
api_type:
- HeaderDef
api_location:
- Wia.h
ms.openlocfilehash: 4c432cab14e08d89a49234dd7c6de059cc9d72c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307286"
---
# <a name="wiatransferparams-structure"></a><span data-ttu-id="4c431-103">Struttura WiaTransferParams</span><span class="sxs-lookup"><span data-stu-id="4c431-103">WiaTransferParams structure</span></span>

<span data-ttu-id="4c431-104">Il **WiaTransferParams** viene trasmesso a un'applicazione durante il trasferimento dei dati dal sistema di runtime di acquisizione immagini Windows (WIA) al metodo [**IWiaTransferCallback:: TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) .</span><span class="sxs-lookup"><span data-stu-id="4c431-104">The **WiaTransferParams** is transmitted to an application during a data transfer by the Windows Image Acquisition (WIA) run-time system to the [**IWiaTransferCallback::TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c431-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c431-105">Syntax</span></span>


```C++
typedef struct _WiaTransferParams {
  LONG    lMessage;
  LONG    lPercentComplete;
  ULONG64 ulTransferredBytes;
  HRESULT hrErrorStatus;
} WiaTransferParams;
```



## <a name="members"></a><span data-ttu-id="4c431-106">Members</span><span class="sxs-lookup"><span data-stu-id="4c431-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4c431-107">**lMessage**</span><span class="sxs-lookup"><span data-stu-id="4c431-107">**lMessage**</span></span>
</dt> <dd>

<span data-ttu-id="4c431-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="4c431-108">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="4c431-109">Indica lo stato del trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="4c431-109">Indicates the status of the data transfer.</span></span>

<dt>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>

<span data-ttu-id="4c431-110"><span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**\_ \_ stato messaggio di trasferimento WIA \_**</span><span class="sxs-lookup"><span data-stu-id="4c431-110"><span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**WIA\_TRANSFER\_MSG\_STATUS**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>

<span data-ttu-id="4c431-111"><span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**\_ \_ \_ fine \_ del flusso del messaggio di trasferimento WIA \_**</span><span class="sxs-lookup"><span data-stu-id="4c431-111"><span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**WIA\_TRANSFER\_MSG\_END\_OF\_STREAM**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>

<span data-ttu-id="4c431-112"><span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**\_ \_ \_ fine \_ del trasferimento del messaggio di trasferimento WIA \_**</span><span class="sxs-lookup"><span data-stu-id="4c431-112"><span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**WIA\_TRANSFER\_MSG\_END\_OF\_TRANSFER**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>

<span data-ttu-id="4c431-113"><span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**\_stato del \_ dispositivo del messaggio di trasferimento WIA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4c431-113"><span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**WIA\_TRANSFER\_MSG\_DEVICE\_STATUS**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>

<span data-ttu-id="4c431-114"><span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**\_ \_ \_ pagina nuovo messaggio di trasferimento WIA \_**</span><span class="sxs-lookup"><span data-stu-id="4c431-114"><span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**WIA\_TRANSFER\_MSG\_NEW\_PAGE**</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="4c431-115">**lPercentComplete**</span><span class="sxs-lookup"><span data-stu-id="4c431-115">**lPercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="4c431-116">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="4c431-116">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="4c431-117">Indica lo stato di avanzamento del trasferimento dei dati come percentuale.</span><span class="sxs-lookup"><span data-stu-id="4c431-117">Indicates the progress of the data transfer as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="4c431-118">**ulTransferredBytes**</span><span class="sxs-lookup"><span data-stu-id="4c431-118">**ulTransferredBytes**</span></span>
</dt> <dd>

<span data-ttu-id="4c431-119">Tipo: **ULONG64**</span><span class="sxs-lookup"><span data-stu-id="4c431-119">Type: **ULONG64**</span></span>

</dd> <dd>

<span data-ttu-id="4c431-120">Indica la quantità di dati trasferiti.</span><span class="sxs-lookup"><span data-stu-id="4c431-120">Indicates the amount of data transferred.</span></span>

</dd> <dt>

<span data-ttu-id="4c431-121">**hrErrorStatus**</span><span class="sxs-lookup"><span data-stu-id="4c431-121">**hrErrorStatus**</span></span>
</dt> <dd>

<span data-ttu-id="4c431-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4c431-122">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="4c431-123">Stato, o stato di errore, del dispositivo impostato dal driver; ad esempio, "riscaldamento".</span><span class="sxs-lookup"><span data-stu-id="4c431-123">The status, or error state, of the device set by the driver; for example, "warming up".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c431-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c431-124">Requirements</span></span>



| <span data-ttu-id="4c431-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c431-125">Requirement</span></span> | <span data-ttu-id="4c431-126">Valore</span><span class="sxs-lookup"><span data-stu-id="4c431-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="4c431-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c431-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4c431-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c431-128">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4c431-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c431-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4c431-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4c431-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4c431-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c431-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c431-132"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c431-132"><dt>Wia.h</dt></span></span> </dl> |



 

 




