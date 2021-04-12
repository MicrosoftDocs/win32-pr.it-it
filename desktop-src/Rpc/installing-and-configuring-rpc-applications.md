---
title: Installazione e configurazione di applicazioni RPC
description: Quando il sistema operativo Microsoft Windows è installato in un server o in un client, il programma di installazione installa automaticamente i file di runtime RPC.
ms.assetid: cfcada3d-cf7c-42a9-9ed4-0b1bba7a98cf
keywords:
- Remote Procedure Call RPC, attività, installazione e configurazione di applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90837261c571276a74bb3a5354c7b9a5db2da6cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471758"
---
# <a name="installing-and-configuring-rpc-applications"></a><span data-ttu-id="13013-104">Installazione e configurazione di applicazioni RPC</span><span class="sxs-lookup"><span data-stu-id="13013-104">Installing and Configuring RPC Applications</span></span>

<span data-ttu-id="13013-105">Quando il sistema operativo Microsoft Windows è installato in un server o in un client, il programma di installazione installa automaticamente i file di runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="13013-105">When the Microsoft Windows operating system is installed on a server or client, setup automatically installs the RPC run-time files.</span></span> <span data-ttu-id="13013-106">Non è richiesta alcuna ulteriore installazione RPC.</span><span class="sxs-lookup"><span data-stu-id="13013-106">No further RPC installation is required.</span></span> <span data-ttu-id="13013-107">È tuttavia necessario assicurarsi che la versione di Windows installata supporti tutte le funzionalità utilizzate nell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="13013-107">You must ensure, however, that the version of Windows you install supports all the features used in your distributed application.</span></span>

<span data-ttu-id="13013-108">Quando si utilizza un'applicazione RPC in un sistema operativo Windows 3. x o Microsoft MS-DOS, è necessario copiare i file eseguibili della fase di esecuzione RPC nei computer Windows 3. x o MS-DOS che utilizzeranno l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="13013-108">When you use an RPC application on a Windows 3.x or Microsoft MS-DOS operating system, you must copy the RPC run-time executable files to the Windows 3.x or MS-DOS computers that will be using the application.</span></span> <span data-ttu-id="13013-109">La directory \\ mstools \\ RPC \_ RT16 nel CD di Platform Software Development Kit (SDK) contiene un'immagine del disco di questi file insieme a un programma di installazione per installare i file.</span><span class="sxs-lookup"><span data-stu-id="13013-109">The directory \\mstools\\rpc\_rt16 on the Platform Software Development Kit (SDK) CD contains a disk image of these files along with a setup program to install the files.</span></span> <span data-ttu-id="13013-110">Usare questa immagine del disco per creare un disco di installazione per la distribuzione con l'applicazione RPC.</span><span class="sxs-lookup"><span data-stu-id="13013-110">Use this disk image to create an install disk for distribution with your RPC application.</span></span> <span data-ttu-id="13013-111">È anche possibile usare applicazioni client a 16 bit destinate a MS-DOS o Windows in un sistema operativo Windows a 32 bit o a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="13013-111">You can also use 16-bit client applications targeted toward MS-DOS or Windows on a 32-bit/64-bit Windows operating system.</span></span> <span data-ttu-id="13013-112">Tuttavia, il programma di installazione dell'applicazione deve installare i file eseguibili contenuti in questa immagine del disco.</span><span class="sxs-lookup"><span data-stu-id="13013-112">However, your application's installation program must install the executable files contained in this disk image.</span></span>

<span data-ttu-id="13013-113">Quando si compila un'applicazione RPC per un client Macintosh, è necessario collegare i file necessari all'applicazione in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="13013-113">When you build an RPC application for a Macintosh client, you must link the necessary files to the application at build time.</span></span> <span data-ttu-id="13013-114">Non è necessaria alcuna installazione RPC aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="13013-114">No additional RPC installation is needed.</span></span>

<span data-ttu-id="13013-115">Per ulteriori informazioni sui file ridistribuibili e sui contratti di licenza, vedere \\ licenza \\Redist.txt e \\ \\License.txt di licenza nel CD di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="13013-115">For more details about redistributable files and licensing agreements, see \\LICENSE\\Redist.txt and \\LICENSE\\License.txt on the Platform SDK CD.</span></span>

<span data-ttu-id="13013-116">In questa sezione vengono fornite informazioni sulla configurazione di applicazioni RPC in un'ampia gamma di piattaforme hardware e software.</span><span class="sxs-lookup"><span data-stu-id="13013-116">This section contains information about setting up RPC applications on a variety of hardware and software platforms.</span></span> <span data-ttu-id="13013-117">Viene presentata la discussione nelle seguenti sezioni:</span><span class="sxs-lookup"><span data-stu-id="13013-117">It presents the discussion in the following sections:</span></span>

-   [<span data-ttu-id="13013-118">Configurazione del provider di servizi dei nomi</span><span class="sxs-lookup"><span data-stu-id="13013-118">Configuring the Name Service Provider</span></span>](configuring-the-name-service-provider.md)
-   [<span data-ttu-id="13013-119">Informazioni registro di sistema</span><span class="sxs-lookup"><span data-stu-id="13013-119">Registry Information</span></span>](registry-information.md)
-   [<span data-ttu-id="13013-120">Uso di RPC con proxy Winsock</span><span class="sxs-lookup"><span data-stu-id="13013-120">Using RPC with Winsock Proxy</span></span>](using-rpc-with-winsock-proxy.md)
-   [<span data-ttu-id="13013-121">Installazione di SPX/IPX</span><span class="sxs-lookup"><span data-stu-id="13013-121">SPX/IPX Installation</span></span>](spx-ipx-installation.md)
-   [<span data-ttu-id="13013-122">Configurazione del server di sicurezza</span><span class="sxs-lookup"><span data-stu-id="13013-122">Configuring the Security Server</span></span>](configuring-the-security-server.md)

 

 




