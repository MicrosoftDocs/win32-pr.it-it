---
description: 'Altre informazioni su: trasferimento di dati'
ms.assetid: 34871ff4-7eb0-451b-a62b-85b632af9a47
title: Trasferimento di dati
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05d94e9e09aad121720ca491864a23f3d2d38b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307331"
---
# <a name="transferring-data"></a><span data-ttu-id="e6dcf-103">Trasferimento di dati</span><span class="sxs-lookup"><span data-stu-id="e6dcf-103">Transferring Data</span></span>

> [!Note]  
> <span data-ttu-id="e6dcf-104">Questo sistema di scripting è stato sostituito con il livello di automazione Windows Image Acquisition (WIA).</span><span class="sxs-lookup"><span data-stu-id="e6dcf-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="e6dcf-105">Vedere [livello di automazione acquisizione immagini Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="e6dcf-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="e6dcf-106">Usare il metodo di [**trasferimento**](-wia-iwiadispatchitem-transfer.md) di un oggetto [**Item**](-wia-item.md) per trasferire i dati di immagini o audio da un dispositivo a un file o agli Appunti.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-106">Use the [**Transfer**](-wia-iwiadispatchitem-transfer.md) method of an [**Item**](-wia-item.md) object to transfer image or audio data from a device to a file or the clipboard.</span></span>

<span data-ttu-id="e6dcf-107">Passare un percorso e un nome file come primo parametro per salvare i dati su disco oppure passare la stringa "clipboard" per trasferire l'elemento negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="e6dcf-107">Pass a path and filename as the first parameter to save the data to disk, or pass the string "clipboard" to transfer the item to the clipboard.</span></span>

 

 
