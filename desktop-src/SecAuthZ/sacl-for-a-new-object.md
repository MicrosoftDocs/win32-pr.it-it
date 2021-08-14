---
description: SACL per un nuovo oggetto
ms.assetid: 1d0d6fee-e5ec-4d8f-8ed8-10c725c57a6a
title: SACL per un nuovo oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f9833fcfb45a612b6135579e44aca6f219661fd2aeb2998b899e5794fa7bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413841"
---
# <a name="sacl-for-a-new-object"></a>SACL per un nuovo oggetto

Il sistema usa l'algoritmo seguente per compilare un elenco di controllo di accesso condiviso per la maggior parte dei tipi di nuovi oggetti a protezione diretta:

1.  L'elenco SACL dell'oggetto è l'elenco SACL del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) specificato dall'autore dell'oggetto. Il sistema unisce tutte le ACE ereditabili nell'elenco SACL specificato, a meno che il bit edizione Standard SACL PROTECTED non sia impostato nei bit di controllo del \_ \_ descrittore di sicurezza. Le ACE SYSTEM RESOURCE ATTRIBUTE e GLI ACE CON ID CRITERI CON AMBITO SISTEMA da un oggetto padre verranno uniti a un nuovo oggetto anche se è impostato \_ \_ il bit EDIZIONE STANDARD \_ \_ \_ \_ \_ \_ SACL \_ PROTECTED.
2.  Se l'autore non specifica un descrittore di sicurezza, il sistema compila l'elenco SACL dell'oggetto da ACE ereditabili.
3.  Se non è presente alcun SACL specificato o ereditato, l'oggetto non dispone di alcun SACL.

Per specificare un SACL per un nuovo oggetto, l'autore dell'oggetto deve avere il edizione Standard \_ SECURITY \_ NAME abilitato. [](privileges.md) Se l'elenco SACL specificato per un nuovo oggetto contiene solo ACE SYSTEM RESOURCE ATTRIBUTE, il edizione Standard \_ SECURITY NAME non è \_ \_ \_ \_ necessario. L'autore non ha bisogno di questo privilegio se l'elenco SACL dell'oggetto viene compilato da ACE ereditate.

Il sistema usa un algoritmo diverso per compilare un sacl per un nuovo oggetto Active Directory. Per altre informazioni, vedere [How Security Descriptors are Set on New Directory Objects](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).

 

 
