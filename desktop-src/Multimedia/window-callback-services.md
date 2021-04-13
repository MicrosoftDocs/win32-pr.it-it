---
title: Servizi di callback finestra
description: Servizi di callback finestra
ms.assetid: 227602e5-7ea1-4afd-ac88-cfeabe746d1f
keywords:
- audio multimediale, servizi di callback finestra
- audio, servizi di callback finestra
- mixer audio, servizi di callback finestra
- mixer, servizi di callback finestra
- Servizi di callback finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48faf2dd94b61f5d4fc47e073fe0f3875bcbb503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472971"
---
# <a name="window-callback-services"></a><span data-ttu-id="94b79-108">Servizi di callback finestra</span><span class="sxs-lookup"><span data-stu-id="94b79-108">Window Callback Services</span></span>

<span data-ttu-id="94b79-109">I servizi mixer forniscono servizi di callback finestra, in modo che l'applicazione possa elaborare i messaggi dai driver del mixer.</span><span class="sxs-lookup"><span data-stu-id="94b79-109">The mixer services provide window callback services so that your application can process messages from mixer drivers.</span></span> <span data-ttu-id="94b79-110">Per usare questi servizi, specificare il flag della finestra di CALLBACK \_ nel parametro *fdwOpen* e un handle di finestra nel parametro *dwCallback* della funzione [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) .</span><span class="sxs-lookup"><span data-stu-id="94b79-110">To use these services, specify the CALLBACK\_WINDOW flag in the *fdwOpen* parameter and a window handle in the *dwCallback* parameter of the [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen) function.</span></span> <span data-ttu-id="94b79-111">I messaggi del driver vengono inviati alla funzione della routine della finestra per la finestra identificata dall'handle in *dwCallback*.</span><span class="sxs-lookup"><span data-stu-id="94b79-111">Driver messages are sent to the window procedure function for the window identified by the handle in *dwCallback*.</span></span> <span data-ttu-id="94b79-112">I messaggi sono specifici del tipo di dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="94b79-112">The messages are specific to the audio device type.</span></span>

 

 