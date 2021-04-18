---
description: La tabella seguente descrive le \_ Opzioni del socket del tipo di traffico IP DSCP \_ \_ .
ms.assetid: 0042B53F-B84E-453A-8E18-87052280DAD5
title: IP_DSCP_TRAFFIC_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IP_DSCP_TRAFFIC_TYPE
api_type:
- HeaderDef
api_location:
- N/A
ms.openlocfilehash: 80cbe41e58cf36cd366015d83af380f5952630ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328375"
---
# <a name="ip_dscp_traffic_type"></a><span data-ttu-id="20139-103">\_tipo di \_ traffico \_ DSCP IP</span><span class="sxs-lookup"><span data-stu-id="20139-103">IP\_DSCP\_TRAFFIC\_TYPE</span></span>

<span data-ttu-id="20139-104">La tabella seguente descrive le \_ Opzioni del socket del tipo di traffico IP DSCP \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="20139-104">The following table describes IP\_DSCP\_TRAFFIC\_TYPE Socket Options.</span></span>

<dl> <span data-ttu-id="20139-105"><dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**\_tipo di \_ traffico \_ DSCP IP**</dt> </span><span class="sxs-lookup"><span data-stu-id="20139-105"><dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**IP\_DSCP\_TRAFFIC\_TYPE**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="20139-106">Opzione</span><span class="sxs-lookup"><span data-stu-id="20139-106">Option</span></span>              | <span data-ttu-id="20139-107">Recupero</span><span class="sxs-lookup"><span data-stu-id="20139-107">Get</span></span> | <span data-ttu-id="20139-108">Set</span><span class="sxs-lookup"><span data-stu-id="20139-108">Set</span></span> | <span data-ttu-id="20139-109">Tipo optVal</span><span class="sxs-lookup"><span data-stu-id="20139-109">Optval Type</span></span> | <span data-ttu-id="20139-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20139-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------|-----|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20139-111">\_tipo di traffico DSCP \_</span><span class="sxs-lookup"><span data-stu-id="20139-111">DSCP\_TRAFFIC\_TYPE</span></span> | <span data-ttu-id="20139-112">Sì</span><span class="sxs-lookup"><span data-stu-id="20139-112">Yes</span></span> | <span data-ttu-id="20139-113">Sì</span><span class="sxs-lookup"><span data-stu-id="20139-113">Yes</span></span> | <span data-ttu-id="20139-114">DWORD</span><span class="sxs-lookup"><span data-stu-id="20139-114">DWORD</span></span>       | <span data-ttu-id="20139-115">Impostando questo valore su valori definiti nel **\_ \_ tipo di traffico DSCP**, un'applicazione sarà in grado di richiedere i pacchetti di rete da considerare in base al tipo di servizio richiesto.</span><span class="sxs-lookup"><span data-stu-id="20139-115">By setting this value to values defined in **DSCP\_TRAFFIC\_TYPE**, an application will be able to ask its network packets to be treated according to the type of service being requested.</span></span> <span data-ttu-id="20139-116">Analogamente, le chiamate a [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) possono essere usate per ottenere l'impostazione corrente per il tipo di traffico richiesto sul socket specificato</span><span class="sxs-lookup"><span data-stu-id="20139-116">Similarly calls to [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) can be used to obtain the current setting for the type of traffic requested on the given socket</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20139-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20139-117">Requirements</span></span>



| <span data-ttu-id="20139-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="20139-118">Requirement</span></span> | <span data-ttu-id="20139-119">Valore</span><span class="sxs-lookup"><span data-stu-id="20139-119">Value</span></span> |
|----------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="20139-120">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="20139-120">End of client support</span></span><br/> | <span data-ttu-id="20139-121">Windows 10</span><span class="sxs-lookup"><span data-stu-id="20139-121">Windows 10</span></span><br/>                                                          |
| <span data-ttu-id="20139-122">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="20139-122">End of server support</span></span><br/> | <span data-ttu-id="20139-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="20139-123">Windows Server 2016</span></span><br/>                                                 |
| <span data-ttu-id="20139-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20139-124">Header</span></span><br/>                | <dl> <span data-ttu-id="20139-125"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="20139-125"><dt>N/A</dt></span></span> </dl> |



 

 




