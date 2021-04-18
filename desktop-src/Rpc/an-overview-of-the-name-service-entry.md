---
title: Panoramica dell'immissione del nome del servizio
description: La voce servizio del nome è costituita da tre sezioni distinte.
ms.assetid: 3059a9a9-174d-4d04-8565-e4558f17f465
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc3855f586582b013bc47b11eb058ae461014f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298941"
---
# <a name="an-overview-of-the-name-service-entry"></a><span data-ttu-id="37bdb-103">Panoramica dell'immissione del nome del servizio</span><span class="sxs-lookup"><span data-stu-id="37bdb-103">An Overview of the Name Service Entry</span></span>

<span data-ttu-id="37bdb-104">La voce servizio del nome è costituita da tre sezioni distinte.</span><span class="sxs-lookup"><span data-stu-id="37bdb-104">The name service entry consists of three distinct sections.</span></span> <span data-ttu-id="37bdb-105">La prima sezione è per le interfacce (UUID + Version), la seconda sezione contiene gli UUID degli oggetti e la terza sezione è per gli handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="37bdb-105">The first section is for interfaces (UUID + version), the second section contains the object UUIDs, and the third section is for binding handles.</span></span> <span data-ttu-id="37bdb-106">Specificare un nome per la voce che fungerà da metodo per identificarlo.</span><span class="sxs-lookup"><span data-stu-id="37bdb-106">You provide a name for the entry that will serve as a way to identify it.</span></span>

<span data-ttu-id="37bdb-107">Quando si chiama [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta), il server specifica il nome della voce in cui inserire le informazioni esportate.</span><span class="sxs-lookup"><span data-stu-id="37bdb-107">When calling [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta), the server specifies the name of the entry in which to place the exported information.</span></span> <span data-ttu-id="37bdb-108">Questa interfaccia appena esportata viene quindi aggiunta alla sezione Interface della voce del servizio Name.</span><span class="sxs-lookup"><span data-stu-id="37bdb-108">This newly exported interface is then added to the interface section of the name service entry.</span></span> <span data-ttu-id="37bdb-109">Rimangono anche tutte le interfacce già presenti nella voce servizio del nome.</span><span class="sxs-lookup"><span data-stu-id="37bdb-109">Any interfaces that are already present in the name service entry remain as well.</span></span> <span data-ttu-id="37bdb-110">Questo stesso processo viene seguito per gli UUID degli oggetti e gli handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="37bdb-110">This same process is followed for object UUIDs and binding handles.</span></span>

<span data-ttu-id="37bdb-111">Il client chiama [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (o [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) per cercare un handle di binding appropriato.</span><span class="sxs-lookup"><span data-stu-id="37bdb-111">The client calls [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (or [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) to search for an appropriate binding handle.</span></span> <span data-ttu-id="37bdb-112">Vengono estratti il nome della voce, l'handle dell'interfaccia e l'UUID di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="37bdb-112">The entry name, interface handle, and an object UUID are extracted.</span></span> <span data-ttu-id="37bdb-113">Che limitano le voci da cui vengono restituiti gli handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="37bdb-113">These restrict the entries from which binding handles are returned.</span></span> <span data-ttu-id="37bdb-114">Se una voce corrisponde ai criteri di ricerca, tutti gli handle di binding in tale voce vengono restituiti da [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span><span class="sxs-lookup"><span data-stu-id="37bdb-114">If an entry matches the search criteria, all the binding handles in that entry are returned from [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span></span>

 

 




