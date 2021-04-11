---
description: WIA rappresenta un dispositivo della fotocamera come albero gerarchico di oggetti IWiaItem.
ms.assetid: fbb2821c-7f13-4fdd-a2ea-582be303855a
title: Dispositivi della fotocamera WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002a14d8e047019b1af2d2f86c1fd4a2e00d7808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226137"
---
# <a name="wia-camera-devices"></a><span data-ttu-id="3a7f3-103">Dispositivi della fotocamera WIA</span><span class="sxs-lookup"><span data-stu-id="3a7f3-103">WIA Camera Devices</span></span>

<span data-ttu-id="3a7f3-104">WIA rappresenta un dispositivo della fotocamera come albero gerarchico di oggetti [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="3a7f3-104">WIA represents a camera device as a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) objects.</span></span> <span data-ttu-id="3a7f3-105">L'elemento radice, restituito da una chiamata al metodo gestione dispositivi Windows Image Acquisition (WIA) [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) , viene usato per ottenere e impostare le informazioni sul dispositivo, per controllare il dispositivo e per iniziare l'enumerazione degli elementi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3a7f3-105">The root item, returned from a call to the Windows Image Acquisition (WIA) device manager [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) method, is used to get and set device information, to control the device, and to begin device item enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="3a7f3-106">WIA non supporta le fotocamere in Windows Vista o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3a7f3-106">WIA does not support cameras in Windows Vista or later.</span></span> <span data-ttu-id="3a7f3-107">Per queste versioni di Windows, usare l'API Windows Portable Device (WPD) descritta in Windows Driver Development Kit (DDK) per acquisire immagini dalle fotocamere.</span><span class="sxs-lookup"><span data-stu-id="3a7f3-107">For those versions of the Windows, use the Windows Portable Device (WPD) API described in the Windows Driver Development Kit (DDK) to acquire images from cameras.</span></span>

 

<span data-ttu-id="3a7f3-108">Il diagramma seguente illustra un'implementazione della fotocamera di esempio.</span><span class="sxs-lookup"><span data-stu-id="3a7f3-108">The following diagram illustrates a sample camera implementation.</span></span> <span data-ttu-id="3a7f3-109">L'elemento radice della fotocamera ha tre elementi figlio, due immagini e una cartella.</span><span class="sxs-lookup"><span data-stu-id="3a7f3-109">The camera root item has three child items, two pictures and one folder.</span></span> <span data-ttu-id="3a7f3-110">La cartella contiene due elementi figlio, entrambe immagini.</span><span class="sxs-lookup"><span data-stu-id="3a7f3-110">The folder has two child items, both pictures.</span></span>

![implementazione della fotocamera di esempio](images/wihierar.gif)

 

 



