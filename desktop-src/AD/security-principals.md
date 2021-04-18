---
title: Entità di sicurezza
description: In Windows 2000, un'entità di sicurezza è un utente, un gruppo o un computer \ 8212; entità riconosciuta dal sistema di sicurezza.
ms.assetid: 213ee563-35cd-43d2-abb2-f66652df5be1
ms.tgt_platform: multiple
keywords:
- Active Directory delle entità di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877ed77b365fa4a61444e4936dbe859379ee397
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297717"
---
# <a name="security-principals"></a><span data-ttu-id="5635e-104">Entità di sicurezza</span><span class="sxs-lookup"><span data-stu-id="5635e-104">Security Principals</span></span>

<span data-ttu-id="5635e-105">In Windows 2000, un'entità di sicurezza è un utente, un gruppo o un computer, un'entità riconosciuta dal sistema di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="5635e-105">In Windows 2000, a security principal is a user, group, or computer — an entity that the security system recognizes.</span></span> <span data-ttu-id="5635e-106">Sono inclusi utenti umani e processi autonomi.</span><span class="sxs-lookup"><span data-stu-id="5635e-106">This includes human users as well as autonomous processes.</span></span> <span data-ttu-id="5635e-107">In modo rigoroso, il sistema di sicurezza non è in grado di distinguere tra gli utenti connessi e i processi in esecuzione nel computer.</span><span class="sxs-lookup"><span data-stu-id="5635e-107">Strictly speaking, the security system cannot tell the difference between users who are logged in and processes running on the computer.</span></span> <span data-ttu-id="5635e-108">Viene visualizzato come entità di sicurezza con i nomi delle entità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="5635e-108">It sees both as security principals with security principal names.</span></span>

<span data-ttu-id="5635e-109">Utenti, gruppi e computer vengono creati e archiviati come oggetti in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="5635e-109">Users, groups, and computers are created and stored as objects in Active Directory Domain Services.</span></span> <span data-ttu-id="5635e-110">Sono inoltre presenti entità di sicurezza ben note che rappresentano identità speciali definite dal sistema di sicurezza di Windows 2000, ad esempio Everyone, sistema locale, entità autonoma, utente autenticato, proprietario dell'autore e così via.</span><span class="sxs-lookup"><span data-stu-id="5635e-110">There are also well-known security principals that represent special identities defined by the Windows 2000 security system, such as Everyone, Local System, Principal Self, Authenticated User, Creator Owner, and so on.</span></span> <span data-ttu-id="5635e-111">Gli oggetti che rappresentano le entità di sicurezza note, ad esempio l'accesso anonimo, vengono archiviati nel contenitore di entità di sicurezza noto sotto il contenitore di configurazione.</span><span class="sxs-lookup"><span data-stu-id="5635e-111">Objects representing the well-known security principals, such as Anonymous Logon, are stored in the WellKnown Security Principals container beneath the Configuration container.</span></span>

 

 




