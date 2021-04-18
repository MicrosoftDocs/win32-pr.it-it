---
description: La piattaforma sensore e posizione di Windows include le impostazioni di privacy per aiutare a proteggere le informazioni personali degli utenti.
ms.assetid: 24425ed2-7b94-4b05-b117-9118d2074f49
title: Privacy e sicurezza nella piattaforma sensore e posizione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cb0bf50cd27de1fc7fd4f42bd7a8455a549eea3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306363"
---
# <a name="privacy-and-security-in-the-windows-sensor-and-location-platform"></a><span data-ttu-id="04e54-103">Privacy e sicurezza nella piattaforma sensore e posizione di Windows</span><span class="sxs-lookup"><span data-stu-id="04e54-103">Privacy and Security in the Windows Sensor and Location Platform</span></span>

<span data-ttu-id="04e54-104">La piattaforma sensore e posizione di Windows include le impostazioni di privacy per aiutare a proteggere le informazioni personali degli utenti.</span><span class="sxs-lookup"><span data-stu-id="04e54-104">The Windows Sensor and Location platform includes privacy settings to help protect users' personal information.</span></span>

<span data-ttu-id="04e54-105">La piattaforma consente di garantire che i dati dei sensori rimangano privati, quando è necessaria la riservatezza, nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="04e54-105">The platform helps to ensure that sensor data remains private, when privacy is required, in the following ways:</span></span>

-   <span data-ttu-id="04e54-106">Per impostazione predefinita, i sensori sono spenti.</span><span class="sxs-lookup"><span data-stu-id="04e54-106">By default, sensors are off.</span></span> <span data-ttu-id="04e54-107">Poiché la progettazione della piattaforma presuppone che qualsiasi sensore possa fornire dati personali, ogni sensore viene disabilitato fino a quando l'utente non fornisce il consenso esplicito per accedere ai dati del sensore.</span><span class="sxs-lookup"><span data-stu-id="04e54-107">Because the platform design presumes that any sensor can provide personal data, each sensor is disabled until the user provides explicit consent to access the sensor data.</span></span>
-   <span data-ttu-id="04e54-108">Windows fornisce messaggi di divulgazione e contenuto della Guida per l'utente.</span><span class="sxs-lookup"><span data-stu-id="04e54-108">Windows provides disclosure messages and Help content for the user.</span></span> <span data-ttu-id="04e54-109">Questo contenuto consente agli utenti di comprendere in che modo i sensori possono influenzare la privacy dei dati personali e aiutare gli utenti a prendere decisioni informate.</span><span class="sxs-lookup"><span data-stu-id="04e54-109">This content helps users understand how sensors can affect the privacy of their personal data and helps users make informed decisions.</span></span>
-   <span data-ttu-id="04e54-110">Per fornire l'autorizzazione per un sensore sono necessari i diritti di amministratore.</span><span class="sxs-lookup"><span data-stu-id="04e54-110">Providing permission for a sensor requires administrator rights.</span></span>
-   <span data-ttu-id="04e54-111">Quando è abilitata, un dispositivo sensore funziona per tutti i programmi in esecuzione con un determinato account utente (o per tutti gli account utente).</span><span class="sxs-lookup"><span data-stu-id="04e54-111">When it is enabled, a sensor device works for all programs running under a particular user account (or for all user accounts).</span></span> <span data-ttu-id="04e54-112">Sono inclusi gli utenti e i servizi non interattivi, ad esempio ASPNET o SYSTEM.</span><span class="sxs-lookup"><span data-stu-id="04e54-112">This includes noninteractive users and services, such as ASPNET or SYSTEM.</span></span> <span data-ttu-id="04e54-113">Ad esempio, se si Abilita un sensore GPS per l'account utente, solo i programmi in esecuzione con l'account utente hanno accesso al GPS.</span><span class="sxs-lookup"><span data-stu-id="04e54-113">For example, if you enable a GPS sensor for your user account, only programs running under your user account have access to the GPS.</span></span> <span data-ttu-id="04e54-114">Se si Abilita il GPS per tutti gli utenti, qualsiasi programma in esecuzione con qualsiasi account utente avrà accesso al GPS.</span><span class="sxs-lookup"><span data-stu-id="04e54-114">If you enable the GPS for all users, any program running under any user account has access to the GPS.</span></span>
-   <span data-ttu-id="04e54-115">I programmi che usano i sensori possono chiamare un metodo per aprire una finestra di dialogo di sistema che richiede agli utenti di abilitare i dispositivi sensori necessari.</span><span class="sxs-lookup"><span data-stu-id="04e54-115">Programs that use sensors can call a method to open a system dialog box that prompts users to enable needed sensor devices.</span></span> <span data-ttu-id="04e54-116">Questa funzionalità rende più semplice per gli sviluppatori e gli utenti verificare che i sensori funzionino quando sono necessari ai programmi, mantenendo al tempo stesso il controllo della divulgazione dei dati del sensore.</span><span class="sxs-lookup"><span data-stu-id="04e54-116">This feature makes it easy for developers and users to make sure that sensors work when programs need them, while maintaining user control of disclosure of sensor data.</span></span>
-   <span data-ttu-id="04e54-117">I driver dei sensori utilizzano un oggetto speciale che elabora tutte le richieste di I/O.</span><span class="sxs-lookup"><span data-stu-id="04e54-117">Sensor drivers use a special object that processes all I/O requests.</span></span> <span data-ttu-id="04e54-118">Questo oggetto assicura che solo i programmi che dispongono dell'autorizzazione utente possano accedere ai dati del sensore.</span><span class="sxs-lookup"><span data-stu-id="04e54-118">This object makes sure that only programs that have user permission can access sensor data.</span></span>

 

 



