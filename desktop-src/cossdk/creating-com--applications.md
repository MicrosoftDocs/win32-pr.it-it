---
description: Creazione di applicazioni COM+
ms.assetid: 32828d4d-aa98-4e6a-b7de-2ec832024517
title: Creazione di applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42a4b7ad18dab3f7163f527626322e05671e7be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305329"
---
# <a name="creating-com-applications"></a><span data-ttu-id="b1c7e-103">Creazione di applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="b1c7e-103">Creating COM+ Applications</span></span>

<span data-ttu-id="b1c7e-104">In questa sezione viene descritto come creare una nuova applicazione COM+ (vuota), quindi aggiungere componenti a tale applicazione.</span><span class="sxs-lookup"><span data-stu-id="b1c7e-104">This section describes how to create a new (empty) COM+ application and then add components to that application.</span></span> <span data-ttu-id="b1c7e-105">Viene inoltre descritto come aggiungere e rimuovere componenti COM da applicazioni COM+ esistenti e come spostare e copiare componenti da un'applicazione COM+ a un'altra.</span><span class="sxs-lookup"><span data-stu-id="b1c7e-105">It also describes how to add COM components to, and remove them from, existing COM+ applications, and how to move and copy components from one COM+ application to another.</span></span>



| <span data-ttu-id="b1c7e-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="b1c7e-106">Topic</span></span>                                                                                                       | <span data-ttu-id="b1c7e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1c7e-107">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1c7e-108">Creazione di una nuova applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="b1c7e-108">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)<br/>                           | <span data-ttu-id="b1c7e-109">Viene descritto come creare una nuova applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="b1c7e-109">Describes how to create a new COM+ application.</span></span><br/>                         |
| [<span data-ttu-id="b1c7e-110">Installazione di nuovi componenti</span><span class="sxs-lookup"><span data-stu-id="b1c7e-110">Installing New Components</span></span>](installing-new-components.md)<br/>                                       | <span data-ttu-id="b1c7e-111">Viene descritto come installare nuovi componenti di.</span><span class="sxs-lookup"><span data-stu-id="b1c7e-111">Describes how to install new components.</span></span><br/>                                |
| [<span data-ttu-id="b1c7e-112">Importazione di componenti</span><span class="sxs-lookup"><span data-stu-id="b1c7e-112">Importing Components</span></span>](importing-components.md)<br/>                                                 | <span data-ttu-id="b1c7e-113">Viene descritto come importare i componenti di.</span><span class="sxs-lookup"><span data-stu-id="b1c7e-113">Describes how to import components.</span></span><br/>                                     |
| [<span data-ttu-id="b1c7e-114">Rimozione di un componente da un'applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="b1c7e-114">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)<br/> | <span data-ttu-id="b1c7e-115">Viene descritto come eliminare un componente da un'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="b1c7e-115">Describes how to delete a component from a COM+ application.</span></span><br/>            |
| [<span data-ttu-id="b1c7e-116">Spostamento dei componenti</span><span class="sxs-lookup"><span data-stu-id="b1c7e-116">Moving Components</span></span>](moving-components.md)<br/>                                                       | <span data-ttu-id="b1c7e-117">Viene descritto come spostare un componente da un'applicazione COM+ a un'altra.</span><span class="sxs-lookup"><span data-stu-id="b1c7e-117">Describes how to move a component from one COM+ application to another.</span></span><br/> |
| [<span data-ttu-id="b1c7e-118">Copia di componenti</span><span class="sxs-lookup"><span data-stu-id="b1c7e-118">Copying Components</span></span>](copying-components.md)<br/>                                                     | <span data-ttu-id="b1c7e-119">Viene descritto come copiare un componente da un'applicazione COM+ a un'altra.</span><span class="sxs-lookup"><span data-stu-id="b1c7e-119">Describes how to copy a component from one COM+ application to another.</span></span><br/> |
| [<span data-ttu-id="b1c7e-120">Eliminazione di un'applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="b1c7e-120">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)<br/>                                   | <span data-ttu-id="b1c7e-121">Viene descritto come eliminare un'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="b1c7e-121">Describes how to delete a COM+ application.</span></span><br/>                             |



 

<span data-ttu-id="b1c7e-122">Per informazioni concettuali sulle procedure descritte in questa sezione, vedere [Cenni preliminari](com--application-overview.md) sulle applicazioni com+ e [distribuzione di applicazioni com+](deploying-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="b1c7e-122">For conceptual information on the procedures described in this section, see [COM+ Application Overview](com--application-overview.md) and [Deploying COM+ Applications](deploying-com--applications.md).</span></span>

<span data-ttu-id="b1c7e-123">Per informazioni procedurali sulle attività amministrative necessarie per l'esportazione e l'installazione di applicazioni COM+, vedere l'argomento relativo all'installazione delle applicazioni COM+ nella Guida dell'amministratore di Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="b1c7e-123">For procedural information on the administrative tasks involved in exporting and installing COM+ applications, see "Installing COM+ Applications" in the Component Services Administrator's Guide.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1c7e-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b1c7e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1c7e-125">Automazione dell'amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="b1c7e-125">Automating COM+ Administration</span></span>](automating-com--administration.md)
</dt> <dt>

[<span data-ttu-id="b1c7e-126">Configurazione di applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="b1c7e-126">Configuring COM+ Applications</span></span>](configuring-com--applications.md)
</dt> <dt>

[<span data-ttu-id="b1c7e-127">Conversione di pacchetti MTS in applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="b1c7e-127">Conversion of MTS Packages to COM+ Applications</span></span>](conversion-of-mts-packages-to-com--applications.md)
</dt> </dl>

 

 




