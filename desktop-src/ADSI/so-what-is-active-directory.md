---
title: Panoramica dell'esercitazione ADSI con Visual Basic
description: Active Directory è un database per scopi specifici \ 8212; non si tratta di una sostituzione del registro di sistema.
ms.assetid: 899799e3-5ab9-4d19-883a-5bc9f20d2bad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607d9da26d1c96d7cb6f83a799c7633404e5bb4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104566424"
---
# <a name="tutorial-overview-adsi-with-visual-basic"></a><span data-ttu-id="1ae78-103">Panoramica dell'esercitazione: ADSI con Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1ae78-103">Tutorial Overview: ADSI with Visual Basic</span></span>

> [!Note]  
> <span data-ttu-id="1ae78-104">La documentazione seguente fa parte di una descrizione dello scenario esteso per gli sviluppatori Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1ae78-104">The following documentation is part of an extended scenario description for Visual Basic developers.</span></span> <span data-ttu-id="1ae78-105">Per una panoramica generale di Active Directory, vedere la [documentazione relativa ai professionisti IT in TechNet](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="1ae78-105">If you are looking for a general overview of Active Directory, see the [IT Pro docs on Technet](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)).</span></span> <span data-ttu-id="1ae78-106">Per un esame più approfondito del lato sviluppo di Active Directory, vedere [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services).</span><span class="sxs-lookup"><span data-stu-id="1ae78-106">For a more in-depth look at the development side of Active Directory, see [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services).</span></span> <span data-ttu-id="1ae78-107">Per un'introduzione più ampia alle interfacce del servizio Active Directory, vedere l'argomento padre di questo argomento: [Active Directory le interfacce del servizio](active-directory-service-interfaces-adsi.md), nonché l'argomento di pari livello: [informazioni sulle interfacce di servizio di Active Directory](about-adsi.md).</span><span class="sxs-lookup"><span data-stu-id="1ae78-107">For a larger introduction to Active Directory Service Interfaces, see this topic's parent topic: [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md), as well as the sibling topic: [About Active Directory Service Interfaces](about-adsi.md).</span></span>

 

<span data-ttu-id="1ae78-108">Active Directory è un database per scopi specifici, non si tratta di una sostituzione del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="1ae78-108">Active Directory is a special-purpose database — it is not a registry replacement.</span></span> <span data-ttu-id="1ae78-109">La directory è progettata per gestire un numero elevato di operazioni di lettura e ricerca e un numero significativamente inferiore di modifiche e aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="1ae78-109">The directory is designed to handle a large number of read and search operations and a significantly smaller number of changes and updates.</span></span> <span data-ttu-id="1ae78-110">I dati Active Directory sono gerarchici, replicati ed estendibili.</span><span class="sxs-lookup"><span data-stu-id="1ae78-110">Active Directory data is hierarchical, replicated, and extensible.</span></span> <span data-ttu-id="1ae78-111">Poiché è replicato, non si desidera archiviare i dati dinamici, ad esempio i prezzi delle scorte aziendali o le prestazioni della CPU.</span><span class="sxs-lookup"><span data-stu-id="1ae78-111">Because it is replicated, you do not want to store dynamic data, such as corporate stock prices or CPU performance.</span></span> <span data-ttu-id="1ae78-112">Se i dati sono specifici del computer, archiviare i dati nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="1ae78-112">If your data is machine-specific, store the data in the registry.</span></span> <span data-ttu-id="1ae78-113">Esempi tipici di dati archiviati nella directory includono i dati della coda della stampante, i dati di contatto dell'utente e i dati di configurazione di rete/computer.</span><span class="sxs-lookup"><span data-stu-id="1ae78-113">Typical examples of data stored in the directory include printer queue data, user contact data, and network/computer configuration data.</span></span> <span data-ttu-id="1ae78-114">Il database Active Directory è costituito da oggetti e attributi.</span><span class="sxs-lookup"><span data-stu-id="1ae78-114">The Active Directory database consists of objects and attributes.</span></span> <span data-ttu-id="1ae78-115">Gli oggetti e le definizioni degli attributi vengono archiviati nello schema di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1ae78-115">Objects and attribute definitions are stored in the Active Directory schema.</span></span>

<span data-ttu-id="1ae78-116">È possibile che si stiano chiedendo quali oggetti sono attualmente archiviati in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1ae78-116">You may be wondering what objects are currently stored in Active Directory.</span></span> <span data-ttu-id="1ae78-117">Active Directory dispone di tre partizioni.</span><span class="sxs-lookup"><span data-stu-id="1ae78-117">Active Directory has three partitions.</span></span> <span data-ttu-id="1ae78-118">Questi sono anche noti come contesti di denominazione: dominio, schema e configurazione.</span><span class="sxs-lookup"><span data-stu-id="1ae78-118">These are also known as naming contexts: domain, schema, and configuration.</span></span> <span data-ttu-id="1ae78-119">La partizione di dominio contiene utenti, gruppi, contatti, computer, unità organizzative e molti altri tipi di oggetto.</span><span class="sxs-lookup"><span data-stu-id="1ae78-119">The domain partition contains users, groups, contacts, computers, organizational units, and many other object types.</span></span> <span data-ttu-id="1ae78-120">Poiché Active Directory è estensibile, è anche possibile aggiungere classi e/o attributi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="1ae78-120">Because Active Directory is extensible, you can also add your own classes and/or attributes.</span></span> <span data-ttu-id="1ae78-121">La partizione dello schema contiene le classi e le definizioni di attributo.</span><span class="sxs-lookup"><span data-stu-id="1ae78-121">The schema partition contains classes and attribute definitions.</span></span> <span data-ttu-id="1ae78-122">La partizione di configurazione include i dati di configurazione per servizi, partizioni e siti.</span><span class="sxs-lookup"><span data-stu-id="1ae78-122">The configuration partition includes configuration data for services, partitions, and sites.</span></span>

<span data-ttu-id="1ae78-123">Lo screenshot seguente mostra la partizione del dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1ae78-123">The following screen shot shows the Active Directory domain partition.</span></span>

![partizione di dominio Active Directory](images/adadsi1.png)

## <a name="related-topics"></a><span data-ttu-id="1ae78-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1ae78-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ae78-126">Accesso a Active Directory tramite Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1ae78-126">Accessing Active Directory Using Visual Basic</span></span>](accessing-active-directory-using-visual-basic.md)
</dt> <dt>

[<span data-ttu-id="1ae78-127">Scenario: Fabrikam Corporation</span><span class="sxs-lookup"><span data-stu-id="1ae78-127">Scenario: The Fabrikam Corporation</span></span>](scenario--the-fabrikam-corporation.md)
</dt> <dt>

[<span data-ttu-id="1ae78-128">Argomenti avanzati</span><span class="sxs-lookup"><span data-stu-id="1ae78-128">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 