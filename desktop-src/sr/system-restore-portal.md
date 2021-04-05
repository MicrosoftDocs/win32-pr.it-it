---
title: Ripristino configurazione di sistema
description: Imposta i punti di ripristino del sistema e monitora le modifiche del sistema chiave da un programma per consentire il rollback del sistema a uno stato precedente. Scrivere codice di ripristino automatico o script WMI per ripristinare lo stato del sistema in un punto di ripristino registrato.
ms.assetid: 6861eedc-2bd9-49c7-8682-ea557fa29d28
keywords:
- Ripristino configurazione di sistema
- Ripristino configurazione di sistema, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bdc4555171ad867f6e6b925144d9ed673ffc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118043"
---
# <a name="system-restore"></a><span data-ttu-id="1b279-106">Ripristino configurazione di sistema</span><span class="sxs-lookup"><span data-stu-id="1b279-106">System Restore</span></span>

## <a name="purpose"></a><span data-ttu-id="1b279-107">Scopo</span><span class="sxs-lookup"><span data-stu-id="1b279-107">Purpose</span></span>

<span data-ttu-id="1b279-108">Ripristino configurazione di sistema monitora e registra automaticamente le modifiche di sistema principali nel computer di un utente.</span><span class="sxs-lookup"><span data-stu-id="1b279-108">System Restore automatically monitors and records key system changes on a user's computer.</span></span> <span data-ttu-id="1b279-109">È progettato per ridurre i costi di supporto e aumentare la soddisfazione dei clienti consentendo a un utente di annullare una modifica che potrebbe avere causato un problema con il sistema o ripristinare un giorno in cui il sistema è stato in grado di garantire prestazioni ottimali.</span><span class="sxs-lookup"><span data-stu-id="1b279-109">It is designed to reduce support costs and increase customer satisfaction by enabling a user to undo a change that may have caused a problem with the system, or revert to a day when the system was performing optimally.</span></span>

> [!Note]  
> <span data-ttu-id="1b279-110">La seguente documentazione è destinata agli sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="1b279-110">The following documentation is targeted for developers.</span></span> <span data-ttu-id="1b279-111">Per informazioni sull'utilizzo di ripristino configurazione di sistema da parte dell'utente finale, vedere [che cos'è ripristino configurazione di sistema?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)</span><span class="sxs-lookup"><span data-stu-id="1b279-111">If you are an end-user looking for information on how to use System Restore, see [What Is System Restore?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="1b279-112">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="1b279-112">Developer audience</span></span>

<span data-ttu-id="1b279-113">L'API di ripristino del sistema è progettata per l'uso da parte dei programmatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="1b279-113">The System Restore API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="1b279-114">Per utilizzare l'interfaccia di scripting, è necessaria una certa familiarità con Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1b279-114">A familiarity with Windows Management Instrumentation (WMI) is required to use the scripting interface.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="1b279-115">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="1b279-115">Run-time requirements</span></span>

<span data-ttu-id="1b279-116">L'API ripristino di sistema è supportata nei sistemi operativi client a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1b279-116">The System Restore API is supported on client operating systems starting with Windows XP.</span></span> <span data-ttu-id="1b279-117">Per informazioni sui sistemi operativi necessari per usare un particolare elemento API, vedere la sezione requisiti della relativa documentazione.</span><span class="sxs-lookup"><span data-stu-id="1b279-117">For information about which operating systems are required to use a particular API element, see the Requirements section of its documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1b279-118">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="1b279-118">In this section</span></span>



| <span data-ttu-id="1b279-119">Argomento</span><span class="sxs-lookup"><span data-stu-id="1b279-119">Topic</span></span>                                                | <span data-ttu-id="1b279-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b279-120">Description</span></span>                                                                    |
|------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="1b279-121">Overview</span><span class="sxs-lookup"><span data-stu-id="1b279-121">Overview</span></span>](about-system-restore.md)<br/>      | <span data-ttu-id="1b279-122">Panoramica del funzionamento del ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="1b279-122">An overview of how System Restore works.</span></span><br/>                            |
| [<span data-ttu-id="1b279-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="1b279-123">Reference</span></span>](system-restore-reference.md)<br/> | <span data-ttu-id="1b279-124">Documentazione delle funzioni, delle strutture e delle classi di ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="1b279-124">Documentation of System Restore functions, structures, and classes.</span></span><br/> |
| [<span data-ttu-id="1b279-125">Esempi</span><span class="sxs-lookup"><span data-stu-id="1b279-125">Samples</span></span>](using-system-restore.md)<br/>       | <span data-ttu-id="1b279-126">Programma di esempio scritto in C.</span><span class="sxs-lookup"><span data-stu-id="1b279-126">A sample program written in C.</span></span><br/>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="1b279-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1b279-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b279-128">WMI</span><span class="sxs-lookup"><span data-stu-id="1b279-128">WMI</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

