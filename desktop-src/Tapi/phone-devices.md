---
description: Il supporto dei dispositivi telefonici è supplementare anziché Basic, quindi i provider di servizi non devono supportare i dispositivi telefonici.
ms.assetid: 4d9f3b32-20d0-4550-9b3d-db97df8ea289
title: Dispositivi telefonici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f406442e43d8d4f31a89bfc0ccb1e59916d33e0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966854"
---
# <a name="phone-devices"></a><span data-ttu-id="63f8c-103">Dispositivi telefonici</span><span class="sxs-lookup"><span data-stu-id="63f8c-103">Phone Devices</span></span>

<span data-ttu-id="63f8c-104">Il supporto dei dispositivi telefonici è supplementare anziché Basic, quindi i provider di servizi non devono supportare i dispositivi telefonici.</span><span class="sxs-lookup"><span data-stu-id="63f8c-104">Phone device support is supplementary rather than basic, so service providers are not required to support phone devices.</span></span>

<span data-ttu-id="63f8c-105">Proprio come una classe di dispositivo linea è un'astrazione di un dispositivo a linee fisico, la classe del dispositivo Phone rappresenta un'astrazione indipendente dal dispositivo di un set di telefono.</span><span class="sxs-lookup"><span data-stu-id="63f8c-105">Just as a line device class is an abstraction of a physical line device, the phone device class represents a device-independent abstraction of a telephone set.</span></span> <span data-ttu-id="63f8c-106">TAPI considera i dispositivi line e Phone come dispositivi indipendenti l'uno dall'altro.</span><span class="sxs-lookup"><span data-stu-id="63f8c-106">TAPI treats line and phone devices as devices that are independent of each other.</span></span> <span data-ttu-id="63f8c-107">In altre parole, è possibile usare un telefono (dispositivo) senza usare una riga associata ed è possibile usare una linea (dispositivo) senza usare un telefono.</span><span class="sxs-lookup"><span data-stu-id="63f8c-107">In other words, you can use a phone (device) without using an associated line, and you can use a line (device) without using a phone.</span></span>

<span data-ttu-id="63f8c-108">I provider di servizi che implementano completamente questa indipendenza possono offrire usi per questi dispositivi non definiti dai protocolli di telefonia tradizionali.</span><span class="sxs-lookup"><span data-stu-id="63f8c-108">Service providers that fully implement this independence can offer uses for these devices not defined by traditional telephony protocols.</span></span> <span data-ttu-id="63f8c-109">Ad esempio, una persona può usare il telefono del telefono del desktop come dispositivo audio della forma d'onda per la registrazione o la riproduzione vocale, probabilmente senza la conoscenza del comunicatore che il telefono è in uso.</span><span class="sxs-lookup"><span data-stu-id="63f8c-109">For example, a person can use the handset of the desktop's phone as a waveform audio device for voice recording or playback, perhaps without the switch's knowledge that the phone is in use.</span></span> <span data-ttu-id="63f8c-110">In tale implementazione, il sollevamento del dispositivo telefonico locale non deve inviare automaticamente un segnale Offhook al Commuter.</span><span class="sxs-lookup"><span data-stu-id="63f8c-110">In such an implementation, lifting the local phone handset need not automatically send an offhook signal to the switch.</span></span>

<span data-ttu-id="63f8c-111">Questa indipendenza consente anche a un'applicazione di squillare il telefono locale in modo indipendente dalle chiamate in ingresso.</span><span class="sxs-lookup"><span data-stu-id="63f8c-111">This independence also allows an application to ring the local telephone in a manner that is independent of incoming calls.</span></span> <span data-ttu-id="63f8c-112">Le funzionalità dei provider di servizi sono limitate dalle funzionalità dell'hardware e del software utilizzati per collegare il commutirio, il telefono e il computer.</span><span class="sxs-lookup"><span data-stu-id="63f8c-112">The capabilities of service providers are limited by the capabilities of the hardware and software used to interconnect the switch, the phone, and the computer.</span></span>

<span data-ttu-id="63f8c-113">TAPI include funzioni per recuperare le funzionalità del dispositivo che consentono ai client di determinare se tale modello di utilizzo è supportato.</span><span class="sxs-lookup"><span data-stu-id="63f8c-113">TAPI includes functions to retrieve device capabilities that allow clients to determine whether such a usage model is supported.</span></span>

<span data-ttu-id="63f8c-114">In questa sezione vengono descritti i dispositivi telefonici e viene illustrato come utilizzare le funzioni del telefono TAPI per accedere a tali dispositivi.</span><span class="sxs-lookup"><span data-stu-id="63f8c-114">This section describes phone devices and explains how to use the TAPI phone functions to access these devices.</span></span>

-   [<span data-ttu-id="63f8c-115">Dispositivo telefonico</span><span class="sxs-lookup"><span data-stu-id="63f8c-115">Phone Device</span></span>](phone-device-elements.md)
-   [<span data-ttu-id="63f8c-116">Inizializzazione e arresto</span><span class="sxs-lookup"><span data-stu-id="63f8c-116">Initialization and Shutdown</span></span>](initialization-and-shutdown.md)

 

 



