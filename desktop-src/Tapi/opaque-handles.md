---
description: Alcuni tipi definiti da TSPI sono handle opachi.
ms.assetid: e52ed691-0479-48da-9e06-c6a0d7a20e10
title: Handle opachi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df2e0b0f608b9cefc8f0f4f538bffd452a8aab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527097"
---
# <a name="opaque-handles"></a><span data-ttu-id="235ad-103">Handle opachi</span><span class="sxs-lookup"><span data-stu-id="235ad-103">Opaque Handles</span></span>

<span data-ttu-id="235ad-104">Alcuni tipi definiti da TSPI sono handle opachi.</span><span class="sxs-lookup"><span data-stu-id="235ad-104">A few types defined by TSPI are opaque handles.</span></span> <span data-ttu-id="235ad-105">Questi vengono usati in TSPI come riferimenti pubblici a strutture di dati private.</span><span class="sxs-lookup"><span data-stu-id="235ad-105">These are used in TSPI as public references to private data structures.</span></span> <span data-ttu-id="235ad-106">In questo modo è possibile controllare il tipo dei parametri forniti alle procedure dell'interfaccia, fornendo comunque una misura di protezione dei tipi.</span><span class="sxs-lookup"><span data-stu-id="235ad-106">This allows type-checking of parameters supplied to the interface procedures while still giving a measure of type protection.</span></span> <span data-ttu-id="235ad-107">Solo il proprietario della struttura di dati privata è in grado di interpretare il tipo opaco come riferimento alla relativa rappresentazione della struttura di dati.</span><span class="sxs-lookup"><span data-stu-id="235ad-107">Only the owner of the private data structure knows how to interpret the opaque type as a reference to its data structure representation.</span></span> <span data-ttu-id="235ad-108">Per un esempio di come vengono usati gli handle opachi, prendere in considerazione un dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="235ad-108">As an example of how opaque handles are used, consider a phone device.</span></span> <span data-ttu-id="235ad-109">Sia TAPI che il provider di servizi mantengono in genere le strutture dei dati che rappresentano le rispettive visualizzazioni del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="235ad-109">Both TAPI and the service provider typically maintain data structures representing their respective views of the device.</span></span>

<span data-ttu-id="235ad-110">Nelle tipiche strutture di dati del telefono gestite da TAPI e da un provider di servizi, ciascuna contiene un handle opaco per l'altra struttura di dati.</span><span class="sxs-lookup"><span data-stu-id="235ad-110">In typical phone data structures maintained by TAPI and a service provider, each contains an opaque handle for the other data structure.</span></span> <span data-ttu-id="235ad-111">Questi sono stati scambiati in un passaggio di inizializzazione iniziale.</span><span class="sxs-lookup"><span data-stu-id="235ad-111">These were exchanged at an early initialization step.</span></span> <span data-ttu-id="235ad-112">Quando TAPI chiama una funzione TSPI, passa l'handle opaco per fare riferimento al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="235ad-112">When TAPI calls a TSPI function, it passes the opaque handle to refer to the device.</span></span> <span data-ttu-id="235ad-113">Il provider di servizi è in grado di risolvere questo problema come riferimento (freccia) alla struttura dei dati.</span><span class="sxs-lookup"><span data-stu-id="235ad-113">The service provider knows how to resolve this as a reference (arrow) to its data structure.</span></span> <span data-ttu-id="235ad-114">Un processo simile si verifica quando il provider di servizi chiama una funzione di callback in TAPI.</span><span class="sxs-lookup"><span data-stu-id="235ad-114">A similar process occurs when the service provider calls a callback function in TAPI.</span></span>

 

 



