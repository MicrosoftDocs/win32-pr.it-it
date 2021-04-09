---
title: Funzioni di ripristino e riavvio dell'applicazione
description: Il ripristino e il riavvio dell'applicazione definiscono le funzioni seguenti
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f9f5fb41f2ef694b4d99044a8756ff0bb66c3f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118146"
---
# <a name="application-recovery-and-restart-functions"></a><span data-ttu-id="bc993-103">Funzioni di ripristino e riavvio dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="bc993-103">Application Recovery and Restart Functions</span></span>

<span data-ttu-id="bc993-104">Il ripristino e il riavvio dell'applicazione definiscono le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="bc993-104">Application Recovery and Restart defines the following functions:</span></span>



| <span data-ttu-id="bc993-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="bc993-105">Function</span></span>                                                                               | <span data-ttu-id="bc993-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc993-106">Description</span></span>                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc993-107">**ApplicationRecoveryFinished**</span><span class="sxs-lookup"><span data-stu-id="bc993-107">**ApplicationRecoveryFinished**</span></span>](/windows/win32/api/winbase/nf-winbase-applicationrecoveryfinished)                     | <span data-ttu-id="bc993-108">Indica che l'applicazione chiamante ha completato il ripristino dei dati.</span><span class="sxs-lookup"><span data-stu-id="bc993-108">Indicates that the calling application has completed its data recovery.</span></span>                    |
| [<span data-ttu-id="bc993-109">**ApplicationRecoveryInProgress**</span><span class="sxs-lookup"><span data-stu-id="bc993-109">**ApplicationRecoveryInProgress**</span></span>](/windows/win32/api/winbase/nf-winbase-applicationrecoveryinprogress)                 | <span data-ttu-id="bc993-110">Indica che l'applicazione chiamante sta continuando a ripristinare i dati.</span><span class="sxs-lookup"><span data-stu-id="bc993-110">Indicates that the calling application is continuing to recover data.</span></span>                      |
| [<span data-ttu-id="bc993-111">**GetApplicationRecoveryCallback**</span><span class="sxs-lookup"><span data-stu-id="bc993-111">**GetApplicationRecoveryCallback**</span></span>](/windows/win32/api/winbase/nf-winbase-getapplicationrecoverycallback)               | <span data-ttu-id="bc993-112">Recupera un puntatore alla routine di callback di ripristino registrata per il processo specificato.</span><span class="sxs-lookup"><span data-stu-id="bc993-112">Retrieves a pointer to the recovery callback routine registered for the specified process.</span></span> |
| [<span data-ttu-id="bc993-113">**GetApplicationRestartSettings**</span><span class="sxs-lookup"><span data-stu-id="bc993-113">**GetApplicationRestartSettings**</span></span>](/windows/win32/api/winbase/nf-winbase-getapplicationrestartsettings)                 | <span data-ttu-id="bc993-114">Recupera le informazioni di riavvio registrate per il processo specificato.</span><span class="sxs-lookup"><span data-stu-id="bc993-114">Retrieves the restart information registered for the specified process.</span></span>                    |
| [<span data-ttu-id="bc993-115">**RegisterApplicationRecoveryCallback**</span><span class="sxs-lookup"><span data-stu-id="bc993-115">**RegisterApplicationRecoveryCallback**</span></span>](/windows/win32/api/winbase/nf-winbase-registerapplicationrecoverycallback)     | <span data-ttu-id="bc993-116">Registra l'istanza attiva di un'applicazione per il ripristino.</span><span class="sxs-lookup"><span data-stu-id="bc993-116">Registers the active instance of an application for recovery.</span></span>                              |
| [<span data-ttu-id="bc993-117">**RegisterApplicationRestart**</span><span class="sxs-lookup"><span data-stu-id="bc993-117">**RegisterApplicationRestart**</span></span>](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart)                       | <span data-ttu-id="bc993-118">Registra l'istanza attiva di un'applicazione per il riavvio.</span><span class="sxs-lookup"><span data-stu-id="bc993-118">Registers the active instance of an application for restart.</span></span>                               |
| [<span data-ttu-id="bc993-119">**UnregisterApplicationRecoveryCallback**</span><span class="sxs-lookup"><span data-stu-id="bc993-119">**UnregisterApplicationRecoveryCallback**</span></span>](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrecoverycallback) | <span data-ttu-id="bc993-120">Consente di rimuovere l'istanza attiva di un'applicazione dall'elenco di ripristino.</span><span class="sxs-lookup"><span data-stu-id="bc993-120">Removes the active instance of an application from the recovery list.</span></span>                      |
| [<span data-ttu-id="bc993-121">**UnregisterApplicationRestart**</span><span class="sxs-lookup"><span data-stu-id="bc993-121">**UnregisterApplicationRestart**</span></span>](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrestart)                   | <span data-ttu-id="bc993-122">Rimuove l'istanza attiva di un'applicazione dall'elenco di riavvio.</span><span class="sxs-lookup"><span data-stu-id="bc993-122">Removes the active instance of an application from the restart list.</span></span>                       |



 

 

 