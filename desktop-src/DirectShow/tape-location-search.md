---
description: Ricerca posizione nastro
ms.assetid: 17fb4eba-4b2c-41c2-94e2-e58586f92e53
title: Ricerca posizione nastro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d1fb719f3b43374e5aa86f34c60e5b8f14d536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316297"
---
# <a name="tape-location-search"></a><span data-ttu-id="77ca0-103">Ricerca posizione nastro</span><span class="sxs-lookup"><span data-stu-id="77ca0-103">Tape Location Search</span></span>

<span data-ttu-id="77ca0-104">Sebbene i dispositivi DV supportino un comando per la ricerca in base al codice temporale o al numero di traccia assoluto (ATN), il driver MSDV non dispone di un modo standard e indipendente dal dispositivo per accedere a queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="77ca0-104">Although DV devices support a command to search by time code or by absolute track number (ATN), the MSDV driver does not have a standard, device-independent way to access these functions.</span></span> <span data-ttu-id="77ca0-105">L'unica opzione consiste nell'inviare al driver un comando AV/C non elaborato, come descritto nell'argomento relativo all' [emissione di comandi AV/c non elaborati](issuing-raw-av-c-commands.md).</span><span class="sxs-lookup"><span data-stu-id="77ca0-105">The only option is to send a raw AV/C command to the driver as described in the topic [Issuing Raw AV/C Commands](issuing-raw-av-c-commands.md).</span></span>

<span data-ttu-id="77ca0-106">Il driver UVC supporta una proprietà impostata per le ricerche nel percorso del nastro.</span><span class="sxs-lookup"><span data-stu-id="77ca0-106">The UVC driver supports a property set for tape location searches.</span></span> <span data-ttu-id="77ca0-107">Per inviare un comando di ricerca, utilizzare l'interfaccia **IKsControl** e impostare la \_ proprietà del trasporto PROPSETID ext \_ .</span><span class="sxs-lookup"><span data-stu-id="77ca0-107">To send a search command, use the **IKsControl** interface and set the PROPSETID\_EXT\_TRANSPORT property.</span></span> <span data-ttu-id="77ca0-108">L'uso di un set di proprietà è più sicuro dell'invio di comandi AV/C non elaborati al dispositivo, perché i comandi AV/C ignorano il filtro e passano direttamente al driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77ca0-108">Using a property set is safer than sending raw AV/C commands to the device, because AV/C commands bypass the filter and go directly to the device driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77ca0-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="77ca0-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77ca0-110">Controllo di una videocamera DV</span><span class="sxs-lookup"><span data-stu-id="77ca0-110">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> <dt>

[<span data-ttu-id="77ca0-111">Set di proprietà di trasporto dispositivo esterno</span><span class="sxs-lookup"><span data-stu-id="77ca0-111">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



