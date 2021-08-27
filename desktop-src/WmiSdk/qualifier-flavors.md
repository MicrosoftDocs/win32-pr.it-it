---
description: I qualificatori forniscono altre informazioni su un qualificatore, ad esempio se una classe o un'istanza derivata può eseguire l'override del valore originale dei qualificatori.
ms.assetid: 6a0769ac-e16c-45e1-92b6-26e4969bf23d
ms.tgt_platform: multiple
title: Qualificatori Flavors
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a48c5ed3c7b695b19c182bcf05a9ce55b31b0bb94081570c58c8d55f7e48994c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050479"
---
# <a name="qualifier-flavors"></a>Qualificatori Flavors

Le versioni del qualificatore forniscono altre informazioni su un qualificatore, ad esempio se una classe o un'istanza derivata può eseguire l'override del valore originale del qualificatore.

I qualificatori possono essere aggiunti all'inizio del file MOF usando la sintassi seguente, causando l'applicazione in tutta la definizione. Esempio:

``` syntax
Qualifier Description : ToSubClass Amended;
```

Le **descrizioni ToSubClass** **e Amended** si applicano a tutti i qualificatori **Description** nel file MOF.

Nella tabella seguente sono elencate le opzioni del qualificatore.



| Flavor del qualificatore    | Significato                                                                                                                                                                                                                                         |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Modificato**         | Il qualificatore non è necessario nella definizione della classe di base e può essere spostato nella modifica da localizzare.                                                                                                                                  |
| **DisableOverride** | Il qualificatore non può essere sottoposto a override in una classe o in un'istanza derivata. Si noti che la possibilità di eseguire l'override di un qualificatore propagato è il valore predefinito.                                                                                                      |
| **EnableOverride**  | Quando viene propagato a una classe o a un'istanza derivata, è possibile eseguire l'override del valore del qualificatore. **L'impostazione di EnableOverride** è facoltativa perché la possibilità di eseguire l'override del valore del qualificatore è la funzionalità predefinita per i qualificatori propagati. |
| **NotToInstance**   | Il qualificatore non viene propagato alle istanze della classe.                                                                                                                                                                                             |
| **NotToSubClass**   | Il qualificatore non viene propagato alle classi derivate.                                                                                                                                                                                             |
| **Con restrizioni**      | Il qualificatore non viene propagato a istanze o classi derivate.                                                                                                                                                                                |
| **ToInstance**      | Il qualificatore viene propagato alle istanze.                                                                                                                                                                                                       |
| **ToSubClass**      | Il qualificatore viene propagato alle classi derivate. Questa versione è appropriata solo per i qualificatori definiti per una classe e non può essere associata a un qualificatore che descrive un'istanza della classe.                                                           |



 

 

 



