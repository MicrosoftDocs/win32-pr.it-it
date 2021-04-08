---
title: Piattaforma sensore
description: Windows 7 ha modificato il modo in cui gli sviluppatori usano i sensori.
ms.assetid: ed323658-dfd6-4c1b-ada2-5d68ebb56482
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98fe94fd48ffa16080054a22b4d377ab4757d61d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046981"
---
# <a name="sensor-platform"></a><span data-ttu-id="9ac8a-103">Piattaforma sensore</span><span class="sxs-lookup"><span data-stu-id="9ac8a-103">Sensor Platform</span></span>

<span data-ttu-id="9ac8a-104">Windows 7 ha modificato il modo in cui gli sviluppatori usano i sensori.</span><span class="sxs-lookup"><span data-stu-id="9ac8a-104">Windows 7 has changed how developers use sensors.</span></span> <span data-ttu-id="9ac8a-105">Include il supporto nativo per i sensori, espanso da una nuova piattaforma di sviluppo per l'uso dei sensori, inclusi i sensori di posizione, ad esempio i dispositivi GPS (Global Positioning System).</span><span class="sxs-lookup"><span data-stu-id="9ac8a-105">It includes native support for sensors, expanded by a new development platform for working with sensors, including location sensors, such as Global Positioning Systems (GPS) devices.</span></span>

<span data-ttu-id="9ac8a-106">Basati sulla piattaforma dei sensori, le API di *Windows location* sono una nuova funzionalità di Windows 7 che consente agli sviluppatori di applicazioni di accedere alle informazioni sulla posizione fisica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9ac8a-106">Built on the Sensor Platform, the *Windows Location* APIs are a new Windows 7 feature that enables application developers to access the user's physical location information.</span></span> <span data-ttu-id="9ac8a-107">Le API di *Windows location* possono astrarre hardware, supportare contemporaneamente più applicazioni e passare facilmente da una tecnologia all'altra, evitando allo sviluppatore di applicazioni di gestire tali vincoli.</span><span class="sxs-lookup"><span data-stu-id="9ac8a-107">The *Windows Location* APIs can abstract hardware, simultaneously support multiple applications, and seamlessly switch between different technologies, relieving the application developer of the burden of managing these constraints.</span></span> <span data-ttu-id="9ac8a-108">Le API *location* possono essere utilizzate dai programmatori tramite il linguaggio di programmazione C++ (da parte dei programmatori che hanno familiarità con Component Object Model (com)) o utilizzando oggetti com in linguaggi di scripting, ad esempio Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="9ac8a-108">The *Location* APIs can be used by programmers through the C++ programming language (by programmers familiar with Component Object Model (COM)), or by using COM objects in scripting languages, such as Microsoft JScript.</span></span> <span data-ttu-id="9ac8a-109">Il supporto per gli script consente di accedere facilmente ai dati di posizione per progetti quali i gadget.</span><span class="sxs-lookup"><span data-stu-id="9ac8a-109">Scripting support gives easy access to location data for projects such as gadgets.</span></span>

<span data-ttu-id="9ac8a-110">Windows 7 offre una piattaforma solida e facile da usare per l'uso di dispositivi di sensori, ad esempio un sensore di luce di ambiente o un misuratore di temperatura, per creare la consapevolezza ambientale nelle applicazioni Windows.</span><span class="sxs-lookup"><span data-stu-id="9ac8a-110">Windows 7 provides a solid, easy-to-use platform for using sensor devices, such as an ambient light sensor or a temperature gauge, to create environmental awareness in Windows applications.</span></span> <span data-ttu-id="9ac8a-111">I PC possono usare i sensori incorporati nel computer, connessi tramite connessioni cablate o wireless o connessi tramite una rete o *Internet*.</span><span class="sxs-lookup"><span data-stu-id="9ac8a-111">PCs can use sensors that are built into the computer, connected through wired or wireless connections, or connected through a network or the *Internet*.</span></span>

<span data-ttu-id="9ac8a-112">Le API sensori e *località* forniscono un modo standard per *individuare i sensori* e accedere a livello di codice ai dati forniti dai sensori.</span><span class="sxs-lookup"><span data-stu-id="9ac8a-112">The *Sensor* and *Location* APIs provide a standard way to discover sensors, and to programmatically access data that sensors provide.</span></span>

<span data-ttu-id="9ac8a-113">Il pannello di controllo del *sensore* consente agli utenti di abilitare o disabilitare i sensori, controllare l'accesso ai sensori che potrebbero esporre dati sensibili, visualizzare le proprietà dei sensori e modificare le descrizioni dei sensori.</span><span class="sxs-lookup"><span data-stu-id="9ac8a-113">The *Sensor* control panel lets users enable or disable sensors, control access to sensors that might expose sensitive data, view sensor properties, and change the descriptions of sensors.</span></span>

<span data-ttu-id="9ac8a-114">L' [estensione della classe Sensor](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) è una parte essenziale del modello di sviluppo di driver per la piattaforma di sensori.</span><span class="sxs-lookup"><span data-stu-id="9ac8a-114">The [Sensor Class Extension](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) is a core part of the driver development model for the Sensor Platform.</span></span> <span data-ttu-id="9ac8a-115">Fornisce i meccanismi seguenti, che vengono utilizzati durante la scrittura di un driver del sensore [UMDF (User-Mode Driver Framework)](https://developer.microsoft.com/windows/hardware) :</span><span class="sxs-lookup"><span data-stu-id="9ac8a-115">It provides the following mechanisms, which are used when writing a [User-Mode Driver Framework (UMDF)](https://developer.microsoft.com/windows/hardware) sensor driver:</span></span>

-   <span data-ttu-id="9ac8a-116">Integrazione con la piattaforma dei sensori</span><span class="sxs-lookup"><span data-stu-id="9ac8a-116">Integration with the Sensor Platform</span></span>
-   <span data-ttu-id="9ac8a-117">Imposizione della sicurezza</span><span class="sxs-lookup"><span data-stu-id="9ac8a-117">Security enforcement</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ac8a-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9ac8a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ac8a-119">API per sensori</span><span class="sxs-lookup"><span data-stu-id="9ac8a-119">Sensor API</span></span>](../sensorsapi/portal.md)
</dt> <dt>