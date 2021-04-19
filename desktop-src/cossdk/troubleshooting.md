---
description: Risoluzione dei problemi
ms.assetid: e3576161-fc04-47e0-b6b8-75af33fe87ff
title: Risoluzione dei problemi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5dcc9814353f9c19a8f5005a3ee8fe461c37a93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304933"
---
# <a name="troubleshooting"></a><span data-ttu-id="a4250-103">Risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="a4250-103">Troubleshooting</span></span>

<span data-ttu-id="a4250-104">Se si verificano problemi durante la diagnosi degli errori dell'applicazione, vedere i suggerimenti per la risoluzione dei problemi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a4250-104">If you are having trouble diagnosing your application errors, refer to the following of troubleshooting tips:</span></span>

-   <span data-ttu-id="a4250-105">Verificare che il Distributed Transaction Coordinator (DTC) sia in esecuzione in tutti i server.</span><span class="sxs-lookup"><span data-stu-id="a4250-105">Make sure that the Distributed Transaction Coordinator (DTC) is running on all servers.</span></span>
-   <span data-ttu-id="a4250-106">Controllare la comunicazione di rete eseguendo il primo test in un computer locale per verificare che l'applicazione funzioni.</span><span class="sxs-lookup"><span data-stu-id="a4250-106">Check network communication by first testing on a local computer to verify that the application works.</span></span> <span data-ttu-id="a4250-107">Se si esegue TCP/IP nella rete, è possibile utilizzare l'utilità ping.exe per verificare che i computer siano in rete.</span><span class="sxs-lookup"><span data-stu-id="a4250-107">If you are running TCP/IP on your network, you can use the ping.exe utility to verify that the machines are on the network.</span></span>
-   <span data-ttu-id="a4250-108">Verificare che SQL e DTC si trovino nello stesso computer o che il programma di configurazione del client DTC specifichi che DTC si trova in un altro computer.</span><span class="sxs-lookup"><span data-stu-id="a4250-108">Make sure that SQL and DTC are located on the same computer or that the DTC Client Configuration program specifies that the DTC is on another computer.</span></span> <span data-ttu-id="a4250-109">In caso contrario, SQLConnect restituirà un errore internamente quando viene chiamato da un componente transazionale.</span><span class="sxs-lookup"><span data-stu-id="a4250-109">If not, SQLConnect will return an error internally when called from a transactional component.</span></span>
-   <span data-ttu-id="a4250-110">Impostare il timeout della transazione su un numero superiore a quello predefinito di 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="a4250-110">Set the transaction time-out to a higher number than the default 60 seconds.</span></span> <span data-ttu-id="a4250-111">Una volta trascorso il timeout della transazione, COM+ interrompe la transazione.</span><span class="sxs-lookup"><span data-stu-id="a4250-111">After the transaction time-out has elapsed, COM+ aborts the transaction.</span></span> <span data-ttu-id="a4250-112">Tutte le chiamate successive al componente vengono restituite immediatamente con contesto \_ E \_ interrotto.</span><span class="sxs-lookup"><span data-stu-id="a4250-112">All subsequent calls to the component return immediately with CONTEXT\_E\_ABORTED.</span></span>
-   <span data-ttu-id="a4250-113">Verificare che i driver ODBC siano thread-safe e che non abbiano affinità di thread.</span><span class="sxs-lookup"><span data-stu-id="a4250-113">Make sure that your ODBC drivers are thread-safe and do not have thread affinity.</span></span>
-   <span data-ttu-id="a4250-114">Se si verificano problemi durante il funzionamento di un'applicazione su più server, riavviare il client e quindi verificare che il controller di dominio sia configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="a4250-114">If you have difficulty getting an application to work over several servers, reboot the client and then verify that your domain controller is configured properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4250-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a4250-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4250-116">Criteri di isolamento degli errori e FailFast</span><span class="sxs-lookup"><span data-stu-id="a4250-116">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="a4250-117">Individuazione dell'origine di un errore</span><span class="sxs-lookup"><span data-stu-id="a4250-117">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="a4250-118">Modalità di modifica dei valori restituiti da COM+</span><span class="sxs-lookup"><span data-stu-id="a4250-118">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="a4250-119">Interpretazione dei codici di errore</span><span class="sxs-lookup"><span data-stu-id="a4250-119">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="a4250-120">Strategie per la gestione degli errori in COM+</span><span class="sxs-lookup"><span data-stu-id="a4250-120">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> </dl>

 

 



