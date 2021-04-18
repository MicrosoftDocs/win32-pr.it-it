---
description: WIA fornisce un livello di compatibilità TWAIN che consente alle applicazioni compatibili con TWAIN di comunicare con i dispositivi Windows Image Acquisition (WIA).
ms.assetid: 8e5673b9-c234-4722-b244-41aae015ac0c
title: Compatibilità con TWAIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afc7d0beb9a6001a0cbb4dc0bc032cf4df781736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307327"
---
# <a name="twain-compatibility"></a><span data-ttu-id="04e77-103">Compatibilità con TWAIN</span><span class="sxs-lookup"><span data-stu-id="04e77-103">TWAIN Compatibility</span></span>

<span data-ttu-id="04e77-104">WIA fornisce un livello di compatibilità TWAIN che consente alle applicazioni compatibili con TWAIN di comunicare con i dispositivi Windows Image Acquisition (WIA).</span><span class="sxs-lookup"><span data-stu-id="04e77-104">WIA provides a TWAIN compatibility layer that allows TWAIN-aware applications to communicate with Windows Image Acquisition (WIA) devices.</span></span> <span data-ttu-id="04e77-105">Le applicazioni compatibili con TWAIN non dispongono dell'accesso completo alla funzionalità WIA.</span><span class="sxs-lookup"><span data-stu-id="04e77-105">TWAIN-aware applications do not have full access to WIA functionality.</span></span> <span data-ttu-id="04e77-106">Ad esempio, un'applicazione non può escludere l'interfaccia utente utilizzando il livello di compatibilità TWAIN.</span><span class="sxs-lookup"><span data-stu-id="04e77-106">For example, an application cannot suppress the user interface using the TWAIN compatibility layer.</span></span>

<span data-ttu-id="04e77-107">I dispositivi WIA vengono visualizzati due volte in un'applicazione che è in grado di riconoscere sia WIA che TWAIN: una volta tramite la comunicazione WIA normale e una volta tramite il livello di compatibilità TWAIN.</span><span class="sxs-lookup"><span data-stu-id="04e77-107">WIA devices appear twice to an application that is aware of both WIA and TWAIN: once through normal WIA communication, and once through the TWAIN compatibility layer.</span></span> <span data-ttu-id="04e77-108">Per evitare l'inserimento di un dispositivo WIA due volte, un'applicazione che è a conoscenza di WIA e TWAIN deve filtrare i dispositivi WIA che passano attraverso il livello di compatibilità TWAIN.</span><span class="sxs-lookup"><span data-stu-id="04e77-108">To avoid listing a WIA device twice, an application that is aware of both WIA and TWAIN must filter out the WIA devices that come through the TWAIN compatibility layer.</span></span> <span data-ttu-id="04e77-109">Tutti i dispositivi WIA che passano attraverso il livello di compatibilità TWAIN hanno "WIA-" come prefisso, quindi è facile filtrarli.</span><span class="sxs-lookup"><span data-stu-id="04e77-109">All WIA devices that come through the TWAIN compatibility layer have "WIA-" as a prefix, so it is easy to filter them.</span></span>

 

 



