---
title: Testo Descrizione punto di ripristino
description: Quando un'applicazione chiama la funzione SRSetRestorePoint, può fornire qualsiasi testo come descrizione per il punto di ripristino; Tuttavia, nella tabella seguente viene illustrato il testo della descrizione consigliata.
ms.assetid: e6e1974b-c162-4019-9349-936f3786cb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e90fd1b7d5776c8c3798a68946382cc702b3bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221532"
---
# <a name="restore-point-description-text"></a><span data-ttu-id="c987a-103">Testo Descrizione punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="c987a-103">Restore Point Description Text</span></span>

<span data-ttu-id="c987a-104">Quando un'applicazione chiama la funzione [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) , può fornire qualsiasi testo come descrizione per il punto di ripristino; Tuttavia, nella tabella seguente viene illustrato il testo della descrizione consigliata.</span><span class="sxs-lookup"><span data-stu-id="c987a-104">When an application calls the [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) function, it can provide any text as a description for the restore point; however, the following table shows the recommended description text.</span></span>



| <span data-ttu-id="c987a-105">Modifica del sistema</span><span class="sxs-lookup"><span data-stu-id="c987a-105">System modification</span></span>                            | <span data-ttu-id="c987a-106">Tipo di punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="c987a-106">Restore point type</span></span>      | <span data-ttu-id="c987a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c987a-107">Description</span></span>            |
|------------------------------------------------|-------------------------|------------------------|
| <span data-ttu-id="c987a-108">Installazione delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="c987a-108">Application installation</span></span>                       | <span data-ttu-id="c987a-109">\_installazione applicazione</span><span class="sxs-lookup"><span data-stu-id="c987a-109">APPLICATION\_INSTALL</span></span>    | <span data-ttu-id="c987a-110">*Appname* installato</span><span class="sxs-lookup"><span data-stu-id="c987a-110">Installed *AppName*</span></span>    |
| <span data-ttu-id="c987a-111">Modifica dell'applicazione (aggiunta/rimozione di funzionalità)</span><span class="sxs-lookup"><span data-stu-id="c987a-111">Application modification (add/remove features)</span></span> | <span data-ttu-id="c987a-112">MODIFICARE \_ le impostazioni</span><span class="sxs-lookup"><span data-stu-id="c987a-112">MODIFY\_SETTINGS</span></span>        | <span data-ttu-id="c987a-113">*Appname* configurato</span><span class="sxs-lookup"><span data-stu-id="c987a-113">Configured *AppName*</span></span>   |
| <span data-ttu-id="c987a-114">Rimozione di applicazioni</span><span class="sxs-lookup"><span data-stu-id="c987a-114">Application removal</span></span>                            | <span data-ttu-id="c987a-115">disinstallazione dell'applicazione \_</span><span class="sxs-lookup"><span data-stu-id="c987a-115">APPLICATION\_UNINSTALL</span></span>  | <span data-ttu-id="c987a-116">*Appname* rimosso</span><span class="sxs-lookup"><span data-stu-id="c987a-116">Removed *AppName*</span></span>      |
| <span data-ttu-id="c987a-117">Installazione del driver di dispositivo</span><span class="sxs-lookup"><span data-stu-id="c987a-117">Device driver installation</span></span>                     | <span data-ttu-id="c987a-118">\_installazione del driver di dispositivo \_</span><span class="sxs-lookup"><span data-stu-id="c987a-118">DEVICE\_DRIVER\_INSTALL</span></span> | <span data-ttu-id="c987a-119">*Drivername* installato</span><span class="sxs-lookup"><span data-stu-id="c987a-119">Installed *DriverName*</span></span> |



 

<span data-ttu-id="c987a-120">I programmi di installazione, ad esempio Windows Installer e InstallShield, usano le convenzioni seguenti per il testo della descrizione:</span><span class="sxs-lookup"><span data-stu-id="c987a-120">Installers, such as Windows Installer and InstallShield, use these conventions for the description text:</span></span>

-   <span data-ttu-id="c987a-121">Il nome del prodotto segue il verbo. ad esempio, è installato *appname*.</span><span class="sxs-lookup"><span data-stu-id="c987a-121">The product name follows the verb; for example, Installed *AppName*.</span></span>
-   <span data-ttu-id="c987a-122">Il nome del prodotto può essere usato da solo (*appname*) o il nome del prodotto e il nome della società può essere usato (*MyCompany AppName*).</span><span class="sxs-lookup"><span data-stu-id="c987a-122">The product name can be used alone (*AppName*) or the product name and the company name may both be used (*MyCompany AppName*).</span></span>

 

 




