---
description: Elenca le interfacce nelle API di autenticazione.
ms.assetid: bde3bcae-2152-4589-92a0-b44d98f233ef
title: Interfacce di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b101fd4fdd3c518d24b5b6f798fcaa4e0327dd22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232048"
---
# <a name="authentication-interfaces"></a><span data-ttu-id="e5481-103">Interfacce di autenticazione</span><span class="sxs-lookup"><span data-stu-id="e5481-103">Authentication Interfaces</span></span>

<span data-ttu-id="e5481-104">Le interfacce di autenticazione vengono categorizzate in base all'utilizzo come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="e5481-104">Authentication interfaces are categorized according to usage as follows:</span></span>

-   [<span data-ttu-id="e5481-105">Interfacce smart card</span><span class="sxs-lookup"><span data-stu-id="e5481-105">Smart Card Interfaces</span></span>](#smart-card-interfaces)
-   [<span data-ttu-id="e5481-106">Interfacce di condivisione delle identità</span><span class="sxs-lookup"><span data-stu-id="e5481-106">Identity Sharing Interfaces</span></span>](#identity-sharing-interfaces)

## <a name="smart-card-interfaces"></a><span data-ttu-id="e5481-107">Interfacce smart card</span><span class="sxs-lookup"><span data-stu-id="e5481-107">Smart Card Interfaces</span></span>

<span data-ttu-id="e5481-108">Smart Card SDK fornisce le seguenti interfacce COM.</span><span class="sxs-lookup"><span data-stu-id="e5481-108">The Smart Card SDK provides the following COM interfaces.</span></span> <span data-ttu-id="e5481-109">I metodi per un'interfaccia specifica sono elencati nel sommario e nella pagina di riferimento per tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e5481-109">The methods for a specific interface are listed in the Table of Contents and on the reference page for that interface.</span></span>



| <span data-ttu-id="e5481-110">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="e5481-110">Interface</span></span>                                    | <span data-ttu-id="e5481-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5481-111">Description</span></span>                                                                                                                                                                              |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5481-112">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="e5481-112">**IByteBuffer**</span></span>](ibytebuffer.md)           | <span data-ttu-id="e5481-113">Gestisce un oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="e5481-113">Manages a stream object.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="e5481-114">**Scheda di**</span><span class="sxs-lookup"><span data-stu-id="e5481-114">**ISCard**</span></span>](iscard.md)                     | <span data-ttu-id="e5481-115">Apre e gestisce una connessione a una [*Smart Card*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="e5481-115">Opens and manages a connection to a [*smart card*](/windows/desktop/SecGloss/s-gly).</span></span>                                                                    |
| [<span data-ttu-id="e5481-116">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="e5481-116">**ISCardAuth**</span></span>](iscardauth.md)             | <span data-ttu-id="e5481-117">Autentica un'applicazione, una smart card o un utente.</span><span class="sxs-lookup"><span data-stu-id="e5481-117">Authenticates an application, smart card, or user.</span></span>                                                                                                                                       |
| [<span data-ttu-id="e5481-118">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="e5481-118">**ISCardCmd**</span></span>](iscardcmd.md)               | <span data-ttu-id="e5481-119">Costruisce e gestisce un' [*unità dati del protocollo dell'applicazione*](/windows/desktop/SecGloss/a-gly) Smart Card (APDU).</span><span class="sxs-lookup"><span data-stu-id="e5481-119">Constructs and manages a smart card [*Application Protocol Data Unit*](/windows/desktop/SecGloss/a-gly) (APDU).</span></span> |
| [<span data-ttu-id="e5481-120">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="e5481-120">**ISCardDatabase**</span></span>](iscarddatabase.md)     | <span data-ttu-id="e5481-121">Esegue operazioni del database di [*Resource Manager*](/windows/desktop/SecGloss/r-gly) per smart card.</span><span class="sxs-lookup"><span data-stu-id="e5481-121">Performs smart card [*resource manager*](/windows/desktop/SecGloss/r-gly) database operations.</span></span>                                              |
| [<span data-ttu-id="e5481-122">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="e5481-122">**ISCardFileAccess**</span></span>](iscardfileaccess.md) | <span data-ttu-id="e5481-123">Esegue Servizi file comuni, ad esempio l'individuazione, la selezione, la lettura, la scrittura, la creazione e l'eliminazione di file.</span><span class="sxs-lookup"><span data-stu-id="e5481-123">Performs common file services such as locating, selecting, reading, writing, creating, and deleting files.</span></span>                                                                               |
| [<span data-ttu-id="e5481-124">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="e5481-124">**ISCardISO7816**</span></span>](iscardiso7816.md)       | <span data-ttu-id="e5481-125">Costruisce un comando APDU.</span><span class="sxs-lookup"><span data-stu-id="e5481-125">Constructs an APDU command.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="e5481-126">**ISCardLocate**</span><span class="sxs-lookup"><span data-stu-id="e5481-126">**ISCardLocate**</span></span>](iscardlocate.md)         | <span data-ttu-id="e5481-127">Individua una smart card.</span><span class="sxs-lookup"><span data-stu-id="e5481-127">Locates a smart card.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="e5481-128">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="e5481-128">**ISCardManage**</span></span>](iscardmanage.md)         | <span data-ttu-id="e5481-129">Gestisce il sistema di smart card.</span><span class="sxs-lookup"><span data-stu-id="e5481-129">Manages the smart card system.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="e5481-130">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="e5481-130">**ISCardTypeConv**</span></span>](iscardtypeconv.md)     | <span data-ttu-id="e5481-131">Fornisce i metodi utilizzati per supportare altre interfacce COM per smart card.</span><span class="sxs-lookup"><span data-stu-id="e5481-131">Provides methods used to support other smart card COM interfaces.</span></span> <span data-ttu-id="e5481-132">Questa interfaccia viene fornita solo per compatibilità con le versioni precedenti e non deve più essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e5481-132">This interface is provided for backward compatibility only and should no longer be used.</span></span>                               |
| [<span data-ttu-id="e5481-133">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="e5481-133">**ISCardVerify**</span></span>](iscardverify.md)         | <span data-ttu-id="e5481-134">Verifica o modifica i criteri di verifica del contenitore di schede (CHV).</span><span class="sxs-lookup"><span data-stu-id="e5481-134">Verifies or changes card holder verification (CHV) policy.</span></span>                                                                                                                               |



 

