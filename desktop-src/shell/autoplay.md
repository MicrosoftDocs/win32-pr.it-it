---
description: AutoRun è una funzionalità del sistema operativo Windows.
title: Creazione di un'applicazione CD-ROM abilitata per l'AutoRun
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5c583c1d-a4eb-4291-a839-c1ca7c51342c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 33f3ccc0a253690cd377cad908f87b43ac1ea304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225938"
---
# <a name="creating-an-autorun-enabled-cd-rom-application"></a><span data-ttu-id="790c4-103">Creazione di un'applicazione CD-ROM abilitata per l'AutoRun</span><span class="sxs-lookup"><span data-stu-id="790c4-103">Creating an AutoRun-enabled CD-ROM Application</span></span>

<span data-ttu-id="790c4-104">AutoRun è una funzionalità del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="790c4-104">AutoRun is a feature of the Windows operating system.</span></span> <span data-ttu-id="790c4-105">Consente di automatizzare le procedure per l'installazione e la configurazione di prodotti progettati per piattaforme basate su Windows distribuite su CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="790c4-105">It automates the procedures for installing and configuring products designed for Windows-based platforms that are distributed on CD-ROMs.</span></span> <span data-ttu-id="790c4-106">Quando gli utenti inseriscono un disco Compact abilitato per l'AutoRun nell'unità CD-ROM, l'esecuzione automatica esegue automaticamente un'applicazione nel CD-ROM che installa, configura o esegue il prodotto selezionato.</span><span class="sxs-lookup"><span data-stu-id="790c4-106">When users insert an AutoRun-enabled compact disc into their CD-ROM drive, AutoRun automatically runs an application on the CD-ROM that installs, configures, or runs the selected product.</span></span>

<span data-ttu-id="790c4-107">AutoRun può essere usato per installare ed eseguire applicazioni CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="790c4-107">AutoRun can be used to install and run CD-ROM applications.</span></span> <span data-ttu-id="790c4-108">Sebbene l'esecuzione automatica sia più comunemente usata per le applicazioni Windows, può essere usata anche per installare, configurare o eseguire applicazioni basate su MS-DOS in una sessione Microsoft MS-DOS di Windows.</span><span class="sxs-lookup"><span data-stu-id="790c4-108">Although AutoRun is most commonly used for Windows applications, it can also be used to install, configure, or run MS-DOS-based applications in a Windows Microsoft MS-DOS session.</span></span> <span data-ttu-id="790c4-109">È possibile configurare ogni applicazione basata su MS-DOS con una propria icona univoca, un file di Config.sys e un file di Autoexec.bat.</span><span class="sxs-lookup"><span data-stu-id="790c4-109">You can configure each MS-DOS-based application with its own unique icon, Config.sys file, and Autoexec.bat file.</span></span> <span data-ttu-id="790c4-110">Windows crea i file di configurazione corretti per l'applicazione basata su MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="790c4-110">Windows creates the correct configuration files for the MS-DOS-based application.</span></span> <span data-ttu-id="790c4-111">L'applicazione di avvio avvia quindi l'applicazione basata su MS-DOS in una finestra.</span><span class="sxs-lookup"><span data-stu-id="790c4-111">The startup application then starts the MS-DOS-based application in a window.</span></span>

> [!Note]  
> <span data-ttu-id="790c4-112">Per il funzionamento dell'avvio automatico, l'unità CD-ROM deve avere driver di dispositivo 32 o 64 bit che rilevano quando un utente inserisce un disco compatto e invia una notifica al sistema.</span><span class="sxs-lookup"><span data-stu-id="790c4-112">For AutoRun to work, the CD-ROM drive must have 32 or 64-bit device drivers that detect when a user inserts a compact disc and notify the system.</span></span>

 

<span data-ttu-id="790c4-113">Le sezioni seguenti illustrano come implementare un'applicazione CD-ROM abilitata per l'esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="790c4-113">The following sections discuss how to implement an AutoRun-enabled CD-ROM application.</span></span>

-   [<span data-ttu-id="790c4-114">Creazione di un'applicazione AutoRun-Enabled</span><span class="sxs-lookup"><span data-stu-id="790c4-114">Creating an AutoRun-Enabled Application</span></span>](autoplay-works.md)
-   [<span data-ttu-id="790c4-115">Voci Autorun. inf</span><span class="sxs-lookup"><span data-stu-id="790c4-115">Autorun.inf Entries</span></span>](autorun-cmds.md)
-   [<span data-ttu-id="790c4-116">Abilitazione e disabilitazione dell'esecuzione automatica</span><span class="sxs-lookup"><span data-stu-id="790c4-116">Enabling and Disabling AutoRun</span></span>](autoplay-reg.md)

 

 



