---
description: Nella procedura seguente viene illustrato come eseguire il debug di un monitoraggio.
ms.assetid: 499f409c-e25a-4ab3-b0aa-e6b308fc7169
title: Debug di un monitoraggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641818b7f1cd1740c2732ced5527a2e278793a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529017"
---
# <a name="debugging-a-monitor"></a><span data-ttu-id="a2f3a-103">Debug di un monitoraggio</span><span class="sxs-lookup"><span data-stu-id="a2f3a-103">Debugging a Monitor</span></span>

<span data-ttu-id="a2f3a-104">Nella procedura seguente viene illustrato come eseguire il debug di un monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="a2f3a-104">The following procedure demonstrates how to debug a monitor.</span></span>

<span data-ttu-id="a2f3a-105">**Per eseguire il debug di un monitoraggio**</span><span class="sxs-lookup"><span data-stu-id="a2f3a-105">**To debug a monitor**</span></span>

1.  <span data-ttu-id="a2f3a-106">Installare la DLL di monitoraggio e il file di database di programma (con estensione pdb) generato al momento della compilazione del monitoraggio nel percorso corretto.</span><span class="sxs-lookup"><span data-stu-id="a2f3a-106">Install the monitor DLL and the program database (.pdb) file generated when you compiled the monitor in the correct location.</span></span> <span data-ttu-id="a2f3a-107">Per ulteriori informazioni, vedere [installazione di un monitoraggio per Network Monitor](installing-a-monitor-to-network-monitor.md) .</span><span class="sxs-lookup"><span data-stu-id="a2f3a-107">See [Installing a Monitor to Network Monitor](installing-a-monitor-to-network-monitor.md) for further details.</span></span>
2.  <span data-ttu-id="a2f3a-108">Verificare che il servizio di controllo di monitoraggio sia configurato come server anziché come servizio selezionando Pannello di controllo, servizi.</span><span class="sxs-lookup"><span data-stu-id="a2f3a-108">Verify that the Monitor Control Service is configured as a server instead of a service by selecting Control Panel, Services.</span></span>
3.  <span data-ttu-id="a2f3a-109">Aprire un prompt dei comandi e passare alla directory Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="a2f3a-109">Open a command prompt and go to the Network Monitor directory.</span></span> <span data-ttu-id="a2f3a-110">Digitare:</span><span class="sxs-lookup"><span data-stu-id="a2f3a-110">Type:</span></span>

    <span data-ttu-id="a2f3a-111">**Mcsvc.exe/RegServer**</span><span class="sxs-lookup"><span data-stu-id="a2f3a-111">**Mcsvc.exe /RegServer**</span></span>

    <span data-ttu-id="a2f3a-112">Al termine della sessione di debug del monitoraggio, è possibile ripristinare la condizione predefinita di MCSVC digitando:</span><span class="sxs-lookup"><span data-stu-id="a2f3a-112">After the monitor debugging session is complete, you can return the MCSVC to its default condition by typing:</span></span>

    <span data-ttu-id="a2f3a-113">**Mcsvc.exe/Service**</span><span class="sxs-lookup"><span data-stu-id="a2f3a-113">**Mcsvc.exe /Service**</span></span>

4.  <span data-ttu-id="a2f3a-114">In Microsoft Visual Studio avviare Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="a2f3a-114">In Microsoft Visual Studio, launch Microsoft Visual C++.</span></span>
5.  <span data-ttu-id="a2f3a-115">Nel **file** **aprire** l'opzione di menu, quindi selezionare il nome della DLL di monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="a2f3a-115">From the **File**, **Open** menu option, select the name of your monitor DLL.</span></span>
6.  <span data-ttu-id="a2f3a-116">Dopo il caricamento di Microsoft Visual C++, fare clic su **progetto**, **Impostazioni**.</span><span class="sxs-lookup"><span data-stu-id="a2f3a-116">After Microsoft Visual C++ loads, click **Project**, **Settings**.</span></span>
7.  <span data-ttu-id="a2f3a-117">Fare clic sulla scheda **debug** in **eseguibile** per la sessione di debug e digitare il percorso completo di Mcsvc.exe.</span><span class="sxs-lookup"><span data-stu-id="a2f3a-117">Click the **Debug** tab under **Executable** for debug session and type the full path of Mcsvc.exe.</span></span> <span data-ttu-id="a2f3a-118">Ad esempio, C: \\ Program Files \\ Netmon2 \\Mcsvc.exe.</span><span class="sxs-lookup"><span data-stu-id="a2f3a-118">For example, C:\\Program files\\Netmon2\\Mcsvc.exe.</span></span>
8.  <span data-ttu-id="a2f3a-119">Impostare i punti di interruzione nel codice.</span><span class="sxs-lookup"><span data-stu-id="a2f3a-119">Set the breakpoints in the code.</span></span>

> [!Note]  
> <span data-ttu-id="a2f3a-120">Non utilizzare una finestra di messaggio per il debug del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="a2f3a-120">Do not use a message box for monitor debugging.</span></span> <span data-ttu-id="a2f3a-121">Se il MCSVC è in esecuzione come servizio, il popup non verrà visualizzato e MCSVC apparirà in blocco.</span><span class="sxs-lookup"><span data-stu-id="a2f3a-121">If the MCSVC is running as a service, you will not see the popup, and MCSVC will appear to hang.</span></span>

 

 

 



