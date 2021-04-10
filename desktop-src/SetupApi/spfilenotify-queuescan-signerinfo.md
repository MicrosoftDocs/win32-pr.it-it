---
description: La \_ notifica SPFILENOTIFY QUEUESCAN \_ SIGNERINFO viene inviata a una routine di callback da SetupScanFileQueue per ogni nodo nella coda secondaria di copia della coda di file.
ms.assetid: 5b22e8ba-9a18-461b-bad7-b2d76f83d7f3
title: Messaggio SPFILENOTIFY_QUEUESCAN_SIGNERINFO (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29bf9e9c7e0ab76303d8c2fb21a0109ec60358f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967864"
---
# <a name="spfilenotify_queuescan_signerinfo-message"></a><span data-ttu-id="21089-103">\_ \_ Messaggio SIGNERINFO QUEUESCAN SPFILENOTIFY</span><span class="sxs-lookup"><span data-stu-id="21089-103">SPFILENOTIFY\_QUEUESCAN\_SIGNERINFO message</span></span>

<span data-ttu-id="21089-104">La notifica **SPFILENOTIFY \_ QUEUESCAN \_ SIGNERINFO** viene inviata a una routine di callback da [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) per ogni nodo nella coda secondaria di copia della coda di file.</span><span class="sxs-lookup"><span data-stu-id="21089-104">The **SPFILENOTIFY\_QUEUESCAN\_SIGNERINFO** notification is sent to a callback routine by [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) for each node in the copy subqueue of the file queue.</span></span> <span data-ttu-id="21089-105">Questo errore si verifica solo se è stata chiamata la funzione **SetupScanFileQueue** specificando il flag SPQ \_ Scan \_ use \_ callback \_ SIGNERINFO.</span><span class="sxs-lookup"><span data-stu-id="21089-105">This only occurs if the **SetupScanFileQueue** function was called specifying the flag SPQ\_SCAN\_USE\_CALLBACK\_SIGNERINFO.</span></span> <span data-ttu-id="21089-106">Disponibile a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="21089-106">Available starting with Windows XP.</span></span>


```C++
SPFILENOTIFY_QUEUESCAN_SIGNERINFO
  Param1 = (PFILEPATHS_SIGNERINFO) Filepaths;
            
```



## <a name="parameters"></a><span data-ttu-id="21089-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="21089-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21089-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="21089-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="21089-109">Puntatore a una struttura [**\_ SIGNERINFO filePaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) .</span><span class="sxs-lookup"><span data-stu-id="21089-109">Pointer to a [**FILEPATHS\_SIGNERINFO**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_signerinfo_a) structure.</span></span> <span data-ttu-id="21089-110">Il membro di **destinazione** è il nome del file di destinazione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="21089-110">The **Target** member is the filename of the target file on the system.</span></span> <span data-ttu-id="21089-111">Il membro di **origine** è il percorso previsto del file di origine.</span><span class="sxs-lookup"><span data-stu-id="21089-111">The **Source** member is the expected path of the source file.</span></span> <span data-ttu-id="21089-112">Il membro **Win32Error** è l'errore di firma.</span><span class="sxs-lookup"><span data-stu-id="21089-112">The **Win32Error** member is the signing error.</span></span> <span data-ttu-id="21089-113">Se la routine di callback restituisce **Win32Error**= = nessun errore, vengono restituite informazioni sulla firma \_ .</span><span class="sxs-lookup"><span data-stu-id="21089-113">Signature information is returned if the callback routine returns **Win32Error**==NO\_ERROR.</span></span> <span data-ttu-id="21089-114">Il membro **DigitalSigner** è il firmatario digitale.</span><span class="sxs-lookup"><span data-stu-id="21089-114">The **DigitalSigner** member is the digital signer.</span></span> <span data-ttu-id="21089-115">Il membro della **versione** è la versione.</span><span class="sxs-lookup"><span data-stu-id="21089-115">The **Version** member is the version.</span></span> <span data-ttu-id="21089-116">**CatalogFile** è il file di catalogo.</span><span class="sxs-lookup"><span data-stu-id="21089-116">The **CatalogFile** is the catalog file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21089-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21089-117">Return value</span></span>

<span data-ttu-id="21089-118">La routine di callback deve restituire un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="21089-118">The callback routine should return a [system error code](/windows/desktop/Debug/system-error-codes).</span></span>

<span data-ttu-id="21089-119">Se la routine di callback non restituisce alcun \_ errore, l'analisi della coda continua e restituisce se la routine restituisce un altro codice di errore, l'analisi della coda si interrompe e [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="21089-119">If the callback routine returns NO\_ERROR, the queue scan continues, and returns If the routine returns any other error code, the queue scan aborts and [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) returns **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="21089-120">Questa notifica non viene gestita dalla funzione [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .</span><span class="sxs-lookup"><span data-stu-id="21089-120">This notification is not handled by the [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="21089-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21089-121">Requirements</span></span>



| <span data-ttu-id="21089-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="21089-122">Requirement</span></span> | <span data-ttu-id="21089-123">Valore</span><span class="sxs-lookup"><span data-stu-id="21089-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21089-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21089-124">Minimum supported client</span></span><br/> | <span data-ttu-id="21089-125">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="21089-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="21089-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21089-126">Minimum supported server</span></span><br/> | <span data-ttu-id="21089-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="21089-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="21089-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21089-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="21089-129"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="21089-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21089-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21089-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21089-131">Overview</span><span class="sxs-lookup"><span data-stu-id="21089-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="21089-132">Notifications</span><span class="sxs-lookup"><span data-stu-id="21089-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="21089-133">**SetupScanFileQueue**</span><span class="sxs-lookup"><span data-stu-id="21089-133">**SetupScanFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

