---
description: L'API di distribuzione peer definisce i tipi di dati seguenti.
ms.assetid: 5a378965-696c-4205-b9de-bdf93f00018f
title: Tipi di dati dell'API di distribuzione peer (Peerdist. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a7bff6fe75c8f4632248c92af37aea6e00c3052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312253"
---
# <a name="peer-distribution-api-data-types"></a><span data-ttu-id="a7c09-103">Tipi di dati dell'API di distribuzione peer</span><span class="sxs-lookup"><span data-stu-id="a7c09-103">Peer Distribution API Data Types</span></span>

<span data-ttu-id="a7c09-104">L'API di distribuzione peer definisce i tipi di dati seguenti.</span><span class="sxs-lookup"><span data-stu-id="a7c09-104">The Peer Distribution API defines the following data types.</span></span>


```C++
typedef HANDLE PEERDIST_INSTANCE_HANDLE;
typedef HANDLE PEERDIST_CONTENT_HANDLE;
typedef HANDLE PEERDIST_CONTENTINFO_HANDLE;
typedef HANDLE PEERDIST_STREAM_HANDLE;
```





| <span data-ttu-id="a7c09-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a7c09-105">Data type</span></span>                                                                                                                     | <span data-ttu-id="a7c09-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7c09-106">Description</span></span>                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7c09-107"><span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**\_handle dell'istanza di PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="a7c09-107"><span id="PEERDIST_INSTANCE_HANDLE"></span><span id="peerdist_instance_handle"></span>**PEERDIST\_INSTANCE\_HANDLE**</span></span>          | <span data-ttu-id="a7c09-108">Handle associato all'istanza di distribuzione peer.</span><span class="sxs-lookup"><span data-stu-id="a7c09-108">A handle associated with the Peer Distribution instance.</span></span> <span data-ttu-id="a7c09-109">Questo handle viene creato da [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup)e usato nella maggior parte delle operazioni di distribuzione peer.</span><span class="sxs-lookup"><span data-stu-id="a7c09-109">This handle is created by [**PeerDistStartup**](/windows/desktop/api/PeerDist/nf-peerdist-peerdiststartup), and used in most Peer Distribution operations.</span></span><br/>                                          |
| <span data-ttu-id="a7c09-110"><span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**\_handle di contenuto PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="a7c09-110"><span id="PEERDIST_CONTENT_HANDLE"></span><span id="peerdist_content_handle"></span>**PEERDIST\_CONTENT\_HANDLE**</span></span>             | <span data-ttu-id="a7c09-111">Handle associato al contenuto.</span><span class="sxs-lookup"><span data-stu-id="a7c09-111">A handle associated with content.</span></span> <span data-ttu-id="a7c09-112">Questo handle viene creato da [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) e a cui viene fatto riferimento durante l'apertura, la chiusura, l'aggiunta o la pubblicazione di contenuto.</span><span class="sxs-lookup"><span data-stu-id="a7c09-112">This handle is created by [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent) and is referenced when opening, closing, adding, or publishing content.</span></span><br/>                     |
| <span data-ttu-id="a7c09-113"><span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**\_handle CONTENTINFO \_ PEERDIST**</span><span class="sxs-lookup"><span data-stu-id="a7c09-113"><span id="PEERDIST_CONTENTINFO_HANDLE"></span><span id="peerdist_contentinfo_handle"></span>**PEERDIST\_CONTENTINFO\_HANDLE**</span></span> | <span data-ttu-id="a7c09-114">Handle associato alle informazioni sul contenuto.</span><span class="sxs-lookup"><span data-stu-id="a7c09-114">A handle associated with content information.</span></span> <span data-ttu-id="a7c09-115">Questo handle viene creato da [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)e viene usato durante il recupero delle informazioni sul contenuto codificato.</span><span class="sxs-lookup"><span data-stu-id="a7c09-115">This handle is created by [**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation), and is used when retrieving encoded content information.</span></span><br/> |
| <span data-ttu-id="a7c09-116"><span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**\_handle del flusso PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="a7c09-116"><span id="PEERDIST_STREAM_HANDLE"></span><span id="peerdist_stream_handle"></span>**PEERDIST\_STREAM\_HANDLE**</span></span>                | <span data-ttu-id="a7c09-117">Handle associato a un flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="a7c09-117">A handle associated with a data stream.</span></span> <span data-ttu-id="a7c09-118">Questo handle viene creato da [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) ed è usato come riferimento durante la pubblicazione, la chiusura o l'aggiunta di contenuto trasmesso.</span><span class="sxs-lookup"><span data-stu-id="a7c09-118">This handle is created by [**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream) and is referenced when publishing, closing, or adding to streamed content.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="a7c09-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7c09-119">Requirements</span></span>



| <span data-ttu-id="a7c09-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7c09-120">Requirement</span></span> | <span data-ttu-id="a7c09-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a7c09-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7c09-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7c09-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a7c09-123">\[Solo app desktop Windows 7 Professional\]</span><span class="sxs-lookup"><span data-stu-id="a7c09-123">Windows 7 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a7c09-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7c09-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a7c09-125">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a7c09-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a7c09-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7c09-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7c09-127"><dt>Peerdist. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7c09-127"><dt>Peerdist.h</dt></span></span> </dl> |



 

 




