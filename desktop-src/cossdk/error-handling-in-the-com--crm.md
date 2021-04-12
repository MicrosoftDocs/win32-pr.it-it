---
description: Gestione degli errori in COM+ CRM
ms.assetid: 9de31fb5-31e9-494a-b61f-87bcff0d5085
title: Gestione degli errori in COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aba2b5c4541485433a85fe01fee7870c2e43f62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483452"
---
# <a name="error-handling-in-the-com-crm"></a><span data-ttu-id="954b1-103">Gestione degli errori in COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="954b1-103">Error Handling in the COM+ CRM</span></span>

<span data-ttu-id="954b1-104">Le applicazioni server COM+ implementano un criterio FailFast.</span><span class="sxs-lookup"><span data-stu-id="954b1-104">COM+ server applications implement a failfast policy.</span></span> <span data-ttu-id="954b1-105">Se viene rilevato un errore interno grave, il processo dell'applicazione server viene chiuso e viene scritto un messaggio di errore nel registro eventi di Windows.</span><span class="sxs-lookup"><span data-stu-id="954b1-105">If a serious internal error is detected, the server application process exits and writes an error message to the Windows event log.</span></span> <span data-ttu-id="954b1-106">Ciò consente di rilevare rapidamente i problemi ed è possibile a causa della protezione dei dati dell'applicazione da parte dell'elaborazione delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="954b1-106">This allows quick detection of problems and is possible due to the protection of application data by transaction processing.</span></span> <span data-ttu-id="954b1-107">Controllare sempre nel registro eventi di Windows eventuali errori del CRM, durante lo sviluppo o durante la distribuzione finale.</span><span class="sxs-lookup"><span data-stu-id="954b1-107">Always check the Windows event log for any errors from the CRM, either during development or during final deployment.</span></span>

<span data-ttu-id="954b1-108">Errori di base nell'uso delle interfacce CRM, ad esempio argomenti non validi o errori di sequenza (ad esempio, il tentativo di scrivere un record di log prima di registrare il compensatore CRM), restituire i codici di errore e non attivare FailFast.</span><span class="sxs-lookup"><span data-stu-id="954b1-108">Basic errors in using the CRM interfaces, such as invalid arguments or sequence errors (for example, trying to write a log record before registering the CRM Compensator), return error codes and should not trigger failfast.</span></span> <span data-ttu-id="954b1-109">Per lo sviluppo di CRM, è possibile scegliere di impostare la chiave del registro di sistema VTRACE1 (vedere [le impostazioni del registro di sistema com+ CRM](com--crm-registry-settings.md)), che consente di visualizzare un messaggio nella finestra di output del debugger per ogni errore.</span><span class="sxs-lookup"><span data-stu-id="954b1-109">For CRM development, you may choose to set the VTRACE1 registry key (see [COM+ CRM Registry Settings](com--crm-registry-settings.md)), which causes a message to appear in the debugger output window for each error.</span></span>

<span data-ttu-id="954b1-110">Possono verificarsi anche errori temporanei.</span><span class="sxs-lookup"><span data-stu-id="954b1-110">Transient errors can also occur.</span></span> <span data-ttu-id="954b1-111">Questi errori sono in genere causati da condizioni di temporizzazione e comportano la restituzione di un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="954b1-111">These errors are typically caused by timing conditions and result in an error code being returned.</span></span> <span data-ttu-id="954b1-112">Lo sviluppatore di CRM deve assicurarsi che queste condizioni di errore vengano gestite.</span><span class="sxs-lookup"><span data-stu-id="954b1-112">The CRM developer should ensure that these error conditions are handled.</span></span> <span data-ttu-id="954b1-113">Ad esempio, durante la scrittura di un record di log, è possibile che la transazione venga interrotta a causa di un timeout. Il metodo restituisce quindi un errore, che il chiamante deve verificare e gestire in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="954b1-113">For example, while writing a log record, the transaction could abort due to a time-out. The method then returns an error, which the caller should check for and handle appropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="954b1-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="954b1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="954b1-115">Concetti Gestione risorse di compensazione COM+</span><span class="sxs-lookup"><span data-stu-id="954b1-115">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



