---
title: MCIAVI
description: MCIAVI
ms.assetid: 68639f35-bc20-457d-b937-760af8323dce
keywords:
- Dispositivi MCI, driver MCIAVI
- Comandi MCI, driver MCIAVI
- Driver MCIAVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be2e69cf2b0fd9ee71650c56b0d7d9efb50a46e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471470"
---
# <a name="mciavi"></a><span data-ttu-id="97929-106">MCIAVI</span><span class="sxs-lookup"><span data-stu-id="97929-106">MCIAVI</span></span>

<span data-ttu-id="97929-107">Un file AVI può contenere più di due flussi, ad esempio una sequenza video, una colonna della lingua inglese e una colonna musicale francese.</span><span class="sxs-lookup"><span data-stu-id="97929-107">An AVI file can contain more than two streams — for example, a video sequence, an English soundtrack, and a French soundtrack.</span></span> <span data-ttu-id="97929-108">L'applicazione può usare un flusso indipendentemente dagli altri flussi del file.</span><span class="sxs-lookup"><span data-stu-id="97929-108">Your application can use a stream independently of the other streams in the file.</span></span>

<span data-ttu-id="97929-109">Il tipo di dispositivo **digitalvideo** controlla i file video.</span><span class="sxs-lookup"><span data-stu-id="97929-109">The **digitalvideo** device type controls video files.</span></span> <span data-ttu-id="97929-110">Per un elenco dei comandi MCI riconosciuti dai dispositivi digitali video, vedere [set di comandi Digital-video](digital-video-command-set.md).</span><span class="sxs-lookup"><span data-stu-id="97929-110">For a list of the MCI commands recognized by digital-video devices, see [Digital-Video Command Set](digital-video-command-set.md).</span></span>

<span data-ttu-id="97929-111">Il driver MCIAVI riproduce sequenze video e altri flussi di dati sotto il controllo dei comandi MCI.</span><span class="sxs-lookup"><span data-stu-id="97929-111">The MCIAVI driver plays video sequences and other data streams under the control of MCI commands.</span></span> <span data-ttu-id="97929-112">I flussi di dati possono contenere immagini, audio e tavolozze.</span><span class="sxs-lookup"><span data-stu-id="97929-112">Data streams can contain images, audio, and palettes.</span></span> <span data-ttu-id="97929-113">I dati dell'immagine possono essere costituiti da immagini con tavolozze dei colori o informazioni sui colori reali.</span><span class="sxs-lookup"><span data-stu-id="97929-113">The image data can consist of images with either color palettes or true-color information.</span></span>

<span data-ttu-id="97929-114">L'audio viene sincronizzato con il video entro un trentesimo di secondo.</span><span class="sxs-lookup"><span data-stu-id="97929-114">Audio is synchronized with the video within one-thirtieth of a second.</span></span> <span data-ttu-id="97929-115">Se l'hardware audio non è disponibile, tuttavia, il driver riproduce solo il flusso video.</span><span class="sxs-lookup"><span data-stu-id="97929-115">If audio hardware is not available, however, the driver plays only the video stream.</span></span> <span data-ttu-id="97929-116">Se necessario, il driver MCIAVI può eliminare i fotogrammi video per riprodurre un flusso senza interruzioni audio.</span><span class="sxs-lookup"><span data-stu-id="97929-116">The MCIAVI driver can drop video frames, if necessary, to play a stream without audio interruption.</span></span>

<span data-ttu-id="97929-117">L'applicazione può usare i servizi della classe MCIWnd della finestra anziché l'interfaccia del comando MCI per controllare qualsiasi driver MCI.</span><span class="sxs-lookup"><span data-stu-id="97929-117">Your application can use the MCIWnd window class services instead of the MCI command interface to control any MCI driver.</span></span> <span data-ttu-id="97929-118">Questa classe di finestra gestisce molti dei dettagli relativi alla gestione della finestra che supporta il dispositivo MCI e semplifica la programmazione necessaria per inviare i comandi MCI.</span><span class="sxs-lookup"><span data-stu-id="97929-118">This window class handles many of the details of managing the window supporting the MCI device and simplifies the programming required to send the MCI commands.</span></span> <span data-ttu-id="97929-119">L'applicazione può usare direttamente i servizi di libreria MCIWnd per controllare il dispositivo MCI oppure MCIWnd visualizzare una barra degli strumenti, una barra di scorrimento e i menu che consentono all'utente di controllare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="97929-119">Your application can use the MCIWnd library services directly to control the MCI device, or it can have MCIWnd display a toolbar, scroll bar, and menus that let the user control the device.</span></span> <span data-ttu-id="97929-120">Per ulteriori informazioni sulla classe della finestra MCIWnd, vedere [classe della finestra MCIWnd](mciwnd-window-class.md).</span><span class="sxs-lookup"><span data-stu-id="97929-120">For more information about the MCIWnd window class, see [MCIWnd Window Class](mciwnd-window-class.md).</span></span>

 

 




