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
# <a name="delegation"></a>Delegation

La *delega* è una delle più importanti funzionalità di sicurezza di Active Directory Domain Services. La delega consente a un'autorità amministrativa più elevata di concedere diritti amministrativi specifici per contenitori e sottoalberi a singoli utenti e gruppi. Gli amministratori di dominio, con un'ampia autorità su grandi segmenti di utenti, non sono più necessari.

Una voce ACE può concedere diritti amministrativi specifici per gli oggetti di un contenitore a un utente o a un gruppo. I diritti vengono concessi per operazioni specifiche su classi di oggetti specifiche usando le voci ACE nell'ACL del contenitore. Ad esempio, per consentire a un utente denominato "utente 1" di essere un amministratore dell'unità organizzativa "contabilità aziendale", aggiungere ACE all'ACL in "contabilità aziendale" come indicato di seguito:

"" utente 1 "; Grant Crea, modifica, Elimina; utente classe oggetto "utente 1"; Grant Creare, modificare, eliminare; gruppo di classi di oggetti "User 1"; Grant Write; utente classe di oggetti; Password dell'attributo "

A questo punto, l'utente 1 può creare nuovi utenti e gruppi nell'accounting aziendale e impostare le password per gli utenti esistenti, ma l'utente 1 non può creare altre classi di oggetti e non può influire sugli utenti in altri contenitori, a meno che, ovviamente, all'utente 1 venga concesso l'accesso tramite ACE negli altri contenitori.

 

 




