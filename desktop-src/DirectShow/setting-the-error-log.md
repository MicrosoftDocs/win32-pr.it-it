---
description: Impostazione del log degli errori
ms.assetid: 2e3124e3-32d0-4eb6-9c1d-91b625018ac4
title: Impostazione del log degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac96fb90570408ca41be06656f7cf1704e9f48dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303695"
---
# <a name="setting-the-error-log"></a><span data-ttu-id="8fccc-103">Impostazione del log degli errori</span><span class="sxs-lookup"><span data-stu-id="8fccc-103">Setting the Error Log</span></span>

<span data-ttu-id="8fccc-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="8fccc-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="8fccc-105">Dopo aver implementato la classe di registrazione degli errori, creare una nuova istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="8fccc-105">After you implement the error logging class, create a new instance of the class.</span></span> <span data-ttu-id="8fccc-106">Assegnare quindi ai [servizi di modifica DirectShow](directshow-editing-services.md) un puntatore chiamando il metodo [**IAMSetErrorLog::p log degli \_ errori UT**](iamseterrorlog-put-errorlog.md) nella sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="8fccc-106">Then, give [DirectShow Editing Services](directshow-editing-services.md) a pointer to it by calling the [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) method on the timeline.</span></span> <span data-ttu-id="8fccc-107">Eseguire una query sulla sequenza temporale per l'interfaccia **IAMSetErrorLog** .</span><span class="sxs-lookup"><span data-stu-id="8fccc-107">Query the timeline for the **IAMSetErrorLog** interface.</span></span> <span data-ttu-id="8fccc-108">Per assicurarsi che tutti gli errori vengano registrati, è necessario chiamare questo metodo prima di caricare, salvare o eseguire il rendering della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="8fccc-108">To ensure that all errors are logged, you should call this method before you load, save, or render the timeline.</span></span>


```C++
IAMSetErrorLog  *pSetLog = NULL;
IAMErrorLog     *pLog = new CErrReporter();

pTL->QueryInterface(IID_IAMSetErrorLog, (void **)&pSetLog);
pSetLog->put_ErrorLog(pLog);
pSetLog->Release();
```



<span data-ttu-id="8fccc-109">La registrazione degli errori non ha alcun effetto sui valori restituiti ricevuti quando si chiamano i metodi nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8fccc-109">Error logging has no effect on the return values that you receive when you call methods in your application.</span></span> <span data-ttu-id="8fccc-110">La registrazione degli errori è complementare, ma non sostituisce le consuete tecniche di gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="8fccc-110">Error logging complements but does not replace the usual error handling techniques.</span></span> <span data-ttu-id="8fccc-111">Per creare un'applicazione affidabile, controllare sempre i valori HRESULT.</span><span class="sxs-lookup"><span data-stu-id="8fccc-111">To create a robust application, always check HRESULT values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fccc-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8fccc-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fccc-113">Errori di registrazione</span><span class="sxs-lookup"><span data-stu-id="8fccc-113">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



