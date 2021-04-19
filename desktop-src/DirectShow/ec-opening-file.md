---
description: Il grafico apre un file o ha terminato l'apertura di un file.
ms.assetid: 352867e1-025f-4adb-be32-f7941c0ec8cf
title: EC_OPENING_FILE (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf275a2f9b64f9a30c8049b5207622270edc5098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332196"
---
# <a name="ec_opening_file"></a><span data-ttu-id="58e47-103">\_file di apertura EC \_</span><span class="sxs-lookup"><span data-stu-id="58e47-103">EC\_OPENING\_FILE</span></span>

<span data-ttu-id="58e47-104">Il grafico apre un file o ha terminato l'apertura di un file.</span><span class="sxs-lookup"><span data-stu-id="58e47-104">The graph is opening a file, or has finished opening a file.</span></span>

## <a name="parameters"></a><span data-ttu-id="58e47-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="58e47-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58e47-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="58e47-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="58e47-107">**True** se il grafico sta iniziando ad aprire un file oppure **false** se il grafo non sta più aprendo il file.</span><span class="sxs-lookup"><span data-stu-id="58e47-107">**TRUE** if the graph is starting to open a file, or **FALSE** if the graph is no longer opening the file.</span></span>

</dd> <dt>

<span data-ttu-id="58e47-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="58e47-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="58e47-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="58e47-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="58e47-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="58e47-110">Default Action</span></span>

<span data-ttu-id="58e47-111">No.</span><span class="sxs-lookup"><span data-stu-id="58e47-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="58e47-112">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="58e47-112">Remarks</span></span>

<span data-ttu-id="58e47-113">Un filtro può inviare questo evento se trascorre molto tempo per l'apertura di un file.</span><span class="sxs-lookup"><span data-stu-id="58e47-113">A filter can send this event if it spends significant time opening a file.</span></span> <span data-ttu-id="58e47-114">Ad esempio, il file potrebbe trovarsi in una rete. L'applicazione può utilizzare questo evento per modificare l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="58e47-114">(For example, the file might be located on a network.) The application can use this event to adjust its user interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="58e47-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58e47-115">Requirements</span></span>



| <span data-ttu-id="58e47-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="58e47-116">Requirement</span></span> | <span data-ttu-id="58e47-117">Valore</span><span class="sxs-lookup"><span data-stu-id="58e47-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="58e47-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58e47-118">Header</span></span><br/> | <dl> <span data-ttu-id="58e47-119"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="58e47-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58e47-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58e47-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58e47-121">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="58e47-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="58e47-122">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="58e47-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




