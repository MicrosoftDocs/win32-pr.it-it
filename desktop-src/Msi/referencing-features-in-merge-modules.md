---
description: I moduli unione funzionano solo con i componenti e non con le funzionalità. Tuttavia, alcune tabelle nei moduli unione, ad esempio la tabella PublishComponent, contengono campi che fanno riferimento alle funzionalità.
ms.assetid: f2891457-efef-4319-bd09-5de7fcf32d21
title: Riferimento alle funzionalità nei moduli unione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2857b71fd651955319457092d9cf689ded954af758e7906b44a761dfa6ad782
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375951"
---
# <a name="referencing-features-in-merge-modules"></a>Riferimento alle funzionalità nei moduli unione

I moduli unione funzionano solo con i componenti e non con le funzionalità. Tuttavia, alcune tabelle nei moduli unione, ad esempio la [tabella PublishComponent](publishcomponent-table.md), contengono campi che fanno riferimento alle funzionalità.

GUID null: deve essere creato in qualsiasi campo di un database del {00000000-0000-0000-0000-000000000000} modulo unione che fa riferimento a una funzionalità. Quando il modulo unione viene unito in un pacchetto di installazione, lo strumento di merge sostituisce il GUID Null con la funzionalità specificata nel pacchetto di installazione, ad eccezione delle tabelle che richiedono una gestione speciale, ad esempio la tabella [ModuleSignature](modulesignature-table.md) e le tabelle ModuleSequence.

Si noti che se come chiave primaria viene usato un GUID Null, non è garantito che il valore sostituito dallo strumento di unione sia univoco. Gli autori di moduli unione sono responsabili di garantire che nessuna chiave primaria esistente nell'interfaccia utente sia duplicata quando lo strumento di unione sostituisce i GUID null con funzionalità.

 

 



