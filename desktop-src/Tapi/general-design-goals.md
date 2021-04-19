---
description: L'elenco seguente contiene gli obiettivi di progettazione dell'MSP di TAPI.
ms.assetid: 286b96c1-047b-4cb9-a189-af2818cfec58
title: Obiettivi di progettazione generali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052bbf607e71986678acca29d17d587bfa5bccf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308082"
---
# <a name="general-design-goals"></a><span data-ttu-id="ef4b7-103">Obiettivi di progettazione generali</span><span class="sxs-lookup"><span data-stu-id="ef4b7-103">General Design Goals</span></span>

<span data-ttu-id="ef4b7-104">L'elenco seguente contiene gli obiettivi di progettazione dell'MSP di TAPI.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-104">The following list contains the TAPI MSP design goals.</span></span>

-   <span data-ttu-id="ef4b7-105">Le classi base sono state mantenute semplici, con membri e metodi introdotti solo quando strettamente necessario.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-105">Base classes have been kept simple, with members and methods introduced only when absolutely necessary.</span></span>
-   <span data-ttu-id="ef4b7-106">Ereditarietà semplice.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-106">Simple inheritance.</span></span> <span data-ttu-id="ef4b7-107">Nessuna ereditarietà multipla tra le classi, sebbene venga utilizzata più ereditarietà per le interfacce.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-107">No multiple inheritance among classes, although multiple inheritance is used for the interfaces.</span></span>
-   <span data-ttu-id="ef4b7-108">Il blocco si verifica solo in una direzione per impedire il deadlock.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-108">Locking happens only in one direction to prevent deadlock.</span></span> <span data-ttu-id="ef4b7-109">I metodi sull'oggetto chiamata che richiedono il blocco sulla chiamata potrebbero chiamare metodi sul flusso che richiedono il blocco sul flusso.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-109">Methods on the call object that require the lock on the call might call methods on the stream that require the lock on the stream.</span></span> <span data-ttu-id="ef4b7-110">Tuttavia, i metodi nel flusso che richiedono il blocco sul flusso non chiameranno mai un metodo sulla chiamata che richiede un blocco sulla chiamata.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-110">However, methods on the stream that require the lock on the stream will never call a method on the call that requires a lock on the call.</span></span>
-   <span data-ttu-id="ef4b7-111">RefCounts vengono usati per proteggere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-111">Refcounts are used to protect access.</span></span> <span data-ttu-id="ef4b7-112">Tutti i callback inviati al pool di thread contengono refCounts.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-112">All callbacks posted to the thread pool hold refcounts.</span></span> <span data-ttu-id="ef4b7-113">Refcount viene annullato quando l'attesa viene annullata.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-113">The refcount is canceled when the wait is canceled.</span></span> <span data-ttu-id="ef4b7-114">L'oggetto Address ha refCounts nei terminali.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-114">The Address object has refcounts on Terminals.</span></span> <span data-ttu-id="ef4b7-115">Gli oggetti Call hanno refCounts sull'indirizzo e sui flussi.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-115">Call objects have refcounts on the Address and on Streams.</span></span> <span data-ttu-id="ef4b7-116">Gli oggetti Stream hanno refCounts su chiamate e terminali.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-116">Stream objects have refcounts on Calls and Terminals.</span></span> <span data-ttu-id="ef4b7-117">I terminali hanno refCounts sui flussi.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-117">The Terminals have refcounts on Streams.</span></span> <span data-ttu-id="ef4b7-118">Il refCounts circolare si interrompe quando viene chiamato il metodo Shutdown sugli oggetti Address e call.</span><span class="sxs-lookup"><span data-stu-id="ef4b7-118">The circular refcounts break when the shutdown method on the Address and Call objects is called.</span></span>

 

 



