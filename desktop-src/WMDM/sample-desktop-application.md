---
title: Applicazione desktop di esempio
description: Applicazione desktop di esempio
ms.assetid: 3736dd01-b02f-4056-b19b-0e7cc6c9aa67
keywords:
- Windows Media Gestione dispositivi, esempi
- Gestione dispositivi, esempi
- applicazioni desktop, esempi
- Windows Media Gestione dispositivi, esempio di applicazione desktop
- Esempio di Gestione dispositivi, applicazione desktop
- applicazione di esempio WMDMApp
- esempi, applicazioni desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4008a25ca4448d4d4be7c9f667c5a9e4f08023
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396087"
---
# <a name="sample-desktop-application"></a><span data-ttu-id="42c74-110">Applicazione desktop di esempio</span><span class="sxs-lookup"><span data-stu-id="42c74-110">Sample Desktop Application</span></span>

<span data-ttu-id="42c74-111">Windows Media Gestione dispositivi viene fornito con un'applicazione desktop di esempio denominata WMDMApp.</span><span class="sxs-lookup"><span data-stu-id="42c74-111">The Windows Media Device Manager ships with a sample desktop application called wmdmapp.</span></span> <span data-ttu-id="42c74-112">Questa applicazione dispone di un'interfaccia utente grafica che consente di esplorare i dispositivi connessi, creare playlist nel dispositivo e trascinare i file multimediali nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="42c74-112">This application has a graphical user interface that allows you to browse connected devices, create playlists on the device, and drag media files to the device.</span></span>

<span data-ttu-id="42c74-113">Questa applicazione di esempio è costituita da due parti:</span><span class="sxs-lookup"><span data-stu-id="42c74-113">This sample application consists of two pieces:</span></span>

-   <span data-ttu-id="42c74-114">wmdapp.exe, un eseguibile che visualizza una finestra ed esegue la maggior parte dell'interfaccia utente e della funzionalità di base del programma e</span><span class="sxs-lookup"><span data-stu-id="42c74-114">wmdapp.exe, an executable that displays a window and performs most of the user interface and basic functionality of the program, and</span></span>
-   <span data-ttu-id="42c74-115">proghelp.dll, una DLL helper che esegue funzioni di utilità per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="42c74-115">proghelp.dll, a helper DLL that performs utility functions for the application.</span></span> <span data-ttu-id="42c74-116">È necessario registrare questa DLL dopo la compilazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="42c74-116">You must register this DLL after building the project.</span></span>

<span data-ttu-id="42c74-117">Per compilare l'applicazione di esempio, è possibile usare Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="42c74-117">To compile the sample application, you can use Visual Studio.</span></span> <span data-ttu-id="42c74-118">Nella sezione seguente viene descritto come eseguire questa operazione:</span><span class="sxs-lookup"><span data-stu-id="42c74-118">The following section describes how this is done:</span></span>

-   [<span data-ttu-id="42c74-119">Compilazione dell'applicazione di esempio con Visual Studio</span><span class="sxs-lookup"><span data-stu-id="42c74-119">Compiling the Sample Application Using Visual Studio</span></span>](compiling-the-sample-application-using-visual-studio.md)

<span data-ttu-id="42c74-120">Dopo aver compilato il progetto, registrare il file di proghelp.dll.</span><span class="sxs-lookup"><span data-stu-id="42c74-120">After compiling the project, register the proghelp.dll file.</span></span> <span data-ttu-id="42c74-121">Per registrare questa DLL, aprire un prompt dei comandi e passare alla directory contenente questa DLL e digitare `regsvr32 proghelp.dll` .</span><span class="sxs-lookup"><span data-stu-id="42c74-121">To register this DLL, open a command prompt and browse to the directory containing this DLL and type `regsvr32 proghelp.dll`.</span></span>

 

 




