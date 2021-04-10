---
description: Poiché l'API di installazione non fornisce una routine di callback del cabinet predefinita, è necessario specificare una routine. La routine di callback necessaria per la funzione SetupIterateCabinet deve avere lo stesso formato di quelle a cui punta filecallback.
ms.assetid: 45a2690e-1db6-4a09-a141-9e68ebc2a6d8
title: Creazione di una routine di callback del cabinet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f25d59515a6afdd68cef4458868fbfb62335aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231840"
---
# <a name="creating-a-cabinet-callback-routine"></a><span data-ttu-id="0bf87-104">Creazione di una routine di callback del cabinet</span><span class="sxs-lookup"><span data-stu-id="0bf87-104">Creating a Cabinet Callback Routine</span></span>

<span data-ttu-id="0bf87-105">Poiché l'API di installazione non fornisce una routine di callback del cabinet predefinita, è necessario specificare una routine.</span><span class="sxs-lookup"><span data-stu-id="0bf87-105">Because the Setup API does not supply a default cabinet callback routine, you need to supply a routine.</span></span> <span data-ttu-id="0bf87-106">La routine di callback necessaria per la funzione [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) deve avere lo stesso formato di quelle a cui punta [filecallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="0bf87-106">The callback routine that the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function requires must have the same form as those pointed to by [FileCallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span>

<span data-ttu-id="0bf87-107">Di seguito è riportata la sintassi utilizzata da [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) per inviare una notifica alla routine di callback.</span><span class="sxs-lookup"><span data-stu-id="0bf87-107">Following is the syntax that [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) uses to send a notification to the callback routine.</span></span>

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //cabinet notification
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

<span data-ttu-id="0bf87-108">Il parametro *context* è un puntatore void a una variabile di contesto o a una struttura che può essere utilizzata dalla routine di callback per archiviare le informazioni che devono essere mantenute tra le chiamate successive alla routine di callback.</span><span class="sxs-lookup"><span data-stu-id="0bf87-108">The *Context* parameter is a void pointer to a context variable or structure that can be used by the callback routine to store information that needs to persist between subsequent calls to the callback routine.</span></span>

<span data-ttu-id="0bf87-109">Questa implementazione del contesto è specificata dalla routine di callback e non viene mai fatto riferimento o modificata da [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="0bf87-109">This context's implementation is specified by the callback routine, and it is never referenced or altered by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

<span data-ttu-id="0bf87-110">Il parametro *Notification* è un Unsigned Integer e sarà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0bf87-110">The *Notification* parameter is an unsigned integer and will be one of the following values.</span></span>



| <span data-ttu-id="0bf87-111">Notifica</span><span class="sxs-lookup"><span data-stu-id="0bf87-111">Notification</span></span>                                                        | <span data-ttu-id="0bf87-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bf87-112">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="0bf87-113">**SPFILENOTIFY \_ FILEextracted**</span><span class="sxs-lookup"><span data-stu-id="0bf87-113">**SPFILENOTIFY\_FILEEXTRACTED**</span></span>](spfilenotify-fileextracted.md)   | <span data-ttu-id="0bf87-114">Il file è stato estratto dal file CAB.</span><span class="sxs-lookup"><span data-stu-id="0bf87-114">The file has been extracted from the cabinet.</span></span>      |
| [<span data-ttu-id="0bf87-115">**\_FILEINCABINET SPFILENOTIFY**</span><span class="sxs-lookup"><span data-stu-id="0bf87-115">**SPFILENOTIFY\_FILEINCABINET**</span></span>](spfilenotify-fileincabinet.md)   | <span data-ttu-id="0bf87-116">Viene rilevato un file nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="0bf87-116">A file is encountered in the cabinet.</span></span>              |
| [<span data-ttu-id="0bf87-117">**\_NEEDNEWCABINET SPFILENOTIFY**</span><span class="sxs-lookup"><span data-stu-id="0bf87-117">**SPFILENOTIFY\_NEEDNEWCABINET**</span></span>](spfilenotify-neednewcabinet.md) | <span data-ttu-id="0bf87-118">Il file corrente viene continuato nel file CAB successivo.</span><span class="sxs-lookup"><span data-stu-id="0bf87-118">The current file is continued in the next cabinet.</span></span> |



 

<span data-ttu-id="0bf87-119">I due parametri finali, *param1* e *param2*, sono anche interi senza segno e contengono informazioni aggiuntive relative alla notifica.</span><span class="sxs-lookup"><span data-stu-id="0bf87-119">The final two parameters, *Param1* and *Param2*, are also unsigned integers and contain additional information relevant to the notification.</span></span> <span data-ttu-id="0bf87-120">Per ulteriori informazioni sulle notifiche inviate da [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta), vedere la pagina relativa alle [notifiche dei file CAB](cabinet-file-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="0bf87-120">For more information about the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta), see [Cabinet File Notifications](cabinet-file-notifications.md).</span></span>

