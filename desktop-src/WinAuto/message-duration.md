---
title: Parametro Durata messaggio
description: Le applicazioni utilizzano in genere finestre popup per visualizzare brevemente messaggi di notifica importanti all'utente. Un'applicazione crea la finestra, la Visualizza per una durata definita dall'applicazione, quindi Elimina la finestra.
ms.assetid: a3f7a8d8-78e7-4fb0-8ee2-bd9341857153
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a99a43ace763da94944da334b0865c768cc920
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399151"
---
# <a name="message-duration-parameter"></a><span data-ttu-id="5fcf0-104">Parametro Durata messaggio</span><span class="sxs-lookup"><span data-stu-id="5fcf0-104">Message duration parameter</span></span>

<span data-ttu-id="5fcf0-105">Le applicazioni utilizzano in genere finestre popup per visualizzare brevemente messaggi di notifica importanti all'utente.</span><span class="sxs-lookup"><span data-stu-id="5fcf0-105">Applications typically use pop-up windows to briefly display important notification messages to the user.</span></span> <span data-ttu-id="5fcf0-106">Un'applicazione crea la finestra, la Visualizza per una durata definita dall'applicazione, quindi Elimina la finestra.</span><span class="sxs-lookup"><span data-stu-id="5fcf0-106">An application creates the window, displays it for an application-defined duration, and then destroys the window.</span></span>

<span data-ttu-id="5fcf0-107">Poiché gli utenti con condizioni cognitive o di problemi visivi potrebbero avere bisogno di più tempo per leggere i popup delle notifiche, le applicazioni non dovrebbero scrivere codice per la durata.</span><span class="sxs-lookup"><span data-stu-id="5fcf0-107">Because users with visual impairments or cognitive conditions might need more time to read notification pop-ups, applications should not hard code the duration.</span></span> <span data-ttu-id="5fcf0-108">Al contrario, un'applicazione deve impostare la durata in base al valore del parametro di sistema **\_ GETMESSAGEDURATION SPI** .</span><span class="sxs-lookup"><span data-stu-id="5fcf0-108">Instead, an application should set the duration based on the value of the **SPI\_GETMESSAGEDURATION** system parameter.</span></span> <span data-ttu-id="5fcf0-109">Per recuperare questo parametro, usare la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="5fcf0-109">To retrieve this parameter, use the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<span data-ttu-id="5fcf0-110">Le applicazioni Assistive Technology possono impostare la durata dei messaggi, in base all'input dell'utente, impostando il parametro di sistema **SPI \_ SETMESSAGEDURATION** .</span><span class="sxs-lookup"><span data-stu-id="5fcf0-110">Assistive technology applications can set the message duration, based on user input, by setting the **SPI\_SETMESSAGEDURATION** system parameter.</span></span>

 

 