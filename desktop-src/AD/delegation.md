---
title: Delegation
description: La delega è una delle più importanti funzionalità di sicurezza di Active Directory Domain Services.
ms.assetid: ab8740c9-f5a2-40cc-abce-0ef80c3fca7a
ms.tgt_platform: multiple
keywords:
- Delega AD
- sicurezza AD, delega
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26be1f9350c664d289832874994e2b3ba2e696c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955155"
---
# <a name="delegation"></a><span data-ttu-id="a2fc8-105">Delegation</span><span class="sxs-lookup"><span data-stu-id="a2fc8-105">Delegation</span></span>

<span data-ttu-id="a2fc8-106">La *delega* è una delle più importanti funzionalità di sicurezza di Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="a2fc8-106">*Delegation* is one of the most important security features of Active Directory Domain Services.</span></span> <span data-ttu-id="a2fc8-107">La delega consente a un'autorità amministrativa più elevata di concedere diritti amministrativi specifici per contenitori e sottoalberi a singoli utenti e gruppi.</span><span class="sxs-lookup"><span data-stu-id="a2fc8-107">Delegation enables a higher administrative authority to grant specific administrative rights for containers and subtrees to individuals and groups.</span></span> <span data-ttu-id="a2fc8-108">Gli amministratori di dominio, con un'ampia autorità su grandi segmenti di utenti, non sono più necessari.</span><span class="sxs-lookup"><span data-stu-id="a2fc8-108">Domain administrators, with broad authority over large segments of users, are no longer required.</span></span>

<span data-ttu-id="a2fc8-109">Una voce ACE può concedere diritti amministrativi specifici per gli oggetti di un contenitore a un utente o a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="a2fc8-109">An ACE can grant specific administrative rights for the objects in a container to a user or group.</span></span> <span data-ttu-id="a2fc8-110">I diritti vengono concessi per operazioni specifiche su classi di oggetti specifiche usando le voci ACE nell'ACL del contenitore.</span><span class="sxs-lookup"><span data-stu-id="a2fc8-110">Rights are granted for specific operations on specific object classes using ACEs in the container's ACL.</span></span> <span data-ttu-id="a2fc8-111">Ad esempio, per consentire a un utente denominato "utente 1" di essere un amministratore dell'unità organizzativa "contabilità aziendale", aggiungere ACE all'ACL in "contabilità aziendale" come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="a2fc8-111">For example, to enable a user named "user 1" to be an administrator of the "Corporate Accounting" organizational unit, add ACEs to the ACL on "Corporate Accounting" as follows:</span></span>

<span data-ttu-id="a2fc8-112">"" utente 1 "; Grant Crea, modifica, Elimina; utente classe oggetto "utente 1"; Grant Creare, modificare, eliminare; gruppo di classi di oggetti "User 1"; Grant Write; utente classe di oggetti; Password dell'attributo "</span><span class="sxs-lookup"><span data-stu-id="a2fc8-112">""user 1";Grant ;Create, Modify, Delete;Object-Class User"user 1";Grant ;Create, Modify, Delete;Object-Class Group"user 1";Grant ;Write;Object-Class User; Attribute Password"</span></span>

<span data-ttu-id="a2fc8-113">A questo punto, l'utente 1 può creare nuovi utenti e gruppi nell'accounting aziendale e impostare le password per gli utenti esistenti, ma l'utente 1 non può creare altre classi di oggetti e non può influire sugli utenti in altri contenitori, a meno che, ovviamente, all'utente 1 venga concesso l'accesso tramite ACE negli altri contenitori.</span><span class="sxs-lookup"><span data-stu-id="a2fc8-113">Now, user 1 can create new users and groups in Corporate Accounting and set the passwords on existing users, but user 1 cannot create any other object classes and cannot affect users in any other containers, unless, of course, user 1 is granted that access by ACEs on the other containers.</span></span>

 

 