<span data-ttu-id="0bf87-121">Una \_ routine di callback di notifica file SP \_ \_ restituisce un Unsigned Integer.</span><span class="sxs-lookup"><span data-stu-id="0bf87-121">A SP\_FILE\_NOTIFY\_CALLBACK routine returns an unsigned integer.</span></span> <span data-ttu-id="0bf87-122">La routine di callback del cabinet deve restituire uno dei valori seguenti a seconda della notifica.</span><span class="sxs-lookup"><span data-stu-id="0bf87-122">The cabinet callback routine should return one of the following values depending on the notification.</span></span>

<span data-ttu-id="0bf87-123">Per la \_ notifica SPFILENOTIFY FILEINCABINET, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) prevede che uno dei valori seguenti venga restituito dalla routine di callback.</span><span class="sxs-lookup"><span data-stu-id="0bf87-123">For the SPFILENOTIFY\_FILEINCABINET notification, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) expects one of the following values to be returned by the callback routine.</span></span>



| <span data-ttu-id="0bf87-124">Valore</span><span class="sxs-lookup"><span data-stu-id="0bf87-124">Value</span></span>         | <span data-ttu-id="0bf87-125">Significato</span><span class="sxs-lookup"><span data-stu-id="0bf87-125">Meaning</span></span>                   |
|---------------|---------------------------|
| <span data-ttu-id="0bf87-126">\_interruzione FILEOP</span><span class="sxs-lookup"><span data-stu-id="0bf87-126">FILEOP\_ABORT</span></span> | <span data-ttu-id="0bf87-127">Interrompi elaborazione del cabinet.</span><span class="sxs-lookup"><span data-stu-id="0bf87-127">Abort cabinet processing.</span></span> |
| <span data-ttu-id="0bf87-128">\_doit FILEOP</span><span class="sxs-lookup"><span data-stu-id="0bf87-128">FILEOP\_DOIT</span></span>  | <span data-ttu-id="0bf87-129">Estrarre il file corrente.</span><span class="sxs-lookup"><span data-stu-id="0bf87-129">Extract the current file.</span></span> |
| <span data-ttu-id="0bf87-130">\_Ignora FILEOP</span><span class="sxs-lookup"><span data-stu-id="0bf87-130">FILEOP\_SKIP</span></span>  | <span data-ttu-id="0bf87-131">Ignora il file corrente.</span><span class="sxs-lookup"><span data-stu-id="0bf87-131">Skip the current file.</span></span>    |



 

<span data-ttu-id="0bf87-132">Per \_ \_ le notifiche fileestrate SPFILENOTIFY NEEDNEWCABINET e SPFILENOTIFY, **SetupIterateCabinet** prevede che venga restituito uno dei valori seguenti dalla routine di callback.</span><span class="sxs-lookup"><span data-stu-id="0bf87-132">For SPFILENOTIFY\_NEEDNEWCABINET and SPFILENOTIFY\_FILEEXTRACTED notifications, **SetupIterateCabinet** expects one of the following values to be returned by the callback routine.</span></span>



| <span data-ttu-id="0bf87-133">Valore</span><span class="sxs-lookup"><span data-stu-id="0bf87-133">Value</span></span>      | <span data-ttu-id="0bf87-134">Significato</span><span class="sxs-lookup"><span data-stu-id="0bf87-134">Meaning</span></span>                                                                                                                                                                                                                           |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bf87-135">Nessun \_ errore</span><span class="sxs-lookup"><span data-stu-id="0bf87-135">NO\_ERROR</span></span>  | <span data-ttu-id="0bf87-136">Non è stato rilevato alcun errore, continuare l'elaborazione del file CAB.</span><span class="sxs-lookup"><span data-stu-id="0bf87-136">No error was encountered, continue processing the cabinet.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="0bf87-137">ERRORE \_ xxx</span><span class="sxs-lookup"><span data-stu-id="0bf87-137">ERROR\_XXX</span></span> | <span data-ttu-id="0bf87-138">Si è verificato un errore del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="0bf87-138">An error of the specified type occurred.</span></span> <span data-ttu-id="0bf87-139">La funzione [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) restituirà **false** e il codice di errore specificato verrà restituito da una chiamata a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="0bf87-139">The [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function will return **FALSE**, and the specified error code will be returned by a call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> |



 

<span data-ttu-id="0bf87-140">Se la routine di callback restituisce FILEOP \_ doit, la routine deve fornire anche un percorso di destinazione completo.</span><span class="sxs-lookup"><span data-stu-id="0bf87-140">If the callback routine returns FILEOP\_DOIT, the routine must also provide a full target path.</span></span> <span data-ttu-id="0bf87-141">Per altre informazioni, vedere [**SPFILENOTIFY \_ FILEINCABINET**](spfilenotify-fileincabinet.md).</span><span class="sxs-lookup"><span data-stu-id="0bf87-141">For more information see [**SPFILENOTIFY\_FILEINCABINET**](spfilenotify-fileincabinet.md).</span></span>

 

 
