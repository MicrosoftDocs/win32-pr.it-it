---
description: Un DACL null concede l'accesso completo a tutti gli utenti che lo richiedono. Un DACL vuoto è un DACL correttamente allocato e inizializzato che non contiene voci di controllo di accesso. Un DACL vuoto non concede l'accesso all'oggetto a cui è assegnato.
ms.assetid: 26e5c98d-bbdc-4f9f-96e0-18d1c429f1e6
title: DACL null e DACL vuoti (autorizzazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c06942d7b2d188a74b7e3e307cf60d6740a4251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317038"
---
# <a name="null-dacls-and-empty-dacls-authorization"></a>DACL null e DACL vuoti (autorizzazione)

Se l' [*elenco di controllo di accesso discrezionale*](/windows/desktop/SecGloss/d-gly) (DACL) che appartiene al [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) di un oggetto è impostato su **null**, viene creato un DACL null. Un DACL null concede l'accesso completo a tutti gli utenti che lo richiedono; il normale controllo di sicurezza non viene eseguito rispetto all'oggetto. Un DACL null non deve essere confuso con un DACL vuoto. Un DACL vuoto è un DACL correttamente allocato e inizializzato che non contiene [*voci di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACE). Un DACL vuoto non concede l'accesso all'oggetto a cui è assegnato.

Per un esempio di come creare un DACL, vedere [creazione di un DACL](/windows/desktop/SecBP/creating-a-dacl).

 

 
