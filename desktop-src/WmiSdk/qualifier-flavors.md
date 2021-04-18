---
description: Le versioni dei qualificatori forniscono ulteriori informazioni su un qualificatore, ad esempio se una classe o un'istanza derivata può eseguire l'override del valore originale del qualificatore.
ms.assetid: 6a0769ac-e16c-45e1-92b6-26e4969bf23d
ms.tgt_platform: multiple
title: Versioni qualificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8ddf6c2daea59931e533174c532e3d07b147a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318547"
---
# <a name="qualifier-flavors"></a>Versioni qualificatore

Le versioni dei qualificatori forniscono ulteriori informazioni su un qualificatore, ad esempio se una classe o un'istanza derivata può eseguire l'override del valore originale del qualificatore.

Le versioni dei qualificatori possono essere aggiunte all'inizio del file MOF, usando la sintassi seguente, in modo che vengano applicate in tutta la definizione. Ad esempio:

``` syntax
Qualifier Description : ToSubClass Amended;
```

Le versioni **ToClass** e **emendate** si applicano a tutti i qualificatori della **Descrizione** nel file MOF.

Nella tabella seguente sono elencate le versioni del qualificatore.



| Versione qualificatore    | Significato                                                                                                                                                                                                                                         |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Corretto**         | Il qualificatore non è necessario nella definizione della classe di base e può essere spostato nella modifica da localizzare.                                                                                                                                  |
| **DisableOverride** | Il qualificatore non può essere sottoposto a override in una classe o in un'istanza derivata. Si noti che la possibilità di eseguire l'override di un qualificatore propagato è il valore predefinito.                                                                                                      |
| **EnableOverride**  | Quando viene propagata a una classe o a un'istanza derivata, il valore del qualificatore può essere sottoposto a override. L'impostazione di **EnableOverride** è facoltativa perché la possibilità di eseguire l'override del valore del qualificatore è la funzionalità predefinita per i qualificatori propagati. |
| **NotToInstance**   | Il qualificatore non viene propagato alle istanze della classe.                                                                                                                                                                                             |
| **NotToSubClass**   | Il qualificatore non viene propagato alle classi derivate.                                                                                                                                                                                             |
| **Con restrizioni**      | Il qualificatore non viene propagato a istanze o classi derivate.                                                                                                                                                                                |
| **Istanza di**      | Il qualificatore viene propagato alle istanze.                                                                                                                                                                                                       |
| **ToClass**      | Il qualificatore viene propagato alle classi derivate. Questa caratteristica è appropriata solo per i qualificatori definiti per una classe e non può essere associata a un qualificatore che descrive un'istanza di classe.                                                           |



 

 

 



