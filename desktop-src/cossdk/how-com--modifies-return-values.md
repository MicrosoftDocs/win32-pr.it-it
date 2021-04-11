---
description: Modalità di modifica dei valori restituiti da COM+
ms.assetid: a6997f02-8456-45b5-9f40-4b9094ee4626
title: Modalità di modifica dei valori restituiti da COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa8270e41f1a1a96df0c17ccc1b98530fba4347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127034"
---
# <a name="how-com-modifies-return-values"></a><span data-ttu-id="c824c-103">Modalità di modifica dei valori restituiti da COM+</span><span class="sxs-lookup"><span data-stu-id="c824c-103">How COM+ Modifies Return Values</span></span>

<span data-ttu-id="c824c-104">COM+ non modifica mai il valore restituito di un valore **HRESULT** che indica un errore, ad esempio e ha \_ \_ esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c824c-104">COM+ never changes the return value of an **HRESULT** that indicates failure, such as E\_UNEXPECTED or E\_FAIL.</span></span> <span data-ttu-id="c824c-105">Tuttavia, quando un oggetto che utilizza la funzionalità COM+ restituisce un valore **HRESULT** che indica l'esito positivo (ad esempio \_ , S OK, s \_ false o NOERROR), com+ talvolta converte il valore **HRESULT** in un codice di errore com+ prima che venga restituito al chiamante.</span><span class="sxs-lookup"><span data-stu-id="c824c-105">However, when an object using COM+ functionality returns an **HRESULT** value indicating success (such as S\_OK, S\_FALSE, or NOERROR), COM+ sometimes converts the **HRESULT** into a COM+ error code before it returns to the caller.</span></span>

<span data-ttu-id="c824c-106">Ad esempio, quando un'applicazione restituisce \_ OK dopo la chiamata a [**IObjectContext:: Tocomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), se l'oggetto è la radice di una transazione di cui non è stato eseguito il commit, **HRESULT** viene convertito nel contesto \_ E \_ interrotto.</span><span class="sxs-lookup"><span data-stu-id="c824c-106">For example, when an application returns S\_OK after calling [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), if the object is the root of a transaction that fails to commit, the **HRESULT** is converted to CONTEXT\_E\_ABORTED.</span></span>

<span data-ttu-id="c824c-107">Quando COM+ converte un valore **HRESULT** , cancella tutti i parametri di output del metodo.</span><span class="sxs-lookup"><span data-stu-id="c824c-107">When COM+ converts an **HRESULT** value, it clears all of the method's output parameters.</span></span> <span data-ttu-id="c824c-108">I riferimenti restituiti vengono rilasciati e i valori dei puntatori a oggetti restituiti vengono impostati su **null**.</span><span class="sxs-lookup"><span data-stu-id="c824c-108">Returned references are released, and the values of the returned object pointers are set to **NULL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c824c-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c824c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c824c-110">Criteri di isolamento degli errori e FailFast</span><span class="sxs-lookup"><span data-stu-id="c824c-110">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="c824c-111">Individuazione dell'origine di un errore</span><span class="sxs-lookup"><span data-stu-id="c824c-111">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="c824c-112">Interpretazione dei codici di errore</span><span class="sxs-lookup"><span data-stu-id="c824c-112">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="c824c-113">Strategie per la gestione degli errori in COM+</span><span class="sxs-lookup"><span data-stu-id="c824c-113">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="c824c-114">Risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="c824c-114">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



