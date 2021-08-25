---
description: Un DACL Null concede l'accesso completo a qualsiasi utente che lo richiede. Un DACL vuoto è un DACL allocato e inizializzato correttamente che non contiene voci di controllo di accesso. Un DACL vuoto non concede alcun accesso all'oggetto a cui è assegnato.
ms.assetid: 26e5c98d-bbdc-4f9f-96e0-18d1c429f1e6
title: DACL Null e DACL vuoti (autorizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c15f9a3aeed120ff91dc19a091232721c623683d90f0c9cdccbc065516eea8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907821"
---
# <a name="null-dacls-and-empty-dacls-authorization"></a>DACL Null e DACL vuoti (autorizzazione)

Se [*l'elenco*](/windows/desktop/SecGloss/d-gly) di controllo di accesso discrezionale (DACL) appartenente al descrittore di sicurezza di un oggetto è impostato su **NULL,** viene creato un DACL Null. [](/windows/desktop/SecGloss/s-gly) Un DACL Null concede l'accesso completo a qualsiasi utente che lo richiede. Il normale controllo di sicurezza non viene eseguito rispetto all'oggetto . Un DACL Null non deve essere confuso con un DACL vuoto. Un DACL vuoto è un DACL allocato e inizializzato correttamente che non contiene voci [*di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE). Un DACL vuoto non concede alcun accesso all'oggetto a cui è assegnato.

Per un esempio di come creare un dacl, vedere [Creazione di un dacl.](/windows/desktop/SecBP/creating-a-dacl)

 

 
