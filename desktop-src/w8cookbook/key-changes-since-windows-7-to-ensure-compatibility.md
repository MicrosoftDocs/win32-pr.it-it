---
title: Modifiche principali apportate da Windows 7 per garantire la compatibilità
description: Modifiche principali apportate da Windows 7 per garantire la compatibilità
ms.assetid: 6930AA8C-B9AE-44C0-BC7F-12342DBBEB5E
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ee24b18be55ff498d6c3870f77a32270df68284
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331615"
---
# <a name="key-changes-since-windows-7-to-ensure-compatibility"></a><span data-ttu-id="403e4-103">Modifiche principali apportate da Windows 7 per garantire la compatibilità</span><span class="sxs-lookup"><span data-stu-id="403e4-103">Key changes since Windows 7 to ensure compatibility</span></span>

<span data-ttu-id="403e4-104">Microsoft è consapevole dell'importanza della compatibilità per gli sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="403e4-104">We understand that compatibility matters to developers.</span></span> <span data-ttu-id="403e4-105">ISV e sviluppatori vogliono essere certi che le loro app vengano eseguite come previsto in tutte le versioni supportate del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="403e4-105">ISVs and developers want to ensure their apps will run as expected on all supported versions of the Windows OS.</span></span> <span data-ttu-id="403e4-106">Per i consumatori e le aziende sono in gioco investimenti importanti: è fondamentale che le app che hanno acquistato continuino a funzionare.</span><span class="sxs-lookup"><span data-stu-id="403e4-106">Consumers and businesses have a key investment here—they want to ensure that the apps they have paid for will continue to work.</span></span> <span data-ttu-id="403e4-107">È noto come la compatibilità sia un criterio fondamentale per le decisioni sugli acquisti.</span><span class="sxs-lookup"><span data-stu-id="403e4-107">We know that compatibility is the primary criteria for purchase decisions.</span></span> <span data-ttu-id="403e4-108">Le app scritte in modo corretto in base alle procedure consigliate causano molto meno varianza del codice quando viene rilasciata una nuova versione di Windows e riducono la frammentazione. queste app hanno un investimento di progettazione ridotto per la manutenzione e un time-to-market più rapido.</span><span class="sxs-lookup"><span data-stu-id="403e4-108">Apps that are well written based on best practices will lead to much less code churn when a new Windows version is released, and will reduce fragmentation—these apps have a reduced engineering investment to maintain, and a faster time to market.</span></span>

<span data-ttu-id="403e4-109">Nell'era di Windows 7, l'approccio alla compatibilità è stato perlopiù reattivo.</span><span class="sxs-lookup"><span data-stu-id="403e4-109">In the Windows 7 timeframe, compatibility was very much a reactive approach.</span></span> <span data-ttu-id="403e4-110">In Windows 8 abbiamo iniziato ad adottare una prospettiva diversa, lavorando ai meccanismi interni di Windows per garantire che la compatibilità fosse incorporata e non il risultato di interventi successivi.</span><span class="sxs-lookup"><span data-stu-id="403e4-110">In Windows 8, we started looking at this differently, working within Windows to ensure that compatibility was by design rather than an afterthought.</span></span> <span data-ttu-id="403e4-111">Windows 10 è la versione più compatibile del sistema operativo sin dalla progettazione finora pubblicata.</span><span class="sxs-lookup"><span data-stu-id="403e4-111">Windows 10 is the most compatible-by-design version of the OS to date.</span></span> <span data-ttu-id="403e4-112">Ecco alcuni dei principali aspetti che hanno reso possibile tutto ciò:</span><span class="sxs-lookup"><span data-stu-id="403e4-112">Here are some key ways we accomplished this:</span></span>

-   <span data-ttu-id="403e4-113">Telemetria delle app: consente di comprendere la popolarità delle app nell'ecosistema Windows per informare i test di compatibilità.</span><span class="sxs-lookup"><span data-stu-id="403e4-113">App telemetry: this helps us understand app popularity in the Windows ecosystem to inform compatibility testing.</span></span>
-   <span data-ttu-id="403e4-114">Partenariati ISV: collaborare direttamente con partner esterni per fornire dati e risolvere i problemi riscontrati dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="403e4-114">ISV partnerships: work directly with external partners to provide them with data and help fix issues that our users experience.</span></span>
-   <span data-ttu-id="403e4-115">Revisioni della progettazione, rilevamento upstream: partner con team di funzionalità per ridurre il numero di modifiche di rilievo in Windows.</span><span class="sxs-lookup"><span data-stu-id="403e4-115">Design reviews, upstream detection: partner with feature teams to reduce the number of breaking changes in Windows.</span></span> <span data-ttu-id="403e4-116">La revisione per la compatibilità è un passaggio cruciale per i team responsabili delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="403e4-116">Compatibility review is a gate that our feature teams must pass.</span></span>
-   <span data-ttu-id="403e4-117">Maggiore controllo sulle modifiche apportate all'API & la comunicazione migliorata</span><span class="sxs-lookup"><span data-stu-id="403e4-117">Tighter control over API changes & improved communication</span></span>
-   <span data-ttu-id="403e4-118">Ciclo di volo e feedback: il popolamento di Windows Insider riceve compilazioni con volo che consentono di migliorare la capacità di individuare i problemi di compatibilità prima che una build finale venga rilasciata ai clienti.</span><span class="sxs-lookup"><span data-stu-id="403e4-118">Flighting and feedback loop: The Windows Insider population receives flighted builds that help improve our ability to find compatibility issues before a final build is released to customers.</span></span> <span data-ttu-id="403e4-119">Il processo di feedback non serve solo a mettere in evidenza i bug, ma conferma che vengono offerte le funzionalità desiderate dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="403e4-119">This feedback process not only exposes bugs, but ensures we are shipping features our users want.</span></span>

 

 




