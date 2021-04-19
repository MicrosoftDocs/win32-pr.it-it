---
description: Elenca le interfacce fornite dal motore degli allegati.
ms.assetid: 451587bd-a7ab-446b-b647-be98de251915
title: Interfacce di gestione della sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b3a205757a3bf324a5308a5f6fbc3d63374b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316642"
---
# <a name="security-management-interfaces"></a><span data-ttu-id="7ae06-103">Interfacce di gestione della sicurezza</span><span class="sxs-lookup"><span data-stu-id="7ae06-103">Security Management Interfaces</span></span>

<span data-ttu-id="7ae06-104">Questa sezione contiene le pagine di riferimento per i gruppi di interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ae06-104">This section contains reference pages for the following groups of interfaces:</span></span>

-   [<span data-ttu-id="7ae06-105">Interfacce del motore allegati</span><span class="sxs-lookup"><span data-stu-id="7ae06-105">Attachment Engine Interfaces</span></span>](#attachment-engine-interfaces)

## <a name="attachment-engine-interfaces"></a><span data-ttu-id="7ae06-106">Interfacce del motore allegati</span><span class="sxs-lookup"><span data-stu-id="7ae06-106">Attachment Engine Interfaces</span></span>



| <span data-ttu-id="7ae06-107">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="7ae06-107">Interface</span></span>                                                            | <span data-ttu-id="7ae06-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ae06-108">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ae06-109">**ISceSvcAttachmentData**</span><span class="sxs-lookup"><span data-stu-id="7ae06-109">**ISceSvcAttachmentData**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)               | <span data-ttu-id="7ae06-110">Recupera i dati di configurazione e analisi relativi a un servizio di sicurezza specificato dagli snap-in di configurazione della sicurezza. Gli snap-in configurazione di sicurezza espongono questa interfaccia, che consente alle estensioni degli snap-in di eseguire una chiamata alle informazioni di configurazione o di analisi.</span><span class="sxs-lookup"><span data-stu-id="7ae06-110">Retrieves configuration and analysis data about a specified security service from the Security Configuration snap-ins. The Security Configuration snap-ins expose this interface, which attachment snap-in extensions call to query configuration or analysis information.</span></span>                                                 |
| [<span data-ttu-id="7ae06-111">**ISceSvcAttachmentPersistInfo**</span><span class="sxs-lookup"><span data-stu-id="7ae06-111">**ISceSvcAttachmentPersistInfo**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) | <span data-ttu-id="7ae06-112">Recupera le informazioni di configurazione o analisi modificate da uno snap-in allegato.</span><span class="sxs-lookup"><span data-stu-id="7ae06-112">Retrieves modified configuration or analysis information from an attachment snap-in.</span></span> <span data-ttu-id="7ae06-113">Gli snap-in configurazione di sicurezza chiamano questa interfaccia per recuperare le informazioni modificate dall'estensione dello snap-in allegati.</span><span class="sxs-lookup"><span data-stu-id="7ae06-113">The Security Configuration snap-ins calls this interface to retrieve any modified information from the attachment snap-in extension.</span></span> <span data-ttu-id="7ae06-114">Lo snap-in Configurazione sicurezza archivia quindi questi dati in modo appropriato nel database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="7ae06-114">The Security Configuration snap-in then stores this data appropriately in the security database.</span></span> |



 

<span data-ttu-id="7ae06-115">Per ulteriori informazioni sulle interfacce COM che devono essere implementate dalle estensioni di snap-in, vedere la documentazione di [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .</span><span class="sxs-lookup"><span data-stu-id="7ae06-115">For more information about the COM interfaces that must be implemented by snap-in extensions, see the [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) documentation.</span></span>

 

 
