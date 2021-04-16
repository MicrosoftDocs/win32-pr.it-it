---
title: Applicazione del punto di controllo utente generico
description: L'applicazione del punto di controllo utente generico consente di individuare i dispositivi, controllare i dispositivi individuati e visualizzare le informazioni relative agli eventi, usando un'interfaccia grafica.
ms.assetid: 18ac23df-9d69-4a28-91e5-991eb4f3e6ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee56710cc1fafcc8551b34cb53df531f1f8cb601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104551851"
---
# <a name="generic-user-control-point-application"></a><span data-ttu-id="41fc6-103">Applicazione del punto di controllo utente generico</span><span class="sxs-lookup"><span data-stu-id="41fc6-103">Generic User Control Point Application</span></span>

<span data-ttu-id="41fc6-104">L'applicazione del punto di controllo utente generico consente di individuare i dispositivi, controllare i dispositivi individuati e visualizzare le informazioni relative agli eventi, usando un'interfaccia grafica.</span><span class="sxs-lookup"><span data-stu-id="41fc6-104">The generic user control point (UCP) application allows you to discover devices, control those discovered devices, and view the related eventing information, all using a graphical interface.</span></span>

<span data-ttu-id="41fc6-105">**Per avviare l'applicazione del punto di controllo dell'utilità generico**</span><span class="sxs-lookup"><span data-stu-id="41fc6-105">**To start the generic UCP application**</span></span>

1.  <span data-ttu-id="41fc6-106">Creare e configurare gli esempi \\ netds \\ UPnP \\ GenericUCP \\ cpp \\devtype.txt file (o il \\ \\ file VisualBasicdevtype.txt) con le informazioni sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41fc6-106">Create and configure the samples\\netds\\upnp\\GenericUCP\\CPP\\devtype.txt file (or the \\VisualBasic\\devtype.txt file) with device information.</span></span> <span data-ttu-id="41fc6-107">Questo file consente di configurare il punto di controllo dell'utilità generico per le ricerche "trova per tipo" e "ricerca asincrona".</span><span class="sxs-lookup"><span data-stu-id="41fc6-107">This file allows you to configure the generic UCP for the "find by type" and "async find" searches.</span></span> <span data-ttu-id="41fc6-108">Ogni riga del file deve contenere un tipo di dispositivo e la relativa descrizione.</span><span class="sxs-lookup"><span data-stu-id="41fc6-108">Each line of the file must contain a device type and the related description.</span></span> <span data-ttu-id="41fc6-109">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="41fc6-109">For example:</span></span>

    ``` syntax
    upnp:rootdevice All Root Devices
    urn:schemas-upnp-org:device:mediaplayer:1    Media Player
    ```

    <span data-ttu-id="41fc6-110">Questo esempio è relativo a un dispositivo di riproduzione multimediale fittizio.</span><span class="sxs-lookup"><span data-stu-id="41fc6-110">This example is for a fictitious media player device.</span></span> <span data-ttu-id="41fc6-111">La "Media Player" alla fine della seconda riga non fa parte del tipo di dispositivo, ma è a scopo informativo nell'applicazione del punto di controllo dell'utilità generica.</span><span class="sxs-lookup"><span data-stu-id="41fc6-111">The "Media Player" at the end of the second line is not a part of the device type, it is for informational purposes in the Generic UCP application.</span></span> <span data-ttu-id="41fc6-112">Lo stesso vale per "tutti i dispositivi radice" nella prima riga.</span><span class="sxs-lookup"><span data-stu-id="41fc6-112">The same applies to "All Root Devices" in the first line.</span></span>

    <span data-ttu-id="41fc6-113">Aggiungere una riga che contiene il tipo di dispositivo e la descrizione specifici per ogni dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41fc6-113">Add a line that contains your specific device type and description for each device.</span></span>

2.  <span data-ttu-id="41fc6-114">Creare e configurare gli esempi \\ netds \\ UPnP \\ GenericUCP \\ cpp \\udn.txt file (o il \\ \\ file VisualBasicudn.txt) con le informazioni UDN per i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="41fc6-114">Create and configure the samples\\netds\\upnp\\GenericUCP\\CPP\\udn.txt file (or the \\VisualBasic\\udn.txt file) with UDN information for your devices.</span></span> <span data-ttu-id="41fc6-115">Questo file consente di configurare il punto di controllo dell'utilità generico per la ricerca "Find by UDN".</span><span class="sxs-lookup"><span data-stu-id="41fc6-115">This file allows you to configure the generic UCP for the "find by UDN" search.</span></span> <span data-ttu-id="41fc6-116">Ogni riga usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="41fc6-116">Each line uses the following form:</span></span>

    ``` syntax
    uuid:{7d50b574-4213-4b88-84d9-e5c9241fcb3a}
    ```

    <span data-ttu-id="41fc6-117">Aggiungere una riga che contiene il UDN specifico per ogni dispositivo.</span><span class="sxs-lookup"><span data-stu-id="41fc6-117">Add a line that contains your specific UDN for each device.</span></span>

3.  <span data-ttu-id="41fc6-118">Eseguire GenericUCP.exe.</span><span class="sxs-lookup"><span data-stu-id="41fc6-118">Run GenericUCP.exe.</span></span> <span data-ttu-id="41fc6-119">Viene visualizzata la finestra punto di controllo dell' **utilità generica** .</span><span class="sxs-lookup"><span data-stu-id="41fc6-119">The **Generic UCP** window appears.</span></span>

    ![finestra punto di controllo dell'utilità generica](images/generic-ucp.png)

> [!Note]  
> <span data-ttu-id="41fc6-121">Il servizio **View Presentation** and **View View.** la funzionalità non è implementata nel codice di esempio C++.</span><span class="sxs-lookup"><span data-stu-id="41fc6-121">The **View Presentation** and **View Service Desc.** functionality is not implemented in the C++ sample code.</span></span>

 

 

 




