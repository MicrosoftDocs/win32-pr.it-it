---
title: Scelta delle funzioni
description: Scelta delle funzioni
ms.assetid: ded3c578-5087-4e4f-bf21-2149cf72719d
keywords:
- Windows Media Player Mobile Skins, funzioni per audio
- interfacce, funzioni per l'audio
- creazione di interfacce, funzioni per l'audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a139dc21a7d10847a7920955988ec2b02fced0f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396690"
---
# <a name="choosing-the-functions"></a><span data-ttu-id="4ac66-106">Scelta delle funzioni</span><span class="sxs-lookup"><span data-stu-id="4ac66-106">Choosing the Functions</span></span>

<span data-ttu-id="4ac66-107">Lo scopo di questa interfaccia è fornire funzionalità di base per la riproduzione di audio.</span><span class="sxs-lookup"><span data-stu-id="4ac66-107">The purpose of this skin is to provide basic functionality for playing audio.</span></span> <span data-ttu-id="4ac66-108">Verranno usate le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4ac66-108">The following functions will be used:</span></span>



| <span data-ttu-id="4ac66-109">Funzione</span><span class="sxs-lookup"><span data-stu-id="4ac66-109">Function</span></span>                     | <span data-ttu-id="4ac66-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ac66-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ac66-111">Come playpause o PlayPauseStop\*</span><span class="sxs-lookup"><span data-stu-id="4ac66-111">PlayPause or PlayPauseStop\*</span></span> | <span data-ttu-id="4ac66-112">L'avvio dell'elemento multimediale è di importanza fondamentale.</span><span class="sxs-lookup"><span data-stu-id="4ac66-112">Starting the media item is of prime importance.</span></span> <span data-ttu-id="4ac66-113">Se si sta creando un'interfaccia per Windows Media Player 10 mobile o versione successiva, è necessario usare PlayPauseStop.</span><span class="sxs-lookup"><span data-stu-id="4ac66-113">If you are creating a skin for Windows Media Player 10 Mobile or later, then you should use PlayPauseStop.</span></span> <span data-ttu-id="4ac66-114">Se si utilizza una versione precedente di Windows Media Player Mobile, è necessario utilizzare come playpause.</span><span class="sxs-lookup"><span data-stu-id="4ac66-114">If you are working with an earlier version of Windows Media Player Mobile, then you must use PlayPause.</span></span> <span data-ttu-id="4ac66-115">Entrambe le funzioni forniscono la funzionalità aggiuntiva di sospensione, ma solo PlayPauseStop consente di arrestare una trasmissione in tempo reale quando la funzionalità di sospensione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="4ac66-115">Both functions give you the added functionality of pausing, but only PlayPauseStop allows you to stop a live broadcast when pause functionality is not available.</span></span> |
| <span data-ttu-id="4ac66-116">Interrompere</span><span class="sxs-lookup"><span data-stu-id="4ac66-116">Stop</span></span>                         | <span data-ttu-id="4ac66-117">Si desidera aggiungere stop per interrompere la riproduzione dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="4ac66-117">You will want to add Stop to stop playing the item.</span></span> <span data-ttu-id="4ac66-118">Se si sta creando un'interfaccia per Windows Media Player 10 mobile o versione successiva, la funzione PlayPauseStop fornisce già questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="4ac66-118">If you are creating a skin for Windows Media Player 10 Mobile or later, the PlayPauseStop function already provides this functionality.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="4ac66-119">Prossima</span><span class="sxs-lookup"><span data-stu-id="4ac66-119">Next</span></span>                         | <span data-ttu-id="4ac66-120">Se si dispone di una playlist, sarà possibile scegliere l'elemento successivo.</span><span class="sxs-lookup"><span data-stu-id="4ac66-120">If you have a playlist, you will want to be able to choose the next item.</span></span> <span data-ttu-id="4ac66-121">Questa operazione è necessaria per l'esplorazione di base dei file multimediali digitali.</span><span class="sxs-lookup"><span data-stu-id="4ac66-121">You need this for basic navigation of digital media.</span></span>                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="4ac66-122">Prev (Precedente)</span><span class="sxs-lookup"><span data-stu-id="4ac66-122">Prev</span></span>                         | <span data-ttu-id="4ac66-123">Sebbene sia possibile usare Next per scorrere la playlist fino a quando non si è arrivati all'inizio, l'aggiunta di Prev renderà più semplice per l'utente tornare indietro, oltre che avanti quando si naviga nella playlist.</span><span class="sxs-lookup"><span data-stu-id="4ac66-123">While you could use Next to cycle through the playlist until you came to the beginning, adding Prev will make it easy for the user to go backward as well as forward when navigating the playlist.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="4ac66-124">VolumeUp o VolumeDown\*</span><span class="sxs-lookup"><span data-stu-id="4ac66-124">VolumeUp or VolumeDown\*</span></span>     | <span data-ttu-id="4ac66-125">È necessario fornire all'utente la possibilità di attivare o disattivare il volume.</span><span class="sxs-lookup"><span data-stu-id="4ac66-125">You will want to provide the user with the ability to turn the volume up or down.</span></span>                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="4ac66-126">\*Disponibile per Windows Media Player 10 mobile o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="4ac66-126">\*Available for Windows Media Player 10 Mobile or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ac66-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ac66-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ac66-128">**Guida all'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="4ac66-128">**Skin Guide**</span></span>](skin-guide.md)
</dt> </dl>

 

 




