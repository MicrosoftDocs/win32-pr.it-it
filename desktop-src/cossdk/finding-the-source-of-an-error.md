---
description: Individuazione dell'origine di un errore
ms.assetid: d7287cf1-9501-4d37-b022-b56c8008220c
title: Individuazione dell'origine di un errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b505981f12a6f8b23adc22e92cfc7b7c4b77b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049259"
---
# <a name="finding-the-source-of-an-error"></a><span data-ttu-id="eb4c1-103">Individuazione dell'origine di un errore</span><span class="sxs-lookup"><span data-stu-id="eb4c1-103">Finding the Source of an Error</span></span>

<span data-ttu-id="eb4c1-104">È possibile diagnosticare l'origine e ottenere una descrizione degli errori dell'applicazione utilizzando COM+ e altri strumenti.</span><span class="sxs-lookup"><span data-stu-id="eb4c1-104">You can diagnose the source and obtain a description of application errors by using COM+ and other tools.</span></span> <span data-ttu-id="eb4c1-105">Se si rileva che l'errore dell'applicazione è causato da COM+, è possibile interpretare il messaggio di errore visualizzando il file Winerror. h o utilizzando l'utilità Microsoft Visual C++ Error.</span><span class="sxs-lookup"><span data-stu-id="eb4c1-105">If you discover that the application error is caused by COM+, you can interpret the error message viewing the Winerror.h file or by using the Microsoft Visual C++ error utility.</span></span>

<span data-ttu-id="eb4c1-106">Se l'applicazione server non riesce o causa un comportamento imprevisto, è necessario innanzitutto determinare dove si è verificato l'errore.</span><span class="sxs-lookup"><span data-stu-id="eb4c1-106">If your server application is failing or causing unexpected behavior, you must first determine where the error occurred.</span></span> <span data-ttu-id="eb4c1-107">Il sistema Visualizzatore eventi tiene traccia degli eventi dell'applicazione, della sicurezza e del sistema.</span><span class="sxs-lookup"><span data-stu-id="eb4c1-107">The system Event Viewer tracks application, security, and system events.</span></span> <span data-ttu-id="eb4c1-108">Molti errori "invisibile" vengono registrati qui.</span><span class="sxs-lookup"><span data-stu-id="eb4c1-108">Many "silent" errors are recorded here.</span></span> <span data-ttu-id="eb4c1-109">Tuttavia, non tutti gli errori vengono visualizzati nel Visualizzatore eventi.</span><span class="sxs-lookup"><span data-stu-id="eb4c1-109">However, not all errors are shown in the Event Viewer.</span></span>

<span data-ttu-id="eb4c1-110">Prima di tutto, è necessario fare riferimento al registro applicazioni nel Visualizzatore eventi per controllare l'applicazione associata al messaggio di evento.</span><span class="sxs-lookup"><span data-stu-id="eb4c1-110">You should first refer to the application log in the Event Viewer to check the application associated with the event message.</span></span> <span data-ttu-id="eb4c1-111">Poiché è inoltre possibile archiviare i registri eventi, è possibile tenere traccia di una cronologia eventi dell'errore. Se si fa doppio clic su una voce nel log, viene attivata una pagina **Proprietà evento** che fornisce ulteriori informazioni sull'evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="eb4c1-111">(Because you can also archive event logs, you can track an event history of the error.) Double-clicking an entry in your log activates an **Event Properties** page, which provides further information about the system event.</span></span>

<span data-ttu-id="eb4c1-112">Per ulteriori informazioni sul debug di un'applicazione COM+, vedere [debug di applicazioni com+](debugging-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="eb4c1-112">For more information on debugging a COM+ application, see [Debugging COM+ Applications](debugging-com--applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb4c1-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eb4c1-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb4c1-114">Criteri di isolamento degli errori e FailFast</span><span class="sxs-lookup"><span data-stu-id="eb4c1-114">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="eb4c1-115">Modalità di modifica dei valori restituiti da COM+</span><span class="sxs-lookup"><span data-stu-id="eb4c1-115">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="eb4c1-116">Interpretazione dei codici di errore</span><span class="sxs-lookup"><span data-stu-id="eb4c1-116">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="eb4c1-117">Strategie per la gestione degli errori in COM+</span><span class="sxs-lookup"><span data-stu-id="eb4c1-117">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="eb4c1-118">Risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="eb4c1-118">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



