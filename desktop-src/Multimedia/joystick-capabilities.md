---
title: Funzionalità del joystick
description: Funzionalità del joystick
ms.assetid: 910c7f1d-e20a-4a03-b512-9a7f8cb1e559
keywords:
- input multimediale, joystick
- joystick, spostamento a due assi
- joystick, spostamento a tre assi
- joystick, pulsanti
- joystick, intervalli di movimento
- joystick, frequenze di polling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b317d5a0c8deb48b49224fd051ecb7ce5a0bbced
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726719"
---
# <a name="joystick-capabilities"></a><span data-ttu-id="8c466-109">Funzionalità del joystick</span><span class="sxs-lookup"><span data-stu-id="8c466-109">Joystick Capabilities</span></span>

<span data-ttu-id="8c466-110">I joystick possono supportare un movimento di due o tre assi e un massimo di quattro pulsanti.</span><span class="sxs-lookup"><span data-stu-id="8c466-110">Joysticks can support two- or three-axis movement and up to four buttons.</span></span> <span data-ttu-id="8c466-111">I joystick supportano anche *intervalli diversi di frequenze di movimento e di* *polling*.</span><span class="sxs-lookup"><span data-stu-id="8c466-111">Joysticks also support different *ranges of motion* and *polling frequencies*.</span></span> <span data-ttu-id="8c466-112">L'intervallo di movimento è la distanza in base alla quale un handle di joystick può spostarsi dalla posizione di riposo alla posizione più lontana dalla posizione di riposo.</span><span class="sxs-lookup"><span data-stu-id="8c466-112">The range of motion is the distance a joystick handle can move from its resting position to the position farthest from its resting position.</span></span> <span data-ttu-id="8c466-113">La frequenza di polling è l'intervallo di tempo tra le query del joystick.</span><span class="sxs-lookup"><span data-stu-id="8c466-113">The polling frequency is the time interval between joystick queries.</span></span>

<span data-ttu-id="8c466-114">I driver del joystick possono supportare uno o due joystick.</span><span class="sxs-lookup"><span data-stu-id="8c466-114">Joystick drivers can support either one or two joysticks.</span></span> <span data-ttu-id="8c466-115">È possibile determinare il numero di joystick supportati da un driver del joystick usando la funzione [**joyGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) .</span><span class="sxs-lookup"><span data-stu-id="8c466-115">You can determine the number of joysticks supported by a joystick driver by using the [**joyGetNumDevs**](/windows/win32/api/joystickapi/nf-joystickapi-joygetnumdevs) function.</span></span> <span data-ttu-id="8c466-116">Questa funzione restituisce un Unsigned Integer che contiene il numero di joystick supportati o zero se non è disponibile alcun supporto per il joystick.</span><span class="sxs-lookup"><span data-stu-id="8c466-116">This function returns an unsigned integer that contains the number of supported joysticks or zero if there is no joystick support.</span></span> <span data-ttu-id="8c466-117">Il valore restituito non indica il numero di joystick collegati al sistema.</span><span class="sxs-lookup"><span data-stu-id="8c466-117">The return value does not indicate the number of joysticks attached to the system.</span></span>

<span data-ttu-id="8c466-118">È possibile determinare se un joystick è collegato al sistema tramite la funzione [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) .</span><span class="sxs-lookup"><span data-stu-id="8c466-118">You can determine if a joystick is attached to the system by using the [**joyGetPos**](/windows/win32/api/joystickapi/nf-joystickapi-joygetpos) function.</span></span> <span data-ttu-id="8c466-119">Questa funzione restituisce JOYERR \_ NOERROR se il dispositivo specificato è collegato.</span><span class="sxs-lookup"><span data-stu-id="8c466-119">This function returns JOYERR\_NOERROR if the specified device is attached.</span></span> <span data-ttu-id="8c466-120">In caso contrario, restituisce JOYERR \_ scollegato.</span><span class="sxs-lookup"><span data-stu-id="8c466-120">Otherwise , it returns JOYERR\_UNPLUGGED.</span></span>

<span data-ttu-id="8c466-121">Ogni joystick dispone di diverse funzionalità disponibili per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8c466-121">Each joystick has several capabilities that are available to your application.</span></span> <span data-ttu-id="8c466-122">È possibile recuperare le funzionalità di un joystick usando la funzione [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="8c466-122">You can retrieve the capabilities of a joystick by using the [**joyGetDevCaps**](/windows/win32/api/joystickapi/nf-joystickapi-joygetdevcaps) function.</span></span> <span data-ttu-id="8c466-123">Questa funzione riempie una struttura [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) con funzionalità di joystick quali i valori minimo e massimo per il sistema di coordinate, il numero di pulsanti sul joystick e le frequenze di polling minime e massime.</span><span class="sxs-lookup"><span data-stu-id="8c466-123">This function fills a [**JOYCAPS**](/windows/win32/api/joystickapi/ns-joystickapi-joycaps) structure with joystick capabilities such as the minimum and maximum values for its coordinate system, the number of buttons on the joystick, and the minimum and maximum polling frequencies.</span></span>

 

 