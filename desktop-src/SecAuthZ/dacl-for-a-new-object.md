---
description: DACL per un nuovo oggetto
ms.assetid: ff1146d7-5229-4c75-9768-28c3fab5fcea
title: DACL per un nuovo oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cfd5b8f8c16919260c4dace5394f864fe987885a7f2203b2b41162b7c41e701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782140"
---
# <a name="dacl-for-a-new-object"></a>DACL per un nuovo oggetto

Il sistema usa l'algoritmo seguente per creare un elenco DACL per la maggior parte dei tipi di nuovi oggetti a protezione diretta:

1.  L'elenco DACL dell'oggetto è l'elenco DACL del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) specificato dall'autore dell'oggetto. Il sistema unisce tutte le voci ACE ereditabili nell'elenco DACL specificato, a meno che il bit EDIZIONE STANDARD DACL PROTECTED non sia impostato nei bit di controllo del \_ \_ descrittore di sicurezza.
2.  Se l'autore non specifica un descrittore di sicurezza, il sistema compila l'elenco DACL dell'oggetto da ACE ereditabili.
3.  Se non viene specificato alcun descrittore di sicurezza e non sono presenti ACE ereditabili, l'elenco DACL dell'oggetto è l'elenco DACL predefinito del [*token*](/windows/desktop/SecGloss/i-gly) primario o di rappresentazione dell'autore. [](/windows/desktop/SecGloss/p-gly)
4.  Se non è presente alcun DACL specificato, ereditato o predefinito, il sistema crea l'oggetto senza DACL, che consente a tutti l'accesso completo all'oggetto.

Il sistema usa un algoritmo diverso per creare un elenco DACL per un nuovo oggetto Active Directory. Per altre informazioni, vedere [How Security Descriptors are Set on New Directory Objects](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).

 

 
