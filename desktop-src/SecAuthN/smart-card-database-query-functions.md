---
description: Eseguire una query sul database delle smart card. Possono fornire un elenco di Smart Card fornite da un utente specifico, le interfacce e il provider di servizi primari di una scheda specifica, i gruppi di Reader definiti per il sistema e i lettori in un set di gruppi di lettori.
ms.assetid: a30cbb99-522c-4752-bfcd-75be608785f1
title: Funzioni di query di database per Smart Card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd74c15eb475d5de9ccce84ba5936b724c0d8d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232962"
---
# <a name="smart-card-database-query-functions"></a><span data-ttu-id="84cbc-104">Funzioni di query di database per Smart Card</span><span class="sxs-lookup"><span data-stu-id="84cbc-104">Smart Card Database Query Functions</span></span>

<span data-ttu-id="84cbc-105">Le funzioni seguenti eseguono una query sul [*database delle smart card*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="84cbc-105">The following functions query the [*smart card database*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="84cbc-106">Possono fornire un elenco di Smart Card fornite da un utente specifico, le interfacce e il [*provider di servizi primari*](../secgloss/p-gly.md) di una scheda specifica, i [*gruppi di Reader*](../secgloss/r-gly.md) definiti per il sistema e i [*lettori*](../secgloss/r-gly.md) in un set di gruppi di lettori.</span><span class="sxs-lookup"><span data-stu-id="84cbc-106">They can provide a list of smart cards supplied by a specific user, the interfaces and [*primary service provider*](../secgloss/p-gly.md) of a specific card, the [*reader groups*](../secgloss/r-gly.md) defined for the system, and the [*readers*](../secgloss/r-gly.md) within a set of reader groups.</span></span>

<span data-ttu-id="84cbc-107">Quando si usano queste funzioni, è possibile eseguire una query sul database completo delle smart card oppure è possibile limitare la ricerca impostando il [*contesto di Resource Manager*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="84cbc-107">When you use these functions, you can query the complete smart card database, or you can narrow the search by setting the [*resource manager context*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="84cbc-108">Il contesto di Resource Manager viene impostato chiamando [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) prima di chiamare una funzione di query.</span><span class="sxs-lookup"><span data-stu-id="84cbc-108">The resource manager context is set by calling [**SCardEstablishContext**](/windows/desktop/api/Winscard/nf-winscard-scardestablishcontext) before calling a query function.</span></span>

> [!Note]  
> <span data-ttu-id="84cbc-109">Senza un contesto specificato, alcune informazioni potrebbero essere ancora inaccessibili a causa di restrizioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="84cbc-109">Without a specified context, some information may still be inaccessible due to security restrictions.</span></span>

 



| <span data-ttu-id="84cbc-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="84cbc-110">Topic</span></span>                                                  | <span data-ttu-id="84cbc-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84cbc-111">Description</span></span>                                                                                                                                                                          |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84cbc-112">**SCardGetProviderId**</span><span class="sxs-lookup"><span data-stu-id="84cbc-112">**SCardGetProviderId**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetproviderida)       | <span data-ttu-id="84cbc-113">Recuperare l'identificatore (GUID) del [*provider di servizi primario*](../secgloss/p-gly.md) per la scheda specificata.</span><span class="sxs-lookup"><span data-stu-id="84cbc-113">Retrieve the identifier (GUID) of the [*primary service provider*](../secgloss/p-gly.md) for the given card.</span></span> |
| [<span data-ttu-id="84cbc-114">**SCardListCards**</span><span class="sxs-lookup"><span data-stu-id="84cbc-114">**SCardListCards**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistcardsa)               | <span data-ttu-id="84cbc-115">Recuperare un elenco di schede introdotte in precedenza dal sistema da un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="84cbc-115">Retrieve a list of cards previously introduced to the system by a specific user.</span></span>                                                                                                     |
| [<span data-ttu-id="84cbc-116">**SCardListInterfaces**</span><span class="sxs-lookup"><span data-stu-id="84cbc-116">**SCardListInterfaces**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistinterfacesa)     | <span data-ttu-id="84cbc-117">Recuperare gli identificatori (GUID) delle interfacce fornite da una scheda specificata.</span><span class="sxs-lookup"><span data-stu-id="84cbc-117">Retrieve the identifiers (GUIDs) of the interfaces supplied by a given card.</span></span>                                                                                                         |
| [<span data-ttu-id="84cbc-118">**SCardListReaderGroups**</span><span class="sxs-lookup"><span data-stu-id="84cbc-118">**SCardListReaderGroups**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistreadergroupsa) | <span data-ttu-id="84cbc-119">Recuperare un elenco di gruppi di Reader introdotti in precedenza nel sistema.</span><span class="sxs-lookup"><span data-stu-id="84cbc-119">Retrieve a list of reader groups that have previously been introduced to the system.</span></span>                                                                                                 |
| [<span data-ttu-id="84cbc-120">**SCardListReaders**</span><span class="sxs-lookup"><span data-stu-id="84cbc-120">**SCardListReaders**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardlistreadersa)           | <span data-ttu-id="84cbc-121">Recuperare l'elenco di Reader in un set di gruppi di Reader denominati.</span><span class="sxs-lookup"><span data-stu-id="84cbc-121">Retrieve the list of readers within a set of named reader groups.</span></span>                                                                                                                    |



 

 

 
