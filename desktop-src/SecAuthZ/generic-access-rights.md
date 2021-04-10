---
description: Gli oggetti a protezione diretta utilizzano un formato di maschera di accesso in cui i quattro bit più significativi specificano i diritti di accesso generici.
ms.assetid: e18cede9-9bf7-4866-850b-5d7fa43a5b0f
title: Diritti di accesso generici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adff14aa259222bc37096b8a94f30cffb5ab0876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758249"
---
# <a name="generic-access-rights"></a><span data-ttu-id="16d15-103">Diritti di accesso generici</span><span class="sxs-lookup"><span data-stu-id="16d15-103">Generic Access Rights</span></span>

<span data-ttu-id="16d15-104">Gli oggetti a protezione diretta utilizzano un [formato di maschera di accesso](access-mask-format.md) in cui i quattro bit più significativi specificano i diritti di accesso generici.</span><span class="sxs-lookup"><span data-stu-id="16d15-104">Securable objects use an [access mask format](access-mask-format.md) in which the four high-order bits specify generic access rights.</span></span> <span data-ttu-id="16d15-105">Ogni tipo di oggetto a protezione diretta esegue il mapping di questi bit a un set di diritti di accesso standard e specifici per gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="16d15-105">Each type of securable object maps these bits to a set of its standard and object-specific access rights.</span></span> <span data-ttu-id="16d15-106">Un oggetto file di Windows, ad esempio, esegue il mapping del \_ bit di lettura generico al \_ controllo Read e sincronizza i diritti di accesso standard e al file \_ leggere i \_ dati, i file di \_ lettura e i diritti di \_ accesso specifici per gli \_ \_ oggetti.</span><span class="sxs-lookup"><span data-stu-id="16d15-106">For example, a Windows file object maps the GENERIC\_READ bit to the READ\_CONTROL and SYNCHRONIZE standard access rights and to the FILE\_READ\_DATA, FILE\_READ\_EA, and FILE\_READ\_ATTRIBUTES object-specific access rights.</span></span> <span data-ttu-id="16d15-107">Altri tipi di oggetti mappano il \_ bit di lettura generico a qualsiasi set di diritti di accesso appropriato per quel tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="16d15-107">Other types of objects map the GENERIC\_READ bit to whatever set of access rights is appropriate for that type of object.</span></span>

<span data-ttu-id="16d15-108">È possibile usare i diritti di accesso generici per specificare il tipo di accesso necessario quando si apre un handle a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="16d15-108">You can use generic access rights to specify the type of access you need when you are opening a handle to an object.</span></span> <span data-ttu-id="16d15-109">Questa operazione è in genere più semplice rispetto a specificare tutti i diritti standard e specifici corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="16d15-109">This is typically simpler than specifying all the corresponding standard and specific rights.</span></span>

<span data-ttu-id="16d15-110">Nella tabella seguente vengono illustrate le costanti definite per i diritti di accesso generici.</span><span class="sxs-lookup"><span data-stu-id="16d15-110">The following table shows the constants defined for the generic access rights.</span></span>



| <span data-ttu-id="16d15-111">Costante</span><span class="sxs-lookup"><span data-stu-id="16d15-111">Constant</span></span>         | <span data-ttu-id="16d15-112">Significato generico</span><span class="sxs-lookup"><span data-stu-id="16d15-112">Generic meaning</span></span>            |
|------------------|----------------------------|
| <span data-ttu-id="16d15-113">tutti GENERIci \_</span><span class="sxs-lookup"><span data-stu-id="16d15-113">GENERIC\_ALL</span></span>     | <span data-ttu-id="16d15-114">Tutti i diritti di accesso possibili</span><span class="sxs-lookup"><span data-stu-id="16d15-114">All possible access rights</span></span> |
| <span data-ttu-id="16d15-115">esecuzione GENERIca \_</span><span class="sxs-lookup"><span data-stu-id="16d15-115">GENERIC\_EXECUTE</span></span> | <span data-ttu-id="16d15-116">Esegui accesso</span><span class="sxs-lookup"><span data-stu-id="16d15-116">Execute access</span></span>             |
| <span data-ttu-id="16d15-117">lettura GENERIca \_</span><span class="sxs-lookup"><span data-stu-id="16d15-117">GENERIC\_READ</span></span>    | <span data-ttu-id="16d15-118">accesso in lettura</span><span class="sxs-lookup"><span data-stu-id="16d15-118">Read access</span></span>                |
| <span data-ttu-id="16d15-119">scrittura GENERIca \_</span><span class="sxs-lookup"><span data-stu-id="16d15-119">GENERIC\_WRITE</span></span>   | <span data-ttu-id="16d15-120">Accesso in scrittura</span><span class="sxs-lookup"><span data-stu-id="16d15-120">Write access</span></span>               |



 

<span data-ttu-id="16d15-121">Anche le applicazioni che definiscono oggetti a protezione diretta privati possono usare i diritti di accesso generici.</span><span class="sxs-lookup"><span data-stu-id="16d15-121">Applications that define private securable objects can also use the generic access rights.</span></span>

 

 



