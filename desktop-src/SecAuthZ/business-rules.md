---
description: Una regola business consente a un'applicazione di usare la logica in fase di esecuzione per qualificare le autorizzazioni concesse al client.
ms.assetid: 2220d533-87f5-41a6-a688-a3307f0853fa
title: Regole business
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f77d94ce623086b8850406f9bae4f412d3bbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234334"
---
# <a name="business-rules"></a><span data-ttu-id="ce583-103">Regole business</span><span class="sxs-lookup"><span data-stu-id="ce583-103">Business Rules</span></span>

<span data-ttu-id="ce583-104">Una regola business consente a un'applicazione di usare la logica in fase di esecuzione per qualificare le autorizzazioni concesse al client.</span><span class="sxs-lookup"><span data-stu-id="ce583-104">A business rule allows an application to use logic at run time to qualify permissions granted to the client.</span></span>

<span data-ttu-id="ce583-105">Una regola business è uno script scritto nel linguaggio di programmazione Visual Basic Scripting Edition (VBScript) o scritto utilizzando il software di sviluppo Microsoft JScript associato a un oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) .</span><span class="sxs-lookup"><span data-stu-id="ce583-105">A business rule is a script written in the Visual Basic Scripting Edition (VBScript) programming language or written using the Microsoft JScript development software that is associated with an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object.</span></span> <span data-ttu-id="ce583-106">Quando un'applicazione controlla l'accesso per un'operazione, gestione autorizzazioni verifica innanzitutto se il client corrente ha accesso a tutte le attività che contengono tale operazione ma non associate alle regole business.</span><span class="sxs-lookup"><span data-stu-id="ce583-106">When an application checks access for an operation, Authorization Manager first checks if the current client has access to any tasks that contain that operation but that are not associated with business rules.</span></span> <span data-ttu-id="ce583-107">Se l'accesso non viene concesso in questo modo, gestione autorizzazioni esegue gli script della regola business associati a qualsiasi attività che contiene l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ce583-107">If access is not granted this way, Authorization Manager runs business-rule scripts associated with any task that contains the operation.</span></span>

<span data-ttu-id="ce583-108">Un'applicazione passa informazioni a uno script della regola business come una coppia di matrici che rappresentano i nomi e i valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="ce583-108">An application passes information to a business-rule script as a pair of arrays that represent the names and values of parameters.</span></span> <span data-ttu-id="ce583-109">Lo script può accedere a questi parametri tramite un oggetto [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) creato durante l'esecuzione dello script.</span><span class="sxs-lookup"><span data-stu-id="ce583-109">The script has access to these parameters through an [**AzBizRuleContext**](/windows/desktop/api/Azroles/nn-azroles-iazbizrulecontext) object that is created when the script runs.</span></span>

<span data-ttu-id="ce583-110">Uno script della regola business non può essere assegnato a un'attività contenuta in un ambito delegato.</span><span class="sxs-lookup"><span data-stu-id="ce583-110">A business-rule script cannot be assigned to a task contained by a delegated scope.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce583-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ce583-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce583-112">Qualificazione dell'accesso con la logica di business in C++</span><span class="sxs-lookup"><span data-stu-id="ce583-112">Qualifying Access with Business Logic in C++</span></span>](qualifying-access-with-business-logic-in-c--.md)
</dt> </dl>

 

 



