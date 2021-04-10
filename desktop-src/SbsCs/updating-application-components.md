---
description: Gli assembly privati affiancati possono essere usati per creare componenti che possono essere facilmente aggiornati senza aggiornare anche l'applicazione host.
ms.assetid: 5a45ee79-3ae1-4e9b-a77e-d4209fb23fa8
title: Aggiornamento dei componenti dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba559323c3272db96f0cd106f0fc61624519b770
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966598"
---
# <a name="updating-application-components"></a><span data-ttu-id="f216b-103">Aggiornamento dei componenti dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="f216b-103">Updating Application Components</span></span>

<span data-ttu-id="f216b-104">Gli assembly privati affiancati possono essere usati per creare componenti che possono essere facilmente aggiornati senza aggiornare anche l'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="f216b-104">Side-by-side private assemblies can be used to create components that can be easily updated without also updating the hosting application.</span></span> <span data-ttu-id="f216b-105">Questo consente a un servizio di aggiornamento di installare i componenti aggiornati dell'applicazione, riavviare l'applicazione e fare in modo che l'applicazione usi le modifiche.</span><span class="sxs-lookup"><span data-stu-id="f216b-105">This allows an updating service to install the application's updated components, restart the application, and have the application use the changes.</span></span> <span data-ttu-id="f216b-106">Quando si utilizzano manifesti dell'applicazione, la funzionalità dei componenti ospitati da un'applicazione può essere aggiornata senza dover modificare il codice dell'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="f216b-106">When using application manifests, the functionality of components hosted by an application can be updated without having to change the hosting application's code.</span></span>

<span data-ttu-id="f216b-107">Questo metodo può essere utilizzato per aggiornare la versione delle risorse di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f216b-107">This method can be used to update the version of an application's resources.</span></span> <span data-ttu-id="f216b-108">Se, ad esempio, un'applicazione contiene un assembly, il manifesto dell'applicazione può specificare una dipendenza da questo assembly.</span><span class="sxs-lookup"><span data-stu-id="f216b-108">For example, if an application contains an assembly, the application's manifest can specify a dependency on this assembly.</span></span> <span data-ttu-id="f216b-109">L'applicazione può ottenere l'assembly chiamando [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) per trovare e caricare i file necessari.</span><span class="sxs-lookup"><span data-stu-id="f216b-109">The application can get the assembly by calling [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) to find and load the files it requires.</span></span> <span data-ttu-id="f216b-110">Un aggiornamento deve semplicemente arrestare i bit più recenti per l'assembly, che possono esistere side-by-side con una versione precedente dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="f216b-110">An updater simply has to bring down the newest bits for the assembly, which can exist side-by-side with an earlier version of the assembly.</span></span>

 

 
