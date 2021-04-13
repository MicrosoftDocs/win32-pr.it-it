---
title: Oggetto AudioOutput
description: Oggetto AudioOutput
ms.assetid: 7c1c6079-f445-4980-9559-8d26b6014e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919b435edf31b6ae24a8b5c6977d5aed542efac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104399021"
---
# <a name="the-audiooutput-object"></a><span data-ttu-id="b1c63-103">Oggetto AudioOutput</span><span class="sxs-lookup"><span data-stu-id="b1c63-103">The AudioOutput Object</span></span>

<span data-ttu-id="b1c63-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b1c63-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="b1c63-105">Questo oggetto fornisce l'accesso alle proprietà di output audio gestite dal server.</span><span class="sxs-lookup"><span data-stu-id="b1c63-105">This object provides access to audio output properties maintained by the server.</span></span> <span data-ttu-id="b1c63-106">Le proprietà sono di sola lettura, ma l'utente può modificarle nella finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="b1c63-106">The properties are read-only, but the user can change them in the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="b1c63-107">Se si dichiara una variabile oggetto di tipo [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**), non sarà possibile accedere a tutte le proprietà per l'oggetto [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) .</span><span class="sxs-lookup"><span data-stu-id="b1c63-107">If you declare an object variable of type [**IAgentCtlAudioObjectEx**](https://www.bing.com/search?q=**IAgentCtlAudioObjectEx**), you will not be able to access all properties for the [**AudioOutput**](/windows/desktop/lwef/the-audiooutput-object) object.</span></span> <span data-ttu-id="b1c63-108">Mentre Agent supporta anche [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**), quest'ultima interfaccia viene fornita solo per compatibilità con le versioni precedenti e supporta solo le proprietà nelle versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="b1c63-108">While Agent also supports [**IAgentCtlAudioObject**](https://www.bing.com/search?q=**IAgentCtlAudioObject**), this latter interface is provided only for backward compatibility and supports only those properties in previous releases.</span></span>

-   [<span data-ttu-id="b1c63-109">**Abilitato**</span><span class="sxs-lookup"><span data-stu-id="b1c63-109">**Enabled**</span></span>](enabled-property-ao.md)
-   [<span data-ttu-id="b1c63-110">**SoundEffects**</span><span class="sxs-lookup"><span data-stu-id="b1c63-110">**SoundEffects**</span></span>](soundeffects-property.md)
-   [<span data-ttu-id="b1c63-111">**Stato**</span><span class="sxs-lookup"><span data-stu-id="b1c63-111">**Status**</span></span>](status-property.md)

 

 