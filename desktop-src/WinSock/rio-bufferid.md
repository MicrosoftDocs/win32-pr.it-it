---
description: Specifica un descrittore di buffer registrato utilizzato con le estensioni I/O registrate di Winsock.
ms.assetid: 87D0A3F6-A44C-4D7F-B276-7FD5DC2DE7A3
title: RIO_BUFFERID (Mswsockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75bb439a567c361a056b750728d986891a1da468
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049767"
---
# <a name="rio_bufferid"></a><span data-ttu-id="5cd27-103">RIO \_ BUFFERID</span><span class="sxs-lookup"><span data-stu-id="5cd27-103">RIO\_BUFFERID</span></span>

<span data-ttu-id="5cd27-104">Il **typedef \_ BUFFERID di Rio** specifica un descrittore di buffer registrato usato con le estensioni i/O registrate di Winsock.</span><span class="sxs-lookup"><span data-stu-id="5cd27-104">The **RIO\_BUFFERID** typedef specifies a registered buffer descriptor used with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_BUFFERID_t* RIO_BUFFERID, **PRIO_BUFFERID;
```



<dl> <dt>

<span data-ttu-id="5cd27-105">**RIO \_ BUFFERID**</span><span class="sxs-lookup"><span data-stu-id="5cd27-105">**RIO\_BUFFERID**</span></span>
</dt> <dd>

<span data-ttu-id="5cd27-106">Tipo di dati che specifica un descrittore di buffer registrato utilizzato con le richieste di invio e ricezione.</span><span class="sxs-lookup"><span data-stu-id="5cd27-106">A data type that specifies a registered buffer descriptor used with send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5cd27-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="5cd27-107">Remarks</span></span>

<span data-ttu-id="5cd27-108">Le estensioni I/O registrate di Winsock operano principalmente sui buffer registrati tramite oggetti **Rio \_ BUFFERID** .</span><span class="sxs-lookup"><span data-stu-id="5cd27-108">The Winsock registered I/O extensions operate primarily on registered buffers using **RIO\_BUFFERID** objects.</span></span> <span data-ttu-id="5cd27-109">Un'applicazione ottiene un **\_ BUFFERID Rio** per un buffer esistente usando la funzione [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5cd27-109">An application obtains a **RIO\_BUFFERID** for an existing buffer using the [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) function.</span></span> <span data-ttu-id="5cd27-110">Un'applicazione può rilasciare una registrazione usando la funzione [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) .</span><span class="sxs-lookup"><span data-stu-id="5cd27-110">An application can release a registration using the [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) function.</span></span>

<span data-ttu-id="5cd27-111">Quando un buffer esistente viene registrato come oggetto **Rio \_ BUFFERID** usando la funzione [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) , alcune risorse interne vengono allocate dalla memoria fisica e il buffer dell'applicazione esistente verrà bloccato nella memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="5cd27-111">When an existing buffer is registered as a **RIO\_BUFFERID** object using the [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) function, certain internal resources are allocated from physical memory, and the existing application buffer will be locked into physical memory.</span></span> <span data-ttu-id="5cd27-112">La funzione [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) viene chiamata per annullare la registrazione del buffer, liberare queste risorse interne e consentire il sblocco e il rilascio del buffer dalla memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="5cd27-112">The [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) function is called to deregister the buffer, free these internal resources, and allow the buffer to be unlocked and released from physical memory.</span></span>

<span data-ttu-id="5cd27-113">La registrazione ripetuta e l'annullamento della registrazione dei buffer di applicazione mediante le estensioni I/O registrate di Winsock possono causare un calo significativo delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="5cd27-113">Repeated registration and deregistration of application buffers using the Winsock registered I/O extensions may cause significant performance degradation.</span></span> <span data-ttu-id="5cd27-114">Quando si progetta un'applicazione utilizzando le estensioni I/O registrate di Winsock, è necessario considerare i seguenti approcci di gestione del buffer per ridurre al minimo la registrazione e l'annullamento della registrazione ripetuti dei buffer dell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="5cd27-114">The following buffer management approaches should be considered when designing an application using the Winsock registered I/O extensions to minimize repeated registration and deregistration of application buffers:</span></span>

-   <span data-ttu-id="5cd27-115">• Ottimizzare il riutilizzo dei buffer.</span><span class="sxs-lookup"><span data-stu-id="5cd27-115">• Maximize the reuse of buffers.</span></span>
-   <span data-ttu-id="5cd27-116">• Mantenere un pool limitato di buffer registrati non usati per l'uso da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5cd27-116">• Maintain a limited pool of unused registered buffers for use by the application.</span></span>
-   <span data-ttu-id="5cd27-117">• Mantenere un pool limitato di buffer registrati ed eseguire copie del buffer tra questi buffer registrati e altri buffer non registrati.</span><span class="sxs-lookup"><span data-stu-id="5cd27-117">• Maintain a limited pool of registered buffers and perform buffer copies between these registered buffers and other unregistered buffers.</span></span>

<span data-ttu-id="5cd27-118">Il typedef **Rio \_ BUFFERID** è definito nel file di intestazione *Mswsockdef. h* , che viene incluso automaticamente nel file di intestazione *mswsock. h* .</span><span class="sxs-lookup"><span data-stu-id="5cd27-118">The **RIO\_BUFFERID** typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="5cd27-119">Il file di intestazione *Mswsockdef. h* non deve mai essere utilizzato direttamente.</span><span class="sxs-lookup"><span data-stu-id="5cd27-119">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cd27-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5cd27-120">Requirements</span></span>



| <span data-ttu-id="5cd27-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cd27-121">Requirement</span></span> | <span data-ttu-id="5cd27-122">Valore</span><span class="sxs-lookup"><span data-stu-id="5cd27-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cd27-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cd27-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5cd27-124">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5cd27-124">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="5cd27-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cd27-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5cd27-126">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5cd27-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="5cd27-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5cd27-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cd27-128"><dt>Mswsockdef. h (include mswsock. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5cd27-128"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cd27-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5cd27-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cd27-130">**\_BUF Rio**</span><span class="sxs-lookup"><span data-stu-id="5cd27-130">**RIO\_BUF**</span></span>](/windows/desktop/api/Mswsockdef/ns-mswsockdef-rio_buf)
</dt> <dt>

[<span data-ttu-id="5cd27-131">**RIODeregisterBuffer**</span><span class="sxs-lookup"><span data-stu-id="5cd27-131">**RIODeregisterBuffer**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer)
</dt> <dt>

[<span data-ttu-id="5cd27-132">**RIOReceive**</span><span class="sxs-lookup"><span data-stu-id="5cd27-132">**RIOReceive**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[<span data-ttu-id="5cd27-133">**RIOReceiveEx**</span><span class="sxs-lookup"><span data-stu-id="5cd27-133">**RIOReceiveEx**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

<span data-ttu-id="5cd27-134">[**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5cd27-134">[**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5cd27-135">**RIOSend**</span><span class="sxs-lookup"><span data-stu-id="5cd27-135">**RIOSend**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

<span data-ttu-id="5cd27-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5cd27-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span></span>
</dt> </dl>

 

 
