---
description: 'Altre informazioni su: limitazioni del modello di scripting'
ms.assetid: b8ddbfac-5b5e-4aff-beea-82e7fc984790
title: Limitazioni del modello di scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36ef43cd2cf2133b126eee065c2b33e463eb6401
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307345"
---
# <a name="limitations-of-the-scripting-model"></a><span data-ttu-id="a6024-103">Limitazioni del modello di scripting</span><span class="sxs-lookup"><span data-stu-id="a6024-103">Limitations of the Scripting Model</span></span>

> [!Note]  
> <span data-ttu-id="a6024-104">Questo sistema di scripting è stato sostituito con il livello di automazione Windows Image Acquisition (WIA).</span><span class="sxs-lookup"><span data-stu-id="a6024-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="a6024-105">Vedere [livello di automazione acquisizione immagini Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="a6024-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="a6024-106">Il modello di scripting di Windows Image Acquisition (WIA) espone un subset di funzionalità WIA.</span><span class="sxs-lookup"><span data-stu-id="a6024-106">The Windows Image Acquisition (WIA) scripting model exposes a subset of WIA functionality.</span></span> <span data-ttu-id="a6024-107">Nella tabella seguente vengono fornite le descrizioni delle limitazioni del modello di scripting.</span><span class="sxs-lookup"><span data-stu-id="a6024-107">The following table provides descriptions of the limitations of the scripting model.</span></span> 

| <span data-ttu-id="a6024-108">Funzionalità WIA</span><span class="sxs-lookup"><span data-stu-id="a6024-108">WIA Functionality</span></span>               | <span data-ttu-id="a6024-109">Limitazione del modello di scripting</span><span class="sxs-lookup"><span data-stu-id="a6024-109">Scripting Model Limitation</span></span>                                                                                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6024-110">Eliminazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="a6024-110">Suppressing the user interface</span></span>  | <span data-ttu-id="a6024-111">Impossibile disattivare l'interfaccia utente per l'impostazione delle proprietà del dispositivo/trasferimento.</span><span class="sxs-lookup"><span data-stu-id="a6024-111">Cannot suppress the user interface for setting device/transfer properties.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="a6024-112">Impostazione di proprietà</span><span class="sxs-lookup"><span data-stu-id="a6024-112">Setting properties</span></span>              | <span data-ttu-id="a6024-113">Impossibile impostare (scrivere) le proprietà di un dispositivo o di un elemento.</span><span class="sxs-lookup"><span data-stu-id="a6024-113">Cannot set (write) any device or item properties.</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="a6024-114">Registrazione per gli eventi di callback</span><span class="sxs-lookup"><span data-stu-id="a6024-114">Registering for callback events</span></span> | <span data-ttu-id="a6024-115">Può ricevere solo la notifica per tre eventi specifici: [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md), [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)e [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md).</span><span class="sxs-lookup"><span data-stu-id="a6024-115">Can only receive notification for three specified events: [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md), [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md), and [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md).</span></span> |
| <span data-ttu-id="a6024-116">Gestione degli errori</span><span class="sxs-lookup"><span data-stu-id="a6024-116">Handling errors</span></span>                 | <span data-ttu-id="a6024-117">Non è possibile gestire gli errori WIA.</span><span class="sxs-lookup"><span data-stu-id="a6024-117">Cannot handle WIA errors.</span></span>                                                                                                                                                                                                                                                |



 

 

 
