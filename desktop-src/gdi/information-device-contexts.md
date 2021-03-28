---
description: Il controller di dominio di informazioni viene usato per recuperare i dati predefiniti del dispositivo.
ms.assetid: 8fd05c17-e8c9-4747-9a66-ce7d958edeb9
title: Contesti di dispositivi informativi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002e9d5ebb6831f9e2251e76049e586ac3e84056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528326"
---
# <a name="information-device-contexts"></a><span data-ttu-id="88ee7-103">Contesti di dispositivi informativi</span><span class="sxs-lookup"><span data-stu-id="88ee7-103">Information Device Contexts</span></span>

<span data-ttu-id="88ee7-104">Il controller di dominio di informazioni viene usato per recuperare i dati predefiniti del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="88ee7-104">The information DC is used to retrieve default device data.</span></span> <span data-ttu-id="88ee7-105">Ad esempio, un'applicazione può chiamare la funzione [**create**](/windows/desktop/api/Wingdi/nf-wingdi-createica) per creare un controller di dominio di informazioni per un particolare modello di stampante e quindi chiamare le funzioni [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) e [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) per recuperare gli attributi predefiniti della penna o del pennello.</span><span class="sxs-lookup"><span data-stu-id="88ee7-105">For example, an application can call the [**CreateIC**](/windows/desktop/api/Wingdi/nf-wingdi-createica) function to create an information DC for a particular model of printer and then call the [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) and [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) functions to retrieve the default pen or brush attributes.</span></span> <span data-ttu-id="88ee7-106">Poiché il sistema è in grado di recuperare informazioni sul dispositivo senza creare le strutture normalmente associate ad altri tipi di contesti di dispositivo, un controller di dominio di informazioni comporta un sovraccarico molto inferiore e viene creato notevolmente più velocemente rispetto a qualsiasi altro tipo.</span><span class="sxs-lookup"><span data-stu-id="88ee7-106">Because the system can retrieve device information without creating the structures normally associated with the other types of device contexts, an information DC involves far less overhead and is created significantly faster than any of the other types.</span></span> <span data-ttu-id="88ee7-107">Al termine del recupero dei dati da parte di un'applicazione tramite un controller di dominio di informazioni, deve chiamare la funzione [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) .</span><span class="sxs-lookup"><span data-stu-id="88ee7-107">After an application finishes retrieving data by using an information DC, it must call the [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) function.</span></span>

 

 



