---
description: Il grafico memorizza nel buffer i dati o ha interrotto il buffering dei dati.
ms.assetid: 39e8b151-0323-42b3-99f0-3dcd230925c8
title: EC_BUFFERING_DATA (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1395a10458abd7a29fdb65e7ab55fba62328d6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328471"
---
# <a name="ec_buffering_data"></a><span data-ttu-id="a364c-103">\_dati di buffering EC \_</span><span class="sxs-lookup"><span data-stu-id="a364c-103">EC\_BUFFERING\_DATA</span></span>

<span data-ttu-id="a364c-104">Il grafico memorizza nel buffer i dati o ha interrotto il buffering dei dati.</span><span class="sxs-lookup"><span data-stu-id="a364c-104">The graph is buffering data, or has stopped buffering data.</span></span>

## <a name="parameters"></a><span data-ttu-id="a364c-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="a364c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a364c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a364c-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a364c-107">(**Bool**) **True** se il grafico sta iniziando a memorizzare nel buffer oppure **false** se il grafico ha interrotto il buffering.</span><span class="sxs-lookup"><span data-stu-id="a364c-107">(**BOOL**) **TRUE** if the graph is starting to buffer, or **FALSE** if the graph has stopped buffering.</span></span>

</dd> <dt>

<span data-ttu-id="a364c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a364c-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a364c-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="a364c-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="a364c-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="a364c-110">Default Action</span></span>

<span data-ttu-id="a364c-111">No.</span><span class="sxs-lookup"><span data-stu-id="a364c-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="a364c-112">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="a364c-112">Remarks</span></span>

<span data-ttu-id="a364c-113">Un filtro può inviare questo evento se è necessario che i dati vengano memorizzati nel buffer da un'origine esterna.</span><span class="sxs-lookup"><span data-stu-id="a364c-113">A filter can send this event if it needs to buffer data from an external source.</span></span> <span data-ttu-id="a364c-114">È possibile, ad esempio, caricare i dati da una rete. L'applicazione può utilizzare questo evento per modificare l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="a364c-114">(For example, it might be loading data from a network.) The application can use this event to adjust its user interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="a364c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a364c-115">Requirements</span></span>



| <span data-ttu-id="a364c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a364c-116">Requirement</span></span> | <span data-ttu-id="a364c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a364c-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a364c-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a364c-118">Header</span></span><br/> | <dl> <span data-ttu-id="a364c-119"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="a364c-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a364c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a364c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a364c-121">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="a364c-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a364c-122">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="a364c-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




