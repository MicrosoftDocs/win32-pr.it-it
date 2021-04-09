---
description: Le classi di dispositivi semplificano lo sviluppo consentendo ai programmatori di trattare i dispositivi con proprietà simili in modo analogo.
ms.assetid: 061f3037-1c71-4da1-88d7-29906c136d7b
title: Classe Device (TAPI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560f95b40ffa34f5e02ee7857928b75425fc7ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967471"
---
# <a name="device-class"></a><span data-ttu-id="e6c54-103">Classe Device</span><span class="sxs-lookup"><span data-stu-id="e6c54-103">Device Class</span></span>

<span data-ttu-id="e6c54-104">Le classi di dispositivi semplificano lo sviluppo consentendo ai programmatori di trattare i dispositivi con proprietà simili in modo analogo.</span><span class="sxs-lookup"><span data-stu-id="e6c54-104">Device classes simplify development by letting programmers treat devices that have similar properties in a similar manner.</span></span> <span data-ttu-id="e6c54-105">Un telefono digitale in un ufficio, ad esempio, ha in genere più funzionalità rispetto a un portatile standard in una casa, ma entrambi rispondono allo stesso modo a un set di funzioni di base ed entrambi appartengono a una classe di dispositivi telefonici.</span><span class="sxs-lookup"><span data-stu-id="e6c54-105">For example, a digital phone in an office typically has more capabilities than a standard handset in a home, but both respond in much the same way to a basic set of functions, and both belong to a phone device class.</span></span> <span data-ttu-id="e6c54-106">Le classi di dispositivi consentono di rendere TAPI estendibile offrendo un Framework da cui classificare e supportare nuove apparecchiature.</span><span class="sxs-lookup"><span data-stu-id="e6c54-106">Device classes help make TAPI extensible by providing a framework from which to classify and support new equipment.</span></span>

<span data-ttu-id="e6c54-107">Vedere [le classi di dispositivi TAPI](./tapi-device-classes.md) per le classi che TAPI ha predefinito.</span><span class="sxs-lookup"><span data-stu-id="e6c54-107">See [TAPI Device Classes](./tapi-device-classes.md) for classes that TAPI has predefined.</span></span> <span data-ttu-id="e6c54-108">Un provider di servizi può implementare e definire classi di dispositivi aggiuntive per le apparecchiature supportate.</span><span class="sxs-lookup"><span data-stu-id="e6c54-108">A service provider may implement and define additional device classes for the equipment it supports.</span></span> <span data-ttu-id="e6c54-109">Un'applicazione non deve mai essere in grado di individuare il provider di servizi che controlla il dispositivo, ma può richiedere informazioni sul controllo delle nuove classi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6c54-109">An application never needs to know which service provider controls which device, but may require information on the control of new device classes.</span></span>

<span data-ttu-id="e6c54-110">Un provider di servizi implementa una classe dispositivo eseguendo il mapping delle richieste ai comandi del dispositivo effettivi.</span><span class="sxs-lookup"><span data-stu-id="e6c54-110">A service provider implements a device class by mapping requests into actual device commands.</span></span> <span data-ttu-id="e6c54-111">Ad esempio, quando il provider di servizi per un modem compatibile con Hayes riceve un comando passato tramite TAPISVR per effettuare una chiamata, invia i comandi classici al modem.</span><span class="sxs-lookup"><span data-stu-id="e6c54-111">For example, when the service provider for a Hayes-compatible modem receives a command passed through TAPISVR to make a call, it sends classic AT commands to the modem.</span></span>

<span data-ttu-id="e6c54-112">L'interfaccia del provider di servizi può essere mappata a un'ampia gamma di ambienti, inclusi quelli non tradizionalmente considerati come appartenenti alla telefonia.</span><span class="sxs-lookup"><span data-stu-id="e6c54-112">The service provider interface can be mapped to a wide range of environments, including those not traditionally thought of as belonging to telephony.</span></span> <span data-ttu-id="e6c54-113">Un esempio è la conferenza multimediale su una rete basata su IP, ad esempio Internet.</span><span class="sxs-lookup"><span data-stu-id="e6c54-113">An example is multimedia conferencing over an IP-based network such as the Internet.</span></span>

<span data-ttu-id="e6c54-114">Gli sviluppatori di applicazioni devono tenere in considerazione l'esistenza di altre applicazioni che possono condividere servizi di telefonia.</span><span class="sxs-lookup"><span data-stu-id="e6c54-114">Application developers should keep in mind the existence of other applications that may share telephony services.</span></span>

 

 
