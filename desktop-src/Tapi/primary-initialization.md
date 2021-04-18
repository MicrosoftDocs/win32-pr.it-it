---
description: Un'applicazione TAPI deve chiamare un'operazione di inizializzazione, che richiede una serie di azioni da TAPI e i provider di servizi che configurano l'ambiente di comunicazione per l'applicazione.
ms.assetid: 10df0fb4-08d6-4ba0-85f7-108cc4e237c1
title: Inizializzazione primaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcf37eecdee18861732dd27a4b134face9a17d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316039"
---
# <a name="primary-initialization"></a><span data-ttu-id="cb4bf-103">Inizializzazione primaria</span><span class="sxs-lookup"><span data-stu-id="cb4bf-103">Primary Initialization</span></span>

<span data-ttu-id="cb4bf-104">Un'applicazione TAPI deve chiamare un'operazione di inizializzazione, che richiede una serie di azioni da TAPI e i provider di servizi che configurano l'ambiente di comunicazione per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cb4bf-104">A TAPI application must call an initialization operation, which prompts a series of actions from TAPI and the service providers that set up the communication environment for the application.</span></span>

-   <span data-ttu-id="cb4bf-105">L'inizializzazione è sincrona e non restituisce alcun risultato fino a quando l'operazione non viene completata o non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="cb4bf-105">Initialization is synchronous and does not return until the operation is complete or has failed.</span></span>
-   <span data-ttu-id="cb4bf-106">Se TAPISRV non è già in esecuzione, TAPI lo avvia.</span><span class="sxs-lookup"><span data-stu-id="cb4bf-106">If TAPISRV is not already running, TAPI starts it.</span></span>
-   <span data-ttu-id="cb4bf-107">TAPI configura una connessione al processo TAPISRV.</span><span class="sxs-lookup"><span data-stu-id="cb4bf-107">TAPI sets up a connection to the TAPISRV process.</span></span>
-   <span data-ttu-id="cb4bf-108">TAPISVR carica i provider di servizi specificati nel registro di sistema e chiede di inizializzare i dispositivi supportati.</span><span class="sxs-lookup"><span data-stu-id="cb4bf-108">TAPISVR loads the service providers specified in the registry and prompts them to initialize the devices they support.</span></span>

<span data-ttu-id="cb4bf-109">**TAPI 2. x:** Le applicazioni eseguono l'inizializzazione chiamando [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="cb4bf-109">**TAPI 2.x:** Applications perform initialization by calling [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span></span>

<span data-ttu-id="cb4bf-110">**TAPI 3. x:** Le applicazioni chiamano [**ITTAPI:: Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize).</span><span class="sxs-lookup"><span data-stu-id="cb4bf-110">**TAPI 3.x:** Applications call [**ITTAPI::Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize).</span></span>

 

 
