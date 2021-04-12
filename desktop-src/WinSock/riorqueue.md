---
description: Specifica un descrittore di socket utilizzato dalle richieste di invio e ricezione con le estensioni I/O registrate di Winsock.
ms.assetid: 50E9516C-6078-4466-A593-3F29E4783740
title: RIO_RQ (Mswsockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25abebbe40842532f3cca180868b5b3786e756d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344741"
---
# <a name="rio_rq"></a><span data-ttu-id="c22b5-103">RIO \_ RQ</span><span class="sxs-lookup"><span data-stu-id="c22b5-103">RIO\_RQ</span></span>

<span data-ttu-id="c22b5-104">Il typedef di **Rio \_ RQ** specifica un descrittore di socket usato dalle richieste di invio e ricezione con le estensioni i/O registrate di Winsock.</span><span class="sxs-lookup"><span data-stu-id="c22b5-104">The **RIO\_RQ** typedef specifies a socket descriptor used by send and receive requests with the Winsock registered I/O extensions.</span></span>


```C++
typedef struct RIO_RQ_t* RIO_RQ, **PRIO_RQ;
```



<dl> <dt>

<span data-ttu-id="c22b5-105">**RIO \_ RQ**</span><span class="sxs-lookup"><span data-stu-id="c22b5-105">**RIO\_RQ**</span></span>
</dt> <dd>

<span data-ttu-id="c22b5-106">Tipo di dati che specifica un descrittore di socket utilizzato dalle richieste di invio e ricezione.</span><span class="sxs-lookup"><span data-stu-id="c22b5-106">A data type that specifies a socket descriptor used by send and receive requests.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c22b5-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="c22b5-107">Remarks</span></span>

<span data-ttu-id="c22b5-108">Le estensioni I/O registrate di Winsock operano principalmente su un oggetto **Rio \_ RQ** anziché su un socket.</span><span class="sxs-lookup"><span data-stu-id="c22b5-108">The Winsock registered I/O extensions operate primarily on a **RIO\_RQ** object rather than a socket.</span></span> <span data-ttu-id="c22b5-109">Un'applicazione ottiene un oggetto **Rio \_ RQ** per un socket esistente usando la funzione [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) .</span><span class="sxs-lookup"><span data-stu-id="c22b5-109">An application obtains a **RIO\_RQ** for an existing socket using the [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) function.</span></span> <span data-ttu-id="c22b5-110">Il socket di input deve essere stato creato chiamando la funzione [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) con il flag WSA del flag **\_ \_ Rio** impostato nel parametro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="c22b5-110">The input socket must have been created by calling the [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) function with the **WSA\_FLAG\_RIO** flag set in the *dwFlags* parameter.</span></span>

<span data-ttu-id="c22b5-111">Dopo aver ottenuto un oggetto **Rio \_ RQ** , il descrittore di socket sottostante rimane valido.</span><span class="sxs-lookup"><span data-stu-id="c22b5-111">After obtaining a **RIO\_RQ** object, the underlying socket descriptor remains valid.</span></span> <span data-ttu-id="c22b5-112">Un'applicazione può continuare a usare il socket sottostante per impostare ed eseguire query sulle opzioni del socket, emettere IOCTL e infine chiudere il socket.</span><span class="sxs-lookup"><span data-stu-id="c22b5-112">An application may continue to use the underlying socket to set and query socket options, issue IOCTLs and ultimately close the socket.</span></span>

> [!Note]  
> <span data-ttu-id="c22b5-113">Ai fini dell'efficienza, l'accesso alle code di completamento ([**struct \_ CQ**](riocqueue.md) ) e le code di richiesta (struct di **Rio \_ RQ** ) non sono protette dalle primitive di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="c22b5-113">For purposes of efficiency, access to the completion queues ([**RIO\_CQ**](riocqueue.md) structs) and request queues (**RIO\_RQ** structs) are not protected by synchronization primitives.</span></span> <span data-ttu-id="c22b5-114">Se è necessario accedere a una coda di completamento o di richiesta da più thread, l'accesso deve essere coordinato da una sezione critica, da un blocco Write reader sottile o da un meccanismo simile.</span><span class="sxs-lookup"><span data-stu-id="c22b5-114">If you need to access a completion or request queue from multiple threads, access should be coordinated by a critical section, slim reader write lock or similar mechanism.</span></span> <span data-ttu-id="c22b5-115">Questo blocco non è necessario per l'accesso da un singolo thread.</span><span class="sxs-lookup"><span data-stu-id="c22b5-115">This locking is not needed for access by a single thread.</span></span> <span data-ttu-id="c22b5-116">Thread diversi possono accedere a code di completamento/richieste separate senza blocchi.</span><span class="sxs-lookup"><span data-stu-id="c22b5-116">Different threads can access separate requests/completion queues without locks.</span></span> <span data-ttu-id="c22b5-117">La necessità di sincronizzazione avviene solo quando più thread tentano di accedere alla stessa coda.</span><span class="sxs-lookup"><span data-stu-id="c22b5-117">The need for synchronization occurs only when multiple threads try to access the same queue.</span></span> <span data-ttu-id="c22b5-118">La sincronizzazione è necessaria anche se più thread inviano e ricevono lo stesso socket perché le operazioni di invio e ricezione utilizzano la coda di richieste del socket.</span><span class="sxs-lookup"><span data-stu-id="c22b5-118">Synchronization is also required if multiple threads issue sends and receives on the same socket because the send and receive operations use the socket’s request queue.</span></span>

 

<span data-ttu-id="c22b5-119">Il typedef di [**Rio \_ RQ**](riocqueue.md) è definito nel file di intestazione *Mswsockdef. h* , che viene incluso automaticamente nel file di intestazione *mswsock. h* .</span><span class="sxs-lookup"><span data-stu-id="c22b5-119">The [**RIO\_RQ**](riocqueue.md) typedef is defined in the *Mswsockdef.h* header file which is automatically included in the *Mswsock.h* header file.</span></span> <span data-ttu-id="c22b5-120">Il file di intestazione *Mswsockdef. h* non deve mai essere utilizzato direttamente.</span><span class="sxs-lookup"><span data-stu-id="c22b5-120">The *Mswsockdef.h* header file should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="c22b5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c22b5-121">Requirements</span></span>



| <span data-ttu-id="c22b5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c22b5-122">Requirement</span></span> | <span data-ttu-id="c22b5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c22b5-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c22b5-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c22b5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c22b5-125">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c22b5-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="c22b5-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c22b5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c22b5-127">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c22b5-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="c22b5-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c22b5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c22b5-129"><dt>Mswsockdef. h (include mswsock. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c22b5-129"><dt>Mswsockdef.h (include Mswsock.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c22b5-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c22b5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c22b5-131">**RIOCreateRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="c22b5-131">**RIOCreateRequestQueue**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[<span data-ttu-id="c22b5-132">**RIOReceive**</span><span class="sxs-lookup"><span data-stu-id="c22b5-132">**RIOReceive**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[<span data-ttu-id="c22b5-133">**RIOReceiveEx**</span><span class="sxs-lookup"><span data-stu-id="c22b5-133">**RIOReceiveEx**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

<span data-ttu-id="c22b5-134">[**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c22b5-134">[**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c22b5-135">**RIOSend**</span><span class="sxs-lookup"><span data-stu-id="c22b5-135">**RIOSend**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

<span data-ttu-id="c22b5-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c22b5-136">[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c22b5-137">**WSASocket**</span><span class="sxs-lookup"><span data-stu-id="c22b5-137">**WSASocket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
</dt> </dl>

 

 
