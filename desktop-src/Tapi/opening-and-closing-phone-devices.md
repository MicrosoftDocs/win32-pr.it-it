---
description: Dopo aver determinato le funzionalità di un dispositivo telefonico, un'applicazione deve aprire il dispositivo prima di poter accedere alle funzioni sul telefono.
ms.assetid: 0215db43-b4d7-4a1e-8d4f-d17013c14e61
title: Apertura e chiusura di dispositivi telefonici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4692901d09c680276bda1a5dba77bc57ce599e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308288"
---
# <a name="opening-and-closing-phone-devices"></a><span data-ttu-id="ff02f-103">Apertura e chiusura di dispositivi telefonici</span><span class="sxs-lookup"><span data-stu-id="ff02f-103">Opening and Closing Phone Devices</span></span>

<span data-ttu-id="ff02f-104">Dopo aver determinato le funzionalità di un dispositivo telefonico, un'applicazione deve aprire il dispositivo prima di poter accedere alle funzioni sul telefono.</span><span class="sxs-lookup"><span data-stu-id="ff02f-104">After determining the capabilities of a phone device, an application must open the device before it can access functions on that phone.</span></span> <span data-ttu-id="ff02f-105">Dopo che un dispositivo telefonico è stato aperto correttamente, l'applicazione viene restituita un handle che rappresenta il telefono aperto.</span><span class="sxs-lookup"><span data-stu-id="ff02f-105">After a phone device has been successfully opened, the application is returned a handle representing the open phone.</span></span> <span data-ttu-id="ff02f-106">Un dispositivo telefonico può essere aperto in modalità diverse, offrendo così un modo strutturato per condividere un dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="ff02f-106">A phone device can be opened in different modes, thus providing a structured way of sharing a phone device.</span></span>

<span data-ttu-id="ff02f-107">La funzione [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) apre il dispositivo telefonico specificato per consentire all'applicazione di accedere alle funzioni sul telefono.</span><span class="sxs-lookup"><span data-stu-id="ff02f-107">The [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) function opens the specified phone device to give the application access to functions on the phone.</span></span> <span data-ttu-id="ff02f-108">Un dispositivo telefonico viene identificato per **phoneOpen** per mezzo del relativo identificatore del dispositivo, che viene passato come parametro *dwDeviceID* .</span><span class="sxs-lookup"><span data-stu-id="ff02f-108">A phone device is identified to **phoneOpen** by means of its device identifier, which is passed as the *dwDeviceID* parameter.</span></span>

 

 



