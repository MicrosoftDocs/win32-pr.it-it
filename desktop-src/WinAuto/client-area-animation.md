---
title: Parametro animazione area client
description: Il flag di animazione dell'area client indica se l'utente desidera disabilitare le animazioni negli elementi dell'interfaccia utente.
ms.assetid: 4a3ec9da-d5ae-4cd9-8222-f02143895ce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c62e25fdb08022d53cbe9e818a0a1089988cd6a6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104224017"
---
# <a name="client-area-animation-parameter"></a><span data-ttu-id="6b7ef-103">Parametro animazione area client</span><span class="sxs-lookup"><span data-stu-id="6b7ef-103">Client area animation parameter</span></span>

<span data-ttu-id="6b7ef-104">Il parametro animazione area client indica se l'utente desidera disabilitare le animazioni negli elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="6b7ef-104">The client area animation parameter indicates whether the user wants to disable animations in UI elements.</span></span> <span data-ttu-id="6b7ef-105">Le funzionalità di visualizzazione, ad esempio il lampeggio, il lampeggio, lo sfarfallio e lo stato del contenuto possono causare convulsioni negli utenti con epilessia sensibile alle foto.</span><span class="sxs-lookup"><span data-stu-id="6b7ef-105">Display features such as flashing, blinking, flickering, and moving content can cause seizures in users with photo-sensitive epilepsy.</span></span> <span data-ttu-id="6b7ef-106">Questo parametro consente di abilitare o disabilitare tutte le animazioni di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="6b7ef-106">This parameter enables you to enable or disable all such animations.</span></span>

<span data-ttu-id="6b7ef-107">Le applicazioni usano i flag **SPI \_ GETCLIENTAREAANIMATION** e **SPI \_ SETCLIENTAREAANIMATION** con la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per attivare o disattivare le animazioni dell'area client.</span><span class="sxs-lookup"><span data-stu-id="6b7ef-107">Applications use the **SPI\_GETCLIENTAREAANIMATION** and **SPI\_SETCLIENTAREAANIMATION** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to turn client area animations on or off.</span></span>

 

 