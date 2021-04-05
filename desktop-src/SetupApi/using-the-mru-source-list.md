---
description: La funzione SetupSetSourceList consente di aprire o creare un elenco di origine nel sistema utenti.
ms.assetid: cda632cf-6c92-48fb-aef1-25b320affd3e
title: Uso dell'elenco di origine MRU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbecb9e32a554d1818661b1fd7f6e782744c16e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967176"
---
# <a name="using-the-mru-source-list"></a><span data-ttu-id="581fc-103">Uso dell'elenco di origine MRU</span><span class="sxs-lookup"><span data-stu-id="581fc-103">Using the MRU Source List</span></span>

<span data-ttu-id="581fc-104">La funzione [**SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) aprirà o creerà un elenco di origine nel sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="581fc-104">The [**SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) function will open or create a source list on the user's system.</span></span> <span data-ttu-id="581fc-105">È possibile specificare per impostare l'elenco di utenti, l'elenco di sistema, una combinazione degli elenchi di utenti e di sistema o un elenco temporaneo come elenco di origine MRU.</span><span class="sxs-lookup"><span data-stu-id="581fc-105">You can specify to set the user list, the system list, a combination of the user and system lists, or a temporary list as the MRU source list.</span></span> <span data-ttu-id="581fc-106">Se viene usato un elenco temporaneo, sarà l'unico elenco disponibile per l'applicazione di installazione fino a quando non viene chiamato [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) oppure **SetupSetSourceList** viene chiamato una seconda volta.</span><span class="sxs-lookup"><span data-stu-id="581fc-106">If a temporary list is used, it will be the only list available to the setup application until [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) is called, or **SetupSetSourceList** is called a second time.</span></span>

<span data-ttu-id="581fc-107">Dopo aver impostato un elenco, è possibile eseguire una query sull'elenco di origine usando [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) per ottenere una matrice dei percorsi di origine.</span><span class="sxs-lookup"><span data-stu-id="581fc-107">After a list is set, you can query the source list by using [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) to obtain an array of the source paths.</span></span> <span data-ttu-id="581fc-108">Quando la matrice dell'elenco di origine non è più necessaria, è necessario chiamare la funzione [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) per liberare le risorse allocate da [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista).</span><span class="sxs-lookup"><span data-stu-id="581fc-108">When the source list array is no longer needed, you must call the [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) function to free the resources allocated by [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista).</span></span>

<span data-ttu-id="581fc-109">Per aggiungere un percorso a un elenco di origine, ovvero uno che risiede nel sistema dell'utente o un elenco temporaneo, chiamare [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista).</span><span class="sxs-lookup"><span data-stu-id="581fc-109">To add a path to a source list, either one that is resident on the user's system, or a temporary list, call [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista).</span></span> <span data-ttu-id="581fc-110">Se l'elenco di origine specificato non è temporaneo, tale origine rimarrà nel sistema dell'utente e sarà accessibile alle installazioni successive.</span><span class="sxs-lookup"><span data-stu-id="581fc-110">If the source list specified is not temporary, that source will remain on the user's system and is accessible to subsequent installations.</span></span>

<span data-ttu-id="581fc-111">Per rimuovere un percorso dal percorso di origine, chiamare la funzione [**SetupRemoveFromSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) .</span><span class="sxs-lookup"><span data-stu-id="581fc-111">To remove a path from the source path, call the [**SetupRemoveFromSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) function.</span></span>

 

 



