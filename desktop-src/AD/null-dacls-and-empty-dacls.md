---
title: DACL null e DACL vuoti (AD DS)
description: La presenza di un elenco di controllo di accesso discrezionale (DACL) null nell'attributo nTSecurityDescriptor di qualsiasi oggetto può creare un grave rischio per la sicurezza.
ms.assetid: 32b786d2-e676-4402-ad22-550de9289494
ms.tgt_platform: multiple
keywords:
- Elenchi DACL null e DACL vuoti AD
- Elenchi DACL AD, null e vuoti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b841bb0253547fea291232fb4c9e6e0f3377d18
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956310"
---
# <a name="null-dacls-and-empty-dacls-ad-ds"></a>DACL null e DACL vuoti (AD DS)

La presenza di un elenco di controllo di accesso discrezionale (DACL) null nell'attributo [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) di qualsiasi oggetto può creare un grave rischio per la sicurezza. Un DACL null concede l'accesso completo a tutti gli utenti che lo richiedono; il normale controllo di sicurezza non viene eseguito rispetto all'oggetto. Un DACL null non deve essere confuso con un DACL vuoto. Un DACL vuoto è un DACL correttamente allocato e inizializzato che non contiene voci di controllo di accesso (ACE). Un DACL vuoto non concede l'accesso all'oggetto a cui è assegnato.

Per ulteriori informazioni, vedere [DACL null e DACL vuoti](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).

 

 