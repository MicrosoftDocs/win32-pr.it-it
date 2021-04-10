---
description: Oltre a usare il callback della coda predefinito, è possibile scrivere una routine di callback personalizzata.
ms.assetid: 68781565-71a2-43bf-ad01-7c1cdc514f7b
title: Creazione di una routine di callback della coda personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a119836e994709ff2d0fa21e12489af947394119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883585"
---
# <a name="creating-a-custom-queue-callback-routine"></a><span data-ttu-id="797ff-103">Creazione di una routine di callback della coda personalizzata</span><span class="sxs-lookup"><span data-stu-id="797ff-103">Creating a Custom Queue Callback Routine</span></span>

<span data-ttu-id="797ff-104">Oltre a usare il callback della coda predefinito, è possibile scrivere una routine di callback personalizzata.</span><span class="sxs-lookup"><span data-stu-id="797ff-104">In addition to using the default queue callback, you can write a custom callback routine.</span></span> <span data-ttu-id="797ff-105">Questa funzione deve avere lo stesso formato di [*filecallback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="797ff-105">This function must have the same form as [*FileCallback*](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="797ff-106">Questa operazione è utile se è necessaria una routine di callback per gestire una notifica in un modo diverso da quello fornito dalla routine di callback della coda predefinita.</span><span class="sxs-lookup"><span data-stu-id="797ff-106">This is useful if you need a callback routine to handle a notification in a manner other than that provided by the default queue callback routine.</span></span>

<span data-ttu-id="797ff-107">Se è necessario modificare solo una piccola parte del comportamento predefinito della routine di callback della coda, è possibile creare una routine di callback personalizzata per filtrare le notifiche, gestendo solo quelle che richiedono un comportamento speciale e chiamando [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) per le altre.</span><span class="sxs-lookup"><span data-stu-id="797ff-107">If only a small portion of the default queue callback routine's behavior needs to be changed, you can create a custom callback routine to filter the notifications, handling only those that require special behavior and calling [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) for the others.</span></span>

<span data-ttu-id="797ff-108">Se, ad esempio, si desidera gestire in modo personalizzato gli errori di eliminazione dei file, è possibile creare una funzione di callback personalizzata, ovvero *callback*.</span><span class="sxs-lookup"><span data-stu-id="797ff-108">For example, if you wanted to custom-handle file delete errors, you could create a custom callback function, *MyCallback*.</span></span> <span data-ttu-id="797ff-109">Questa funzione intercetta ed elabora le [**notifiche \_ DELETEERROR di SPFILENOTIFY**](spfilenotify-deleteerror.md) e chiama la funzione di callback della coda predefinita per tutte le altre notifiche.</span><span class="sxs-lookup"><span data-stu-id="797ff-109">This function would intercept and process [**SPFILENOTIFY\_DELETEERROR**](spfilenotify-deleteerror.md) notifications, and call the default queue callback function for all other notifications.</span></span> <span data-ttu-id="797ff-110">Il *callback* restituisce un valore per le notifiche di errore Delete.</span><span class="sxs-lookup"><span data-stu-id="797ff-110">*MyCallback* returns a value for the delete error notifications.</span></span> <span data-ttu-id="797ff-111">Per tutte le altre notifiche, il *callback* passa qualsiasi valore che la routine di callback della coda predefinita ha restituito alla coda.</span><span class="sxs-lookup"><span data-stu-id="797ff-111">For all other notifications, *MyCallback* passes whatever value the default queue callback routine returned to the queue.</span></span>

<span data-ttu-id="797ff-112">Questo flusso di controllo è illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="797ff-112">This flow of control is illustrated in the following diagram.</span></span>

![frecce e caselle che mostrano il flusso di dati per la funzione di callback personalizzata](images/callback.png)

> [!IMPORTANT]
> <span data-ttu-id="797ff-114">Se la funzione di callback personalizzata chiama la routine di callback della coda predefinita, deve passare il puntatore void restituito da [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) o [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) alla routine di callback predefinita.</span><span class="sxs-lookup"><span data-stu-id="797ff-114">If the custom callback function calls the default queue callback routine, it must pass the void pointer returned by [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) to the default callback routine.</span></span>

 

 

 
