---
title: Informazioni su WER
description: Segnalazione errori Windows (WER) è un'infrastruttura di feedback basata su eventi flessibile progettata per raccogliere informazioni sui problemi hardware e software che Windows è in grado di rilevare, segnalare le informazioni a Microsoft e fornire agli utenti le soluzioni disponibili. Per informazioni sui miglioramenti apportati a WER, vedere Novità di WER.
ms.assetid: d26b3d2a-51cf-41d9-936b-f1b45778ea61
keywords:
- Segnalazione errori Windows Segnalazione errori Windows, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37ab7622c3e0b3a7bebff64e6c8373f2d163ba23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330903"
---
# <a name="about-wer"></a><span data-ttu-id="a1366-105">Informazioni su WER</span><span class="sxs-lookup"><span data-stu-id="a1366-105">About WER</span></span>

<span data-ttu-id="a1366-106">Segnalazione errori Windows (WER) è un'infrastruttura di feedback basata su eventi flessibile progettata per raccogliere informazioni sui problemi hardware e software che Windows è in grado di rilevare, segnalare le informazioni a Microsoft e fornire agli utenti le soluzioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="a1366-106">Windows Error Reporting (WER) is a flexible event-based feedback infrastructure designed to gather information about the hardware and software problems that Windows can detect, report the information to Microsoft, and provide users with any available solutions.</span></span> <span data-ttu-id="a1366-107">Per informazioni sui miglioramenti apportati a WER, vedere Novità di [wer](what-s-new-in-wer.md).</span><span class="sxs-lookup"><span data-stu-id="a1366-107">For information about the improvements to WER, see [What's New in WER](what-s-new-in-wer.md).</span></span>

<span data-ttu-id="a1366-108">A partire da Windows Vista, Windows fornisce un arresto anomalo, nessuna risposta e segnalazione errori del kernel per impostazione predefinita senza richiedere modifiche all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a1366-108">Beginning with Windows Vista, Windows provides crash, no response, and kernel fault error reporting by default without requiring changes to your application.</span></span> <span data-ttu-id="a1366-109">Le applicazioni usano invece l'API WER per generare segnalazioni di errori per problemi specifici dell'applicazione che non sono correlati a arresti anomali, non risposte o errori del kernel.</span><span class="sxs-lookup"><span data-stu-id="a1366-109">Applications instead use the WER API to generate error reports for application-specific issues that are not related to crashes, non-responses, or kernel faults.</span></span>

<span data-ttu-id="a1366-110">Per generare segnalazioni di errori per problemi specifici dell'applicazione, è necessario che l'applicazione crei una breve descrizione del problema utilizzando alcune informazioni di base denominate *parametri del report*.</span><span class="sxs-lookup"><span data-stu-id="a1366-110">To generate error reports for application-specific issues, the application must create a short description of the problem using a few basic pieces of information called *report parameters*.</span></span> <span data-ttu-id="a1366-111">I parametri del report includono informazioni quali il nome dell'applicazione, la versione dell'applicazione, il nome del modulo, la versione del modulo e il codice di errore.</span><span class="sxs-lookup"><span data-stu-id="a1366-111">Report parameters include information such as the application name, application version, module name, module version, and error code.</span></span> <span data-ttu-id="a1366-112">La combinazione di questi parametri del report descrive un problema univoco.</span><span class="sxs-lookup"><span data-stu-id="a1366-112">The combination of these report parameters describes a unique problem.</span></span>

<span data-ttu-id="a1366-113">Quando WER verifica la presenza di una soluzione, comunica con il server WER in Microsoft chiedendo prima se il problema è già noto.</span><span class="sxs-lookup"><span data-stu-id="a1366-113">When WER checks for a solution, it communicates with the WER server at Microsoft by first asking if the problem is already known.</span></span> <span data-ttu-id="a1366-114">Il server risponde in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a1366-114">The server responds in one of the following ways:</span></span>

-   <span data-ttu-id="a1366-115">Se il problema è noto ed è presente una soluzione, il server invia la soluzione al computer client e WER Visualizza le informazioni all'utente.</span><span class="sxs-lookup"><span data-stu-id="a1366-115">If the problem is known and there is a solution, the server sends the solution to the client computer and WER displays this information to the user.</span></span>
-   <span data-ttu-id="a1366-116">Se il problema viene esaminato, il server può inviare una risposta che indica lo stato.</span><span class="sxs-lookup"><span data-stu-id="a1366-116">If the problem is being investigated, the server may send a response that indicates the status.</span></span> <span data-ttu-id="a1366-117">Se lo sviluppatore necessita di ulteriori informazioni per risolvere il problema, il server richiede informazioni aggiuntive da WER e WER chiede all'utente l'autorizzazione per l'invio di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="a1366-117">If the developer needs more information to solve the problem, the server requests additional information from WER and WER asks the user for permission to send this information.</span></span>
-   <span data-ttu-id="a1366-118">Se il problema non è noto, il server crea un problema affinché uno sviluppatore analizzi e invii una risposta che indica lo stato.</span><span class="sxs-lookup"><span data-stu-id="a1366-118">If the problem is not known, the server creates an issue for a developer to investigate and sends WER a response that indicates the status.</span></span>

<span data-ttu-id="a1366-119">Con questo processo, WER raccoglie ulteriori informazioni, se necessario, o invia una soluzione all'utente, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="a1366-119">Using this process, WER gathers more information if needed or sends a solution to the user when available.</span></span> <span data-ttu-id="a1366-120">In Windows Vista, l'utente può accedere a **segnalazioni di problemi e soluzioni** in qualsiasi momento per visualizzare le soluzioni disponibili, verificare se sono disponibili nuove soluzioni o gestire le altre impostazioni e report di wer.</span><span class="sxs-lookup"><span data-stu-id="a1366-120">On Windows Vista, the user can go to **Problem Reports and Solutions** at any time to view available solutions, check whether new solutions are available, or manage their other WER reports and settings.</span></span> <span data-ttu-id="a1366-121">In Windows 7, le **soluzioni e i report sui problemi** sono ora chiamati **centro operativo**.</span><span class="sxs-lookup"><span data-stu-id="a1366-121">On Windows 7, the **Problem Reports and Solutions** is now called the **Action Center**.</span></span> <span data-ttu-id="a1366-122">Fare clic su **Start** e immettere "View" in **Cerca programmi e file** , quindi selezionare **Visualizza tutti i report sui** problemi, **Visualizza cronologia affidabilità** o **Visualizza soluzioni ai problemi**.</span><span class="sxs-lookup"><span data-stu-id="a1366-122">Click **Start** and enter "view" in **Search programs and files** and then select **View all problem reports**, **View reliability history**, or **View solutions to problems**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1366-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a1366-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1366-124">Segnalazione errori Windows</span><span class="sxs-lookup"><span data-stu-id="a1366-124">Windows Error Reporting</span></span>](windows-error-reporting.md)
</dt> </dl>

 

 




