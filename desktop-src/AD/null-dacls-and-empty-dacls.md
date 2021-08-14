---
title: DACL Null e DACL vuoti (AD DS)
description: La presenza di un elenco di controllo di accesso discrezionale null nell'attributo nTSecurityDescriptor di qualsiasi oggetto può creare un grave rischio per la sicurezza.
ms.assetid: 32b786d2-e676-4402-ad22-550de9289494
ms.tgt_platform: multiple
keywords:
- DACL Null e DACL vuoti AD
- DACL AD, Null e Vuoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a41e03917c1190b7926eca11db038e2143bcb91d142e0617d143d4d80bb6e601
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185796"
---
# <a name="null-dacls-and-empty-dacls-ad-ds"></a>DACL Null e DACL vuoti (AD DS)

La presenza di un elenco di controllo di accesso discrezionale null nell'attributo [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) di qualsiasi oggetto può creare un grave rischio per la sicurezza. Un DACL Null concede l'accesso completo a qualsiasi utente che lo richiede. Il normale controllo di sicurezza non viene eseguito rispetto all'oggetto . Un DACL Null non deve essere confuso con un DACL vuoto. Un elenco DACL vuoto è un DACL allocato e inizializzato correttamente che non contiene voci di controllo di accesso (ACE). Un elenco DACL vuoto non concede alcun accesso all'oggetto a cui è assegnato.

Per altre informazioni, vedere [DACL Null e DACL vuoti.](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls)

 

 