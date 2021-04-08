---
description: Quando non sono necessari privilegi elevati per installare un pacchetto di Windows Installer, l'autore del pacchetto può disattivare la finestra di dialogo visualizzata da controllo dell'account utente per richiedere l'autorizzazione dell'amministratore.
ms.assetid: cab30f95-cc93-46db-aba5-741b44adb6de
title: Creazione di pacchetti senza la finestra di dialogo controllo dell'account utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dcd44bf7d2250e12e7cafde46b57978b48cceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756230"
---
# <a name="authoring-packages-without-the-uac-dialog-box"></a><span data-ttu-id="6910b-103">Creazione di pacchetti senza la finestra di dialogo controllo dell'account utente</span><span class="sxs-lookup"><span data-stu-id="6910b-103">Authoring Packages without the UAC Dialog Box</span></span>

<span data-ttu-id="6910b-104">Quando non sono necessari privilegi elevati per installare un pacchetto di Windows Installer, l'autore del pacchetto può disattivare la finestra di dialogo visualizzata da [*controllo dell'account utente*](u-gly.md) per richiedere l'autorizzazione dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="6910b-104">When elevated privileges are not required to install a Windows Installer package, the author of the package can suppress the dialog box that [*User Account Control*](u-gly.md) (UAC) displays to prompt users for administrator authorization.</span></span>

<span data-ttu-id="6910b-105">Per evitare la visualizzazione della finestra di dialogo controllo dell'account utente durante l'installazione dell'applicazione, l'autore del pacchetto deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6910b-105">To suppress the display of the UAC dialog box when installing the application, the author of the package should do the following:</span></span>

-   <span data-ttu-id="6910b-106">Installare l'applicazione utilizzando Windows Installer 4,0 o versioni successive in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6910b-106">Install the application using Window Installer 4.0 or later on Windows Vista.</span></span>
-   <span data-ttu-id="6910b-107">Non dipendere dall'utilizzo di privilegi di sistema elevati per installare l'applicazione nel computer.</span><span class="sxs-lookup"><span data-stu-id="6910b-107">Do not depend on using elevated system privileges to install the application on the computer.</span></span>
-   <span data-ttu-id="6910b-108">Installare l'applicazione nel contesto per utente e impostarla come contesto di installazione predefinito del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6910b-108">Install the application in the per-user context and make this the default installation context of the package.</span></span> <span data-ttu-id="6910b-109">Se la proprietà [**ALLUSERS**](allusers.md) non è impostata, il programma di installazione installa il pacchetto nel contesto per singolo utente.</span><span class="sxs-lookup"><span data-stu-id="6910b-109">If the [**ALLUSERS**](allusers.md) property is not set, the installer installs the package in the per-user context.</span></span> <span data-ttu-id="6910b-110">Se non si include la proprietà **ALLUSERS** nella tabella delle [Proprietà](property-table.md), il programma di installazione non imposta questa proprietà e l'installazione per utente diventa il contesto di installazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="6910b-110">If you do not include the **ALLUSERS** property in the [Property table](property-table.md), the installer does not set this property and so per-user installation becomes the default installation context.</span></span> <span data-ttu-id="6910b-111">È possibile eseguire l'override di questa impostazione predefinita impostando la proprietà **ALLUSERS** nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="6910b-111">You can override this default by setting the **ALLUSERS** property on the command line.</span></span>
-   <span data-ttu-id="6910b-112">Impostare il bit 3 nella proprietà [**riepilogo Conteggio parole**](word-count-summary.md) per indicare che non sono necessari privilegi elevati per installare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6910b-112">Set Bit 3 in the [**Word Count Summary**](word-count-summary.md) property to indicate that elevated privileges are not required to install the application.</span></span>

 

 



