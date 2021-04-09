---
description: TAPI consente di accedere alla visualizzazione di un telefono.
ms.assetid: f6017ecc-b2a0-4a92-8c28-ce7411f8dd84
title: Visualizza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dd813297c1d4624bb37cea8d833f63bcebeeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129307"
---
# <a name="display"></a><span data-ttu-id="efaa2-103">Visualizza</span><span class="sxs-lookup"><span data-stu-id="efaa2-103">Display</span></span>

<span data-ttu-id="efaa2-104">TAPI consente di accedere alla visualizzazione di un telefono.</span><span class="sxs-lookup"><span data-stu-id="efaa2-104">TAPI provides access to a phone's display.</span></span> <span data-ttu-id="efaa2-105">La visualizzazione viene modellata come area alfanumerica con righe e colonne.</span><span class="sxs-lookup"><span data-stu-id="efaa2-105">The display is modeled as an alphanumeric area with rows and columns.</span></span> <span data-ttu-id="efaa2-106">Le funzionalità del dispositivo del telefono indicano le dimensioni dello schermo di un telefono come il numero di righe e il numero di colonne.</span><span class="sxs-lookup"><span data-stu-id="efaa2-106">A phone's device capabilities indicate the size of a phone's display as the number of rows and the number of columns.</span></span> <span data-ttu-id="efaa2-107">Entrambi questi numeri sono pari a zero se il dispositivo telefonico non dispone di una visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="efaa2-107">Both these numbers are zero if the phone device does not have a display.</span></span> <span data-ttu-id="efaa2-108">Usare [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) per scrivere informazioni nella visualizzazione di un dispositivo telefonico aperto e [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) per recuperare il contenuto corrente della visualizzazione di un telefono.</span><span class="sxs-lookup"><span data-stu-id="efaa2-108">Use [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) to write information to the display of an open phone device, and [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) to retrieve the current contents of a phone's display.</span></span>

<span data-ttu-id="efaa2-109">Quando viene modificata la visualizzazione di un dispositivo telefonico, viene inviato un messaggio di [**\_ stato telefonico**](phone-state.md) alla funzione dell'applicazione per notificare all'applicazione la modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="efaa2-109">When the display of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application function to notify the application about the state change.</span></span> <span data-ttu-id="efaa2-110">I parametri di questo messaggio forniscono un'indicazione della modifica.</span><span class="sxs-lookup"><span data-stu-id="efaa2-110">Parameters to this message provide an indication of the change.</span></span>

 

 



