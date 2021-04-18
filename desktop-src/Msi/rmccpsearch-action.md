---
description: L'azione RMCCPSearch usa le firme dei file per convalidare che i prodotti idonei siano installati in un sistema prima di eseguire un'installazione dell'aggiornamento.
ms.assetid: d37b2434-86eb-4c6e-b817-77c75dcebbf5
title: Azione RMCCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c273ccb03bb77e0346edf73177d938d6002878a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309455"
---
# <a name="rmccpsearch-action"></a><span data-ttu-id="35a88-103">Azione RMCCPSearch</span><span class="sxs-lookup"><span data-stu-id="35a88-103">RMCCPSearch Action</span></span>

<span data-ttu-id="35a88-104">L'azione RMCCPSearch usa le firme dei file per convalidare che i prodotti idonei siano installati in un sistema prima di eseguire un'installazione dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="35a88-104">The RMCCPSearch action uses file signatures to validate that qualifying products are installed on a system before an upgrade installation is performed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="35a88-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="35a88-105">Sequence Restrictions</span></span>

<span data-ttu-id="35a88-106">È necessario creare l'azione RMCCPSearch nella tabella [InstallUISequence](installuisequence-table.md) e nella [tabella InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="35a88-106">RMCCPSearch action should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="35a88-107">Il programma di installazione impedisce l'esecuzione di RMCCPSearch nella sequenza InstallExecuteSequence se l'azione è già stata eseguita nella sequenza InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="35a88-107">The installer prevents RMCCPSearch from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="35a88-108">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="35a88-108">ActionData Messages</span></span>

<span data-ttu-id="35a88-109">Nessun messaggio ActionData.</span><span class="sxs-lookup"><span data-stu-id="35a88-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="35a88-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="35a88-110">Remarks</span></span>

<span data-ttu-id="35a88-111">Per l'azione RMCCPSearch è necessario impostare la proprietà dell' [**\_ unità CCP**](ccp-drive.md) sul percorso radice sul [*volume*](v-gly.md) rimovibile con l'installazione di uno dei prodotti idonei.</span><span class="sxs-lookup"><span data-stu-id="35a88-111">The RMCCPSearch action requires the [**CCP\_DRIVE**](ccp-drive.md) property to be set to the root path on the removable [*volume*](v-gly.md) that has the installation for any of the qualifying products.</span></span>

<span data-ttu-id="35a88-112">Ogni firma del file nella tabella CCPSearch viene cercata nel percorso a cui fa riferimento la proprietà dell' [**\_ unità CCP**](ccp-drive.md) usando la tabella [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="35a88-112">Each file signature in the CCPSearch table is searched for under the path referred to by the [**CCP\_DRIVE**](ccp-drive.md) property using the [DrLocator](drlocator-table.md) table.</span></span> <span data-ttu-id="35a88-113">L'assenza della firma dalla tabella delle [firme](signature-table.md) indica una directory.</span><span class="sxs-lookup"><span data-stu-id="35a88-113">The absence of the signature from the [Signature](signature-table.md) table denotes a directory.</span></span> <span data-ttu-id="35a88-114">Se viene determinata una firma esistente, l'azione RMCCPSearch viene terminata.</span><span class="sxs-lookup"><span data-stu-id="35a88-114">If any signature is determined to exist, the RMCCPSearch action terminates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35a88-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="35a88-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35a88-116">Tabella CCPSearch</span><span class="sxs-lookup"><span data-stu-id="35a88-116">CCPSearch table</span></span>](ccpsearch-table.md)
</dt> </dl>

 

 



