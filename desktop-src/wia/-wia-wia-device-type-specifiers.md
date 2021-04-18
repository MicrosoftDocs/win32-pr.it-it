---
description: Gli identificatori del tipo di dispositivo Windows Image Acquisition (WIA) sono costanti che indicano il tipo di dispositivo collegato al computer di un utente.
ms.assetid: 569b99ab-628b-4a43-a6e5-0ae81524fcc0
title: Identificatori del tipo di dispositivo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc18b000d84bec5e5be37a5a5c52f28f6f8325d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307316"
---
# <a name="wia-device-type-specifiers"></a><span data-ttu-id="4d64b-103">Identificatori del tipo di dispositivo WIA</span><span class="sxs-lookup"><span data-stu-id="4d64b-103">WIA Device Type Specifiers</span></span>

<span data-ttu-id="4d64b-104">Gli identificatori del tipo di dispositivo Windows Image Acquisition (WIA) sono costanti che indicano il tipo di dispositivo collegato al computer di un utente.</span><span class="sxs-lookup"><span data-stu-id="4d64b-104">Windows Image Acquisition (WIA) Device Type Specifiers are constants that indicate the type of device attached to a user's computer.</span></span> <span data-ttu-id="4d64b-105">Utilizzare la \_ \_ macro di tipo Get STIDEVICE per ottenere questi valori dalla proprietà WIA Device Type.</span><span class="sxs-lookup"><span data-stu-id="4d64b-105">Use the GET\_STIDEVICE\_TYPE macro to obtain these values from the WIA device type property.</span></span> <span data-ttu-id="4d64b-106">Gli identificatori di tipo di dispositivo WIA validi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4d64b-106">The following are valid WIA Device Type Specifiers:</span></span> 

| <span data-ttu-id="4d64b-107">Tipo di dispositivo</span><span class="sxs-lookup"><span data-stu-id="4d64b-107">Device Type</span></span>                 | <span data-ttu-id="4d64b-108">Significato</span><span class="sxs-lookup"><span data-stu-id="4d64b-108">Meaning</span></span>                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d64b-109">StiDeviceTypeDefault</span><span class="sxs-lookup"><span data-stu-id="4d64b-109">StiDeviceTypeDefault</span></span>        | <span data-ttu-id="4d64b-110">Dispositivo WIA generico.</span><span class="sxs-lookup"><span data-stu-id="4d64b-110">Generic WIA device.</span></span> <span data-ttu-id="4d64b-111">Durante le enumerazioni dei dispositivi, questa costante viene usata per enumerare tutti i dispositivi WIA.</span><span class="sxs-lookup"><span data-stu-id="4d64b-111">During device enumerations, this constant is used to enumerate all WIA devices.</span></span>                         |
| <span data-ttu-id="4d64b-112">StiDeviceTypeDigitalCamera</span><span class="sxs-lookup"><span data-stu-id="4d64b-112">StiDeviceTypeDigitalCamera</span></span>  | <span data-ttu-id="4d64b-113">Il dispositivo è una fotocamera.</span><span class="sxs-lookup"><span data-stu-id="4d64b-113">The device is a camera.</span></span> <span data-ttu-id="4d64b-114">*Questo identificatore non è supportato da* Windows Vista *e versioni successive.*</span><span class="sxs-lookup"><span data-stu-id="4d64b-114">*This specifier is not supported by* Windows Vista *and later.*</span></span>                                     |
| <span data-ttu-id="4d64b-115">StiDeviceTypeScanner</span><span class="sxs-lookup"><span data-stu-id="4d64b-115">StiDeviceTypeScanner</span></span>        | <span data-ttu-id="4d64b-116">Il dispositivo è uno scanner.</span><span class="sxs-lookup"><span data-stu-id="4d64b-116">The device is a scanner.</span></span>                                                                                                    |
| <span data-ttu-id="4d64b-117">StiDeviceTypeStreamingVideo</span><span class="sxs-lookup"><span data-stu-id="4d64b-117">StiDeviceTypeStreamingVideo</span></span> | <span data-ttu-id="4d64b-118">Il dispositivo contiene video di streaming.</span><span class="sxs-lookup"><span data-stu-id="4d64b-118">The device contains streaming video.</span></span> <span data-ttu-id="4d64b-119">*Questo identificatore non è supportato da* Windows Server 2003 *,* Windows Vista *o versioni successive.*</span><span class="sxs-lookup"><span data-stu-id="4d64b-119">*This specifier is not supported by* Windows Server 2003 *,* Windows Vista, *or later.*</span></span> |



 

 

 



