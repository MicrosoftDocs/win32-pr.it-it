---
description: Controlli padre e controllo dell'account utente
ms.assetid: dc7c322a-f534-4dda-8c62-aa628a7b91bc
title: Controlli padre e controllo dell'account utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7798661a7cadc4d497791925c83cdfa684b252a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311835"
---
# <a name="parental-controls-and-user-account-control"></a><span data-ttu-id="b2f29-103">Controlli padre e controllo dell'account utente</span><span class="sxs-lookup"><span data-stu-id="b2f29-103">Parental Controls and User Account Control</span></span>

<span data-ttu-id="b2f29-104">Il controllo dell'account utente (UAC) determinerà la presenza di account utente standard e amministratore protetto.</span><span class="sxs-lookup"><span data-stu-id="b2f29-104">User Account Control (UAC) will result in presence of Protected Administrator and Standard User accounts.</span></span> <span data-ttu-id="b2f29-105">Un amministratore protetto viene eseguito con gli stessi diritti di un utente standard in base all'utilizzo normale.</span><span class="sxs-lookup"><span data-stu-id="b2f29-105">A Protected Administrator will run with the same rights as a Standard User under normal usage.</span></span> <span data-ttu-id="b2f29-106">Per le operazioni con privilegi:</span><span class="sxs-lookup"><span data-stu-id="b2f29-106">For privileged operations:</span></span>

-   <span data-ttu-id="b2f29-107">Verrà visualizzata la finestra di dialogo interfaccia utente credenziali che richiede l'immissione di un nome utente e di una password per un amministratore protetto o un amministratore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b2f29-107">A Standard User will be shown the Credentials User Interface dialog box, which requires the input of a user name and password for a Protected Administrator or built-in Administrator.</span></span>
-   <span data-ttu-id="b2f29-108">Verrà visualizzata la finestra di dialogo interfaccia utente di consenso, che richiede la selezione di Consenti per continuare.</span><span class="sxs-lookup"><span data-stu-id="b2f29-108">A Protected Administrator will be shown the Consent User Interface dialog box, which requires selection of Allow to proceed.</span></span>

<span data-ttu-id="b2f29-109">È importante notare che il controllo dell'account utente viene implementato in base al processo, quindi un processo viene eseguito con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="b2f29-109">It is important to note that UAC is implemented on a per-process basis, so a process either runs elevated or not.</span></span> <span data-ttu-id="b2f29-110">In genere, non è adatto da un punto di vista della sicurezza per eseguire applicazioni di grandi dimensioni come sempre con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="b2f29-110">Generally, it is not suitable from a security standpoint to run large applications as always elevated.</span></span> <span data-ttu-id="b2f29-111">Per i controlli padre, il codice che deve modificare le impostazioni deve essere isolato da una delle due opzioni di implementazione:</span><span class="sxs-lookup"><span data-stu-id="b2f29-111">For Parental Controls, code that must modify settings should be isolated by one of two implementation options:</span></span>

1.  <span data-ttu-id="b2f29-112">Creare un file eseguibile di piccole dimensioni per la gestione delle impostazioni contrassegnata nel manifesto come che richiede diritti amministrativi.</span><span class="sxs-lookup"><span data-stu-id="b2f29-112">Create a small executable for settings management that is marked in its manifest as requiring administrative rights.</span></span> <span data-ttu-id="b2f29-113">La chiamata del file eseguibile provocherà la visualizzazione dell'interfaccia utente di consenso o credenziali prima di consentire l'esecuzione del processo.</span><span class="sxs-lookup"><span data-stu-id="b2f29-113">Invocation of the executable will cause the Consent or Credentials UI to be shown prior to allowing the process to run.</span></span>
2.  <span data-ttu-id="b2f29-114">Fornire le interfacce COM in una DLL del prodotto che consenta la chiamata per la documentazione del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="b2f29-114">Provide COM interfaces in a product DLL that allow for invocation per UAC documentation.</span></span> <span data-ttu-id="b2f29-115">In questo modo verrà visualizzata anche l'interfaccia utente di consenso o credenziali appropriata.</span><span class="sxs-lookup"><span data-stu-id="b2f29-115">This will also cause the appropriate Consent or Credentials UI to be shown.</span></span>

 

 



