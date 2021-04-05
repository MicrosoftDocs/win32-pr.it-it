---
description: Un'applicazione in esecuzione come utente standard esegue operazioni che richiedono privilegi di amministratore creando un oggetto Component Object Model con privilegi elevati.
ms.assetid: 246fdf74-cc5b-47b1-b3a8-20441544e7be
title: Modello a oggetti COM dell'amministratore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c7d73cf31ce86c4788675374f34d04f6acf106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883869"
---
# <a name="administrator-com-object-model"></a><span data-ttu-id="372af-103">Modello a oggetti COM dell'amministratore</span><span class="sxs-lookup"><span data-stu-id="372af-103">Administrator COM Object Model</span></span>

<span data-ttu-id="372af-104">Nel modello a oggetti COM dell'amministratore, un'applicazione eseguita come utente standard esegue operazioni che richiedono privilegi di amministratore creando un oggetto [Component Object Model](/windows/desktop/com/component-object-model--com--portal) con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="372af-104">In the administrator COM object model, an application running as a standard user performs operations that require administrator privilege by creating an elevated [Component Object Model](/windows/desktop/com/component-object-model--com--portal) object.</span></span> <span data-ttu-id="372af-105">Per informazioni sulla creazione di un oggetto COM con privilegi elevati, vedere [il moniker di elevazione com](../com/the-com-elevation-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="372af-105">For information about creating an elevated COM object, see [The COM Elevation Moniker](../com/the-com-elevation-moniker.md).</span></span>

<span data-ttu-id="372af-106">Uno svantaggio dell'utilizzo del modello a oggetti COM dell'amministratore è che l'utente viene richiesto ogni volta che viene eseguita un'operazione con privilegi.</span><span class="sxs-lookup"><span data-stu-id="372af-106">One drawback to using the administrator COM object model is that the user is prompted each time a privileged operation is performed.</span></span>

<span data-ttu-id="372af-107">Qualsiasi interfaccia utente in grado di controllare l'oggetto COM deve essere presentata dall'oggetto COM stesso.</span><span class="sxs-lookup"><span data-stu-id="372af-107">Any user interface that can control the COM object must be presented by the COM object itself.</span></span> <span data-ttu-id="372af-108">In caso contrario, un processo senza privilegi può causare l'esecuzione di operazioni privilegiate da parte dell'oggetto COM con privilegi elevati senza che venga richiesto all'utente.</span><span class="sxs-lookup"><span data-stu-id="372af-108">Otherwise, an unprivileged process could cause the elevated COM object to perform privileged operations without the user being prompted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="372af-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="372af-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="372af-110">Sviluppo di applicazioni che richiedono privilegi di amministratore</span><span class="sxs-lookup"><span data-stu-id="372af-110">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="372af-111">Modello di broker amministratore</span><span class="sxs-lookup"><span data-stu-id="372af-111">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="372af-112">Modello di attività con privilegi elevati</span><span class="sxs-lookup"><span data-stu-id="372af-112">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> <dt>

[<span data-ttu-id="372af-113">Modello di servizio del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="372af-113">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> </dl>

 

 
