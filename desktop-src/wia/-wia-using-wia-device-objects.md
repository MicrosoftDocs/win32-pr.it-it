---
description: Un dispositivo di imaging viene rappresentato in Windows Image Acquisition (WIA) come albero gerarchico di oggetti elemento WIA (interfacce IWiaItem).
ms.assetid: 5f3e56aa-8616-4574-882c-619caf54ca04
title: Utilizzo di oggetti dispositivo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1af755b243d322feac746620cb9dd9bd9965d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129387"
---
# <a name="using-wia-device-objects"></a><span data-ttu-id="22e13-103">Utilizzo di oggetti dispositivo WIA</span><span class="sxs-lookup"><span data-stu-id="22e13-103">Using WIA Device Objects</span></span>

<span data-ttu-id="22e13-104">Un dispositivo di imaging viene rappresentato in Windows Image Acquisition (WIA) come albero gerarchico di oggetti elemento WIA (interfacce [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ).</span><span class="sxs-lookup"><span data-stu-id="22e13-104">An imaging device is represented in Windows Image Acquisition (WIA) as a hierarchical tree of WIA item objects ([**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interfaces).</span></span> <span data-ttu-id="22e13-105">In genere, la radice di questo albero di elementi rappresenta il dispositivo stesso, mentre gli altri elementi nell'albero rappresentano le immagini, per una fotocamera o per le aree di analisi, per uno scanner.</span><span class="sxs-lookup"><span data-stu-id="22e13-105">Typically, the root of this item tree represents the device itself, while the other items on the tree represent images, for a camera, or scanning regions, for a scanner.</span></span>

<span data-ttu-id="22e13-106">Le applicazioni utilizzano Gestione dispositivi WIA per creare ed enumerare i dispositivi WIA.</span><span class="sxs-lookup"><span data-stu-id="22e13-106">Applications use the WIA device manager to create and enumerate WIA devices.</span></span> <span data-ttu-id="22e13-107">Le sezioni seguenti illustrano come creare e usare i dispositivi WIA:</span><span class="sxs-lookup"><span data-stu-id="22e13-107">The following sections explain how to create and use WIA devices:</span></span>

-   [<span data-ttu-id="22e13-108">Selezione di un dispositivo</span><span class="sxs-lookup"><span data-stu-id="22e13-108">Selecting a Device</span></span>](-wia-selecting-a-device.md)
-   [<span data-ttu-id="22e13-109">Dispositivi della fotocamera WIA</span><span class="sxs-lookup"><span data-stu-id="22e13-109">WIA Camera Devices</span></span>](-wia-wia-camera-devices.md)
-   [<span data-ttu-id="22e13-110">Dispositivi scanner WIA</span><span class="sxs-lookup"><span data-stu-id="22e13-110">WIA Scanner Devices</span></span>](-wia-wia-scanner-devices.md)

 

 



