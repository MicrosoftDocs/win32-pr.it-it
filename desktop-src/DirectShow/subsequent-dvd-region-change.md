---
description: Modifica dell'area DVD successiva
ms.assetid: 08c0b48a-2851-40c8-addc-21baeb83df1b
title: Modifica dell'area DVD successiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a28982d6807fa5d90356d15cbf5365a595c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317832"
---
# <a name="subsequent-dvd-region-change"></a><span data-ttu-id="66cd2-103">Modifica dell'area DVD successiva</span><span class="sxs-lookup"><span data-stu-id="66cd2-103">Subsequent DVD Region Change</span></span>

<span data-ttu-id="66cd2-104">In Windows 2000 e versioni successive, il navigatore DVD richiama una pagina delle proprietà sul dispositivo dell'unità DVD-ROM nel Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="66cd2-104">In Windows 2000 and later, the DVD Navigator invokes a property page on the DVD-ROM drive device in the Device Manager.</span></span> <span data-ttu-id="66cd2-105">Questa pagina delle proprietà viene inoltre attivata dall'applicazione DVDPlay.exe quando è necessario modificare un'area.</span><span class="sxs-lookup"><span data-stu-id="66cd2-105">This property page is also brought up by the DVDPlay.exe application when a region needs to be changed.</span></span> <span data-ttu-id="66cd2-106">L'interfaccia utente di questa pagina delle proprietà è molto simile a quella di DVDRgn.exe ed è localizzata nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="66cd2-106">The UI of this property page is very similar to that of DVDRgn.exe and it is regionalized in the operating system.</span></span>

<span data-ttu-id="66cd2-107">Per le unità RPC1, i componenti del sistema operativo Windows gestiscono le modifiche apportate all'area.</span><span class="sxs-lookup"><span data-stu-id="66cd2-107">For RPC1 drives, the Windows Operating System components manage region changes.</span></span> <span data-ttu-id="66cd2-108">Le unità RPC2 mantengono l'impostazione dell'area nei propri componenti hardware.</span><span class="sxs-lookup"><span data-stu-id="66cd2-108">RPC2 drives maintain the region setting in their own hardware.</span></span> <span data-ttu-id="66cd2-109">Quando il numero di modifiche consentite viene esaurito in un'unità RPC2, l'unità non riuscirà a modificare l'area e il componente della modifica dell'area nel sistema operativo indicherà che l'utente.</span><span class="sxs-lookup"><span data-stu-id="66cd2-109">When the number of allowed changes are exhausted on a RPC2 drive, the drive will fail the call to change the region and the region-change component in the operating system will indicate that to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66cd2-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="66cd2-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66cd2-111">Supporto delle modifiche all'area DVD in Windows</span><span class="sxs-lookup"><span data-stu-id="66cd2-111">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



