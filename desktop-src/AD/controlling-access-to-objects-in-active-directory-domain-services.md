---
title: Controllo dell'accesso agli oggetti in Active Directory Domain Services
description: Ogni oggetto del servizio di Active Directory directory è protetto dalla sicurezza di Windows 2000.
ms.assetid: 0821069d-76bd-49cb-a617-8446d26e61d9
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, utilizzo, sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cac744ef63fa95c45d5af535f5155378d479fdb
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/04/2019
ms.locfileid: "104046160"
---
# <a name="controlling-object-access-in-active-directory-domain-services"></a><span data-ttu-id="860e9-104">Controllo dell'accesso agli oggetti in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="860e9-104">Controlling object access in Active Directory Domain Services</span></span>

<span data-ttu-id="860e9-105">Ogni oggetto del servizio di Active Directory directory è protetto dalla sicurezza di Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="860e9-105">Each Active Directory directory service object is protected by Windows 2000 security.</span></span> <span data-ttu-id="860e9-106">Questa protezione consente di controllare le operazioni eseguibili da ogni entità di sicurezza nella directory.</span><span class="sxs-lookup"><span data-stu-id="860e9-106">This security protection controls the operations that each security principal can perform in the directory.</span></span> <span data-ttu-id="860e9-107">Nelle sezioni seguenti viene descritto in che modo un'applicazione abilitata per la directory può utilizzare le funzionalità di controllo di accesso in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="860e9-107">The following sections describe how a directory-enabled application can use the access control features in Active Directory.</span></span>

-   [<span data-ttu-id="860e9-108">Funzionamento del controllo di accesso in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="860e9-108">How Access Control Works in Active Directory Domain Services</span></span>](how-access-control-works-in-active-directory-domain-services.md)
-   [<span data-ttu-id="860e9-109">Impatto del controllo di accesso sulle operazioni di lettura, operazione di scrittura, creazione ed eliminazione di oggetti.</span><span class="sxs-lookup"><span data-stu-id="860e9-109">How access control affects read operations, write operation, object creation and deletion.</span></span>](how-security-affects-operations-in-active-directory-domain-services.md)
-   [<span data-ttu-id="860e9-110">Uso delle interfacce IADs e IDirectoryObject per lavorare con il descrittore di sicurezza di un oggetto</span><span class="sxs-lookup"><span data-stu-id="860e9-110">Using the IADs and IDirectoryObject interfaces to work with an object's security descriptor</span></span>](apis-for-working-with-security-descriptors.md)
-   [<span data-ttu-id="860e9-111">Modifica delle autorizzazioni di accesso per un oggetto</span><span class="sxs-lookup"><span data-stu-id="860e9-111">Modifying the access permissions on an object</span></span>](setting-access-rights-on-an-object.md)
-   [<span data-ttu-id="860e9-112">Come vengono impostati i descrittori di sicurezza per i nuovi oggetti directory</span><span class="sxs-lookup"><span data-stu-id="860e9-112">How security descriptors are set on new directory objects</span></span>](how-security-descriptors-are-set-on-new-directory-objects.md)
-   [<span data-ttu-id="860e9-113">Creazione di un descrittore di sicurezza per un nuovo oggetto directory</span><span class="sxs-lookup"><span data-stu-id="860e9-113">Creating a Security Descriptor for a New Directory Object</span></span>](creating-a-security-descriptor-for-a-new-directory-object.md)
-   [<span data-ttu-id="860e9-114">Utilizzo dell'ereditarietà delle autorizzazioni di accesso per consentire l'accesso amministrativo a un intero sottoalbero della directory</span><span class="sxs-lookup"><span data-stu-id="860e9-114">Using inheritance of access permissions to enable administrative access to an entire subtree of the directory</span></span>](inheritance-and-delegation-of-administration.md)
-   [<span data-ttu-id="860e9-115">Creazione, modifica e lettura del descrittore di sicurezza predefinito per una classe di oggetti</span><span class="sxs-lookup"><span data-stu-id="860e9-115">Creating, modifying, and reading the default security descriptor for an object class</span></span>](default-security-descriptor.md)
-   [<span data-ttu-id="860e9-116">Creazione, impostazione e controllo dei diritti di accesso di controllo per le operazioni che vanno oltre quelle incluse nei diritti predefiniti</span><span class="sxs-lookup"><span data-stu-id="860e9-116">Creating, setting, and checking control access rights for operations that go beyond those covered by the predefined rights</span></span>](control-access-rights.md)
-   [<span data-ttu-id="860e9-117">Uso di DsAddSidHistory</span><span class="sxs-lookup"><span data-stu-id="860e9-117">Using DsAddSidHistory</span></span>](using-dsaddsidhistory.md)
-   [<span data-ttu-id="860e9-118">Controllo della visibilità degli oggetti</span><span class="sxs-lookup"><span data-stu-id="860e9-118">Controlling Object Visibility</span></span>](controlling-object-visibility.md)
-   [<span data-ttu-id="860e9-119">DACL null e DACL vuoti</span><span class="sxs-lookup"><span data-stu-id="860e9-119">Null DACLs and Empty DACLs</span></span>](null-dacls-and-empty-dacls.md)

 

 




