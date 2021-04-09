---
description: "Le informazioni di stato e di errore VSS seguenti vengono scritte nel registro eventi dell'applicazione:"
ms.assetid: d0b0f012-ad4f-4bd8-bb97-98f212bcbe81
title: Registrazione degli errori VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9822035f36f56162fb6836bf7ad4c09cdd31b777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129298"
---
# <a name="vss-error-logging"></a><span data-ttu-id="36b81-103">Registrazione degli errori VSS</span><span class="sxs-lookup"><span data-stu-id="36b81-103">VSS Error Logging</span></span>

<span data-ttu-id="36b81-104">Le informazioni di stato e di errore VSS seguenti vengono scritte nel registro eventi dell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="36b81-104">The following VSS error and state information is written to the Application Event Log:</span></span>

-   <span data-ttu-id="36b81-105">Errori del richiedente prodotti tramite l'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)</span><span class="sxs-lookup"><span data-stu-id="36b81-105">Requester errors produced using the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface</span></span>
-   <span data-ttu-id="36b81-106">Errori del writer generati nell'uso della classe [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) , inclusi i metodi di override</span><span class="sxs-lookup"><span data-stu-id="36b81-106">Writer errors produced in using the [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) class, including overriding methods</span></span>
-   <span data-ttu-id="36b81-107">Errori generati dal provider predefinito</span><span class="sxs-lookup"><span data-stu-id="36b81-107">Default-provider-generated errors</span></span>
-   <span data-ttu-id="36b81-108">Errori del servizio VSS generati nell'attività di coordinamento del provider, del writer e del richiedente, ad esempio la generazione di eventi.</span><span class="sxs-lookup"><span data-stu-id="36b81-108">VSS service errors generated in coordinating provider, writer, and requester activity (such as the generation of events)</span></span>

<span data-ttu-id="36b81-109">Questi errori possono avere diverse cause, incluso un errore di programmazione in codice di terze parti o errori di configurazione correlati a VSS.</span><span class="sxs-lookup"><span data-stu-id="36b81-109">These errors might have a number of causes, including a programming error in third-party code or VSS-related configuration errors.</span></span>

<span data-ttu-id="36b81-110">I driver VSS e le funzionalità di implementazione di livello inferiore scrivono errori nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="36b81-110">VSS drivers and lower-level implementation functionality write errors to the System Log.</span></span> <span data-ttu-id="36b81-111">Il software di terze parti (richiedente, provider, writer) può scegliere il registro applicazioni, il registro di sistema o entrambi per scrivere le voci del log degli errori.</span><span class="sxs-lookup"><span data-stu-id="36b81-111">Third-party software (requester, provider, writer) can choose the Application Log, the System Log, or both, to write error log entries.</span></span>

<span data-ttu-id="36b81-112">Si consiglia di usare il registro applicazioni per le applicazioni di livello superiore, ad esempio il codice in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="36b81-112">It is recommended that high-level applications (such as user-mode code) use the Application Log.</span></span> <span data-ttu-id="36b81-113">Le applicazioni di livello inferiore, ad esempio le interfacce hardware e i driver, devono usare il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="36b81-113">Lower-level applications, such as hardware interfaces and drivers, should use the System Log.</span></span>

 

 



