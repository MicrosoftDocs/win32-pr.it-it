---
description: DACL per un nuovo oggetto
ms.assetid: ff1146d7-5229-4c75-9768-28c3fab5fcea
title: DACL per un nuovo oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01d1ec8e92d4d56f977d4454b9a67df0a9bd489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130250"
---
# <a name="dacl-for-a-new-object"></a>DACL per un nuovo oggetto

Il sistema utilizza l'algoritmo seguente per compilare un DACL per la maggior parte dei tipi di nuovi oggetti a protezione diretta:

1.  Il DACL dell'oggetto è l'elenco DACL del [*descrittore di sicurezza*](/windows/desktop/SecGloss/s-gly) specificato dal creatore dell'oggetto. Il sistema unisce eventuali ACE ereditabili nell'elenco DACL specificato, a meno che non \_ \_ sia impostato il bit protetto con DACL se nei bit del controllo del descrittore di sicurezza.
2.  Se il creatore non specifica un descrittore di sicurezza, il sistema compila l'elenco DACL dell'oggetto da voci ACE ereditabili.
3.  Se non è specificato alcun descrittore di sicurezza e non sono presenti ACE ereditabili, il DACL dell'oggetto è l'elenco DACL predefinito del token [*primario*](/windows/desktop/SecGloss/p-gly) o di [*rappresentazione*](/windows/desktop/SecGloss/i-gly) del creatore.
4.  Se non è presente alcun DACL specificato, ereditato o predefinito, il sistema crea l'oggetto senza DACL, che consente a tutti gli utenti di accedere completamente all'oggetto.

Il sistema utilizza un algoritmo diverso per compilare un DACL per un nuovo oggetto Active Directory. Per ulteriori informazioni, vedere [la pagina relativa alla modalità di impostazione dei descrittori di sicurezza per i nuovi oggetti directory](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).

 

 