## <a name="identity-sharing-interfaces"></a><span data-ttu-id="e5481-135">Interfacce di condivisione delle identità</span><span class="sxs-lookup"><span data-stu-id="e5481-135">Identity Sharing Interfaces</span></span>

<span data-ttu-id="e5481-136">Identity sharing SDK fornisce le seguenti interfacce COM.</span><span class="sxs-lookup"><span data-stu-id="e5481-136">The Identity Sharing SDK provides the following COM interfaces.</span></span> <span data-ttu-id="e5481-137">I metodi per un'interfaccia specifica sono elencati nel sommario e nella pagina di riferimento per tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e5481-137">The methods for a specific interface are listed in the Table of Contents and on the reference page for that interface.</span></span>



| <span data-ttu-id="e5481-138">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="e5481-138">Interface</span></span>                                                          | <span data-ttu-id="e5481-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5481-139">Description</span></span>                                                                              |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5481-140">**IAssociatedIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="e5481-140">**IAssociatedIdentityProvider**</span></span>](/windows/desktop/api/IdentityProvider/nn-identityprovider-iassociatedidentityprovider) | <span data-ttu-id="e5481-141">Consente a un provider di identità di associare le identità agli account utente locali.</span><span class="sxs-lookup"><span data-stu-id="e5481-141">Allows an identity provider to associate identities with local user accounts.</span></span>            |
| [<span data-ttu-id="e5481-142">**IIdentityAdvise**</span><span class="sxs-lookup"><span data-stu-id="e5481-142">**IIdentityAdvise**</span></span>](/windows/desktop/api/IdentityProvider/nn-identityprovider-iidentityadvise)                         | <span data-ttu-id="e5481-143">Consente a un provider di identità di notificare un'applicazione chiamante quando viene aggiornata un'identità.</span><span class="sxs-lookup"><span data-stu-id="e5481-143">Allows an identity provider to notify a calling application when an identity is updated.</span></span> |
| [<span data-ttu-id="e5481-144">**Metodo IIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="e5481-144">**IIdentityProvider**</span></span>](/windows/desktop/api/Identityprovider/nn-identityprovider-iidentityprovider)                     | <span data-ttu-id="e5481-145">Rappresenta un provider di identità.</span><span class="sxs-lookup"><span data-stu-id="e5481-145">Represents an identity provider.</span></span>                                                         |
| [<span data-ttu-id="e5481-146">**IIdentityStore**</span><span class="sxs-lookup"><span data-stu-id="e5481-146">**IIdentityStore**</span></span>](/windows/desktop/api/Identitystore/nn-identitystore-iidentitystore)                           | <span data-ttu-id="e5481-147">Fornisce metodi per enumerare e gestire identità e provider di identità.</span><span class="sxs-lookup"><span data-stu-id="e5481-147">Provides methods to enumerate and manage identities and identity providers.</span></span>              |



 

 

 
