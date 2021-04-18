---
title: Sviluppare app piattaforma UWP (Universal Windows Platform) (UWP)
description: Sviluppare app piattaforma UWP (Universal Windows Platform) (UWP)
ms.assetid: 215256D7-CBBA-43B0-A99C-490A25D1F82C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3654c1c8773a813fcc7f88b21a86c2ef6049184
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "106299469"
---
# <a name="develop-universal-windows-platform-uwp-apps"></a><span data-ttu-id="24b01-103">Sviluppare app piattaforma UWP (Universal Windows Platform) (UWP)</span><span class="sxs-lookup"><span data-stu-id="24b01-103">Develop Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="24b01-104">Invitiamo tutti gli ISV di app desktop (Win32) a portare le app desktop al [piattaforma UWP (Universal Windows Platform) (UWP)](https://developer.microsoft.com/windows/bridges/desktop/) tramite il desktop Bridge.</span><span class="sxs-lookup"><span data-stu-id="24b01-104">We encourage all desktop (Win32) app ISVs to bring your desktop apps to the [Universal Windows Platform (UWP)](https://developer.microsoft.com/windows/bridges/desktop/) via the Desktop Bridge.</span></span> <span data-ttu-id="24b01-105">Le app UWP sono supportate anche in [Windows Store](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/), quindi risulta più semplice fornire agli utenti un aggiornamento di versione coerente, con conseguente riduzione dei costi di supporto.</span><span class="sxs-lookup"><span data-stu-id="24b01-105">UWP apps are also supported in the [Windows Store](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/), so it’s easier for you to update your users to a consistent version automatically, lowering your support costs.</span></span>

<span data-ttu-id="24b01-106">Se le app desktop non possono essere convertite tramite desktop Bridge, è consigliabile usare un programma di installazione che segue le procedure consigliate e assicurarsi che sia completamente testato.</span><span class="sxs-lookup"><span data-stu-id="24b01-106">If your desktop apps cannot be converted using the Desktop Bridge, we highly recommend that you use an installer that follows best practices, and ensure this is fully tested.</span></span> <span data-ttu-id="24b01-107">Un programma di installazione è l'utente o la prima esperienza del cliente con l'app.</span><span class="sxs-lookup"><span data-stu-id="24b01-107">An installer is your user or customer's first experience with your app.</span></span> <span data-ttu-id="24b01-108">Troppo spesso, questi programmi non funzionano correttamente o non vengono testati in modo accurato per tutti gli scenari.</span><span class="sxs-lookup"><span data-stu-id="24b01-108">All too often, this doesn’t work well or it hasn’t been fully tested for all scenarios.</span></span> <span data-ttu-id="24b01-109">Il [Kit di certificazione app Windows](https://dev.windows.com/develop/app-certification-kit) consente di testare l'installazione e la disinstallazione dell'app Win32 e di identificare l'uso di API non documentate, oltre ad altri problemi di base relativi alle prestazioni ottimali prima che vengano eseguite dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="24b01-109">The [Windows App Certification Kit](https://dev.windows.com/develop/app-certification-kit) can help you test install and uninstall of your Win32 app and help you identify use of undocumented APIs, as well as other basic performance-related best-practice issues before your users do.</span></span>

## <a name="best-practices"></a><span data-ttu-id="24b01-110">Procedure consigliate:</span><span class="sxs-lookup"><span data-stu-id="24b01-110">Best practices:</span></span>

-   <span data-ttu-id="24b01-111">Usa programmi di installazione compatibili sia con le versioni a 32 bit che con quelle a 64 bit di Windows.</span><span class="sxs-lookup"><span data-stu-id="24b01-111">Use installers that work for both 32-bit and 64-bit versions of Windows.</span></span>
-   <span data-ttu-id="24b01-112">Progetta i programmi di installazione per l'esecuzione in più scenari (livello utente o computer).</span><span class="sxs-lookup"><span data-stu-id="24b01-112">Design your installers to run on multiple scenarios (user or machine level).</span></span>
-   <span data-ttu-id="24b01-113">Mantieni tutti i componenti ridistribuibili Windows nel pacchetto originale. La modifica del pacchetto può causare malfunzionamenti del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="24b01-113">Keep all Windows redistributables in the original packaging – if you repackage these, it’s possible that this will break the installer.</span></span>
-   <span data-ttu-id="24b01-114">Pianifica tempi di sviluppo adeguati per i programmi di installazione. Spesso ne viene sottovalutata l'importanza durante il ciclo di vita di sviluppo del software.</span><span class="sxs-lookup"><span data-stu-id="24b01-114">Schedule development time for your installers—these are often overlooked as a deliverable during the software development lifecycle.</span></span>

 

 




