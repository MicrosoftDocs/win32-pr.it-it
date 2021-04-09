---
description: La routine di callback della coda predefinita gestisce le notifiche inviate da SetupCommitFileQueue in modo generico.
ms.assetid: 6f2b3b9f-86e5-42af-8adc-29a1c768d106
title: Informazioni sulla routine di callback della coda predefinita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dfd22a9fa260aa1e98a2085e0cb925ed1f3438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879022"
---
# <a name="about-the-default-queue-callback-routine"></a><span data-ttu-id="b39a2-103">Informazioni sulla routine di callback della coda predefinita</span><span class="sxs-lookup"><span data-stu-id="b39a2-103">About the Default Queue Callback Routine</span></span>

<span data-ttu-id="b39a2-104">La routine di callback della coda predefinita gestisce le notifiche inviate da [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) in modo generico.</span><span class="sxs-lookup"><span data-stu-id="b39a2-104">The default queue callback routine handles notifications sent by [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) in a generic manner.</span></span> <span data-ttu-id="b39a2-105">Utilizzando la routine predefinita, si ottiene un'interfaccia utente pronta per la creazione di finestre di dialogo di configurazione comuni.</span><span class="sxs-lookup"><span data-stu-id="b39a2-105">By using the default routine, you get a ready-made user interface to create common setup dialog boxes.</span></span> <span data-ttu-id="b39a2-106">Si consiglia di utilizzare la routine di callback della coda predefinita, sia per semplicità d'uso, sia per garantire un aspetto e un comportamento coerenti delle finestre di dialogo generate durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="b39a2-106">It is recommended that you use the default queue callback routine, both for ease of use, and to ensure a consistent appearance and behavior of dialog boxes generated during the installation.</span></span>

<span data-ttu-id="b39a2-107">La routine di callback predefinita richiede una struttura di contesto per la conservazione dei record interni.</span><span class="sxs-lookup"><span data-stu-id="b39a2-107">The default callback routine requires a context structure for internal record keeping.</span></span> <span data-ttu-id="b39a2-108">Inoltre, la coda passa informazioni aggiuntive relative alla notifica corrente in un set di parametri, *param1* e *param2*.</span><span class="sxs-lookup"><span data-stu-id="b39a2-108">In addition, the queue passes additional information relevant to the current notification in a set of parameters, *Param1* and *Param2*.</span></span>

<span data-ttu-id="b39a2-109">Se, ad esempio, la coda Invia una \_ notifica SPFILENOTIFY NEEDMEDIA alla routine di callback predefinita, *param1* punta a una struttura del [**\_ supporto di origine**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) che contiene informazioni sui supporti necessari e *param2* punta a una matrice di caratteri che può ricevere le nuove informazioni sul percorso dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b39a2-109">For example, if the queue sends an SPFILENOTIFY\_NEEDMEDIA notification to the default callback routine, *Param1* points to a [**SOURCE\_MEDIA**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) structure that contains information about the media needed, and *Param2* points to a character array that can receive new path information from the user.</span></span>

<span data-ttu-id="b39a2-110">La routine di callback predefinita utilizza queste informazioni per richiedere all'utente di inserire il supporto di origine necessario, specificare un nuovo percorso, ignorare la copia del file corrente oppure annullare l'operazione corrente.</span><span class="sxs-lookup"><span data-stu-id="b39a2-110">The default callback routine uses this information to prompt the user to either insert the needed source media, specify a new path, skip copying the current file, or cancel the current operation.</span></span> <span data-ttu-id="b39a2-111">La routine di callback della coda predefinita restituisce FILEOP \_ NEWPATH, FILEOP \_ doit, FILEOP \_ Skip o FILEOP \_ Abort alla coda, a seconda dell'azione assunta dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b39a2-111">The default queue callback routine returns FILEOP\_NEWPATH, FILEOP\_DOIT , FILEOP\_SKIP, or FILEOP\_ABORT to the queue, depending on which action the user took.</span></span>

<span data-ttu-id="b39a2-112">Per informazioni sul modo in cui la routine di callback della coda predefinita gestisce ogni notifica della coda, vedere [notifiche della coda di file](file-queue-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="b39a2-112">For information on how the default queue callback routine handles each queue notification, see [File Queue Notifications](file-queue-notifications.md).</span></span>

<span data-ttu-id="b39a2-113">Per informazioni sulle routine di callback della coda personalizzate, vedere [creazione di una routine di callback della coda personalizzata](creating-a-custom-queue-callback-routine.md).</span><span class="sxs-lookup"><span data-stu-id="b39a2-113">For information on custom queue callback routines, see [Creating a Custom Queue Callback Routine](creating-a-custom-queue-callback-routine.md).</span></span>

 

 



