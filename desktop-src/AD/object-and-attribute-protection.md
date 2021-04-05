---
title: Protezione di oggetti e attributi
description: Un elenco di controllo di accesso (ACL) protegge tutti gli oggetti in Active Directory Domain Services.
ms.assetid: 64ac1f88-57d6-4821-bd17-f7ef1004922c
ms.tgt_platform: multiple
keywords:
- Protezione di oggetti e attributi
- protezione di Active Directory, oggetti e attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c046df35740f21f8706120ee6e11cfad1d4f626
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707594"
---
# <a name="object-and-attribute-protection"></a><span data-ttu-id="8d67d-105">Protezione di oggetti e attributi</span><span class="sxs-lookup"><span data-stu-id="8d67d-105">Object and Attribute Protection</span></span>

<span data-ttu-id="8d67d-106">Un elenco di controllo di accesso (ACL) protegge tutti gli oggetti in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="8d67d-106">An access-control list (ACL) protects all objects in Active Directory Domain Services.</span></span> <span data-ttu-id="8d67d-107">Gli ACL determinano gli utenti che possono visualizzare l'oggetto, gli attributi che possono leggere e le azioni che ogni utente può eseguire sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8d67d-107">ACLs determine who can view the object, what attributes they can read, and what actions each user can perform on the object.</span></span> <span data-ttu-id="8d67d-108">L'esistenza di un oggetto o di un attributo non viene mai rivelata a un utente non autorizzato.</span><span class="sxs-lookup"><span data-stu-id="8d67d-108">The existence of an object or an attribute is never revealed to an unauthorized user.</span></span>

<span data-ttu-id="8d67d-109">Un ACL è un elenco di voci di controllo di accesso (ACE) archiviate con l'oggetto protetto.</span><span class="sxs-lookup"><span data-stu-id="8d67d-109">An ACL is a list of access-control entries (ACEs) stored with the object that it protects.</span></span> <span data-ttu-id="8d67d-110">In Windows NT e Windows 2000, un ACL viene archiviato come valore binario, denominato descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="8d67d-110">In Windows NT and Windows 2000, an ACL is stored as a binary value, called a security descriptor.</span></span> <span data-ttu-id="8d67d-111">Ogni voce ACE contiene un ID di sicurezza (SID) che identifica l'entità (utente o gruppo) a cui si applica la voce ACE e i dati sul tipo di accesso concesso o negato dall'ACE.</span><span class="sxs-lookup"><span data-stu-id="8d67d-111">Each ACE contains a security identifier (SID), which identifies the principal (user or group) to whom the ACE applies, and data about what type of access the ACE grants or denies.</span></span>

<span data-ttu-id="8d67d-112">Gli ACL per gli oggetti directory contengono ACE applicabili all'oggetto nel suo complesso e le voci ACE applicabili ai singoli attributi dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8d67d-112">ACLs for directory objects contain ACEs that apply to the object as a whole and ACEs that apply to the individual attributes of the object.</span></span> <span data-ttu-id="8d67d-113">Questo consente a un amministratore di controllare non solo quali utenti possono visualizzare un oggetto, ma anche le proprietà che possono essere visualizzate dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="8d67d-113">This allows an administrator to control not only which users can see an object, but also what properties those users can view.</span></span> <span data-ttu-id="8d67d-114">Ad esempio, a tutti gli utenti potrebbe essere concesso l'accesso in lettura agli attributi di posta elettronica e numero di telefono per tutti gli altri utenti, ma le proprietà di sicurezza degli utenti potrebbero essere negate a tutti i membri di un gruppo di amministratori della sicurezza speciale.</span><span class="sxs-lookup"><span data-stu-id="8d67d-114">For example, all users might be granted read access to the email and telephone number attributes for all other users, but security properties of users might be denied to all but members of a special security administrators group.</span></span> <span data-ttu-id="8d67d-115">Ai singoli utenti potrebbe essere concesso l'accesso in scrittura agli attributi personali, ad esempio il telefono e gli indirizzi di posta elettronica, sui rispettivi oggetti utente.</span><span class="sxs-lookup"><span data-stu-id="8d67d-115">Individual users might be granted write access to personal attributes such as the telephone and mailing addresses on their own user objects.</span></span>

 

 




