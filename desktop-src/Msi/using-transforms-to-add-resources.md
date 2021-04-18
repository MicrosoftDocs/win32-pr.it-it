---
description: Le risorse necessarie per la personalizzazione di un'applicazione, ad esempio i modelli aziendali, possono essere distribuite con l'applicazione includendo una trasformazione con il pacchetto di installazione dell'applicazione.
ms.assetid: 3d9328d0-4d95-449c-bf2b-5487f7ba5971
title: Uso delle trasformazioni per aggiungere risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c11fac7ad65601286fb550abd950bf5ac49af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312311"
---
# <a name="using-transforms-to-add-resources"></a>Uso delle trasformazioni per aggiungere risorse

Le risorse necessarie per la personalizzazione di un'applicazione, ad esempio i modelli aziendali, possono essere distribuite con l'applicazione includendo una trasformazione con il pacchetto di installazione dell'applicazione. Quando si distribuiscono risorse, ad esempio file, chiavi del registro di sistema o collegamenti, è necessario attenersi alle regole seguenti, usando una trasformazione.

-   La trasformazione deve aggiungere uno o più componenti nuovi al database di installazione per contenere le risorse aggiuntive. La trasformazione non deve aggiungere risorse a un componente già esistente nell'installazione.
-   La trasformazione deve aggiungere una o più nuove funzionalità al database di installazione per contenere questi nuovi componenti. Queste nuove funzionalità non devono essere gli elementi padre di tutte le funzionalità esistenti, ma le nuove funzionalità padre e figlio possono essere introdotte insieme. Alle nuove funzionalità devono essere assegnati nomi univoci in tutte le altre trasformazioni per questo prodotto. Due trasformazioni non devono mai aggiungere una funzionalità a questo prodotto con lo stesso nome elencato nella colonna feature della [tabella Feature](feature-table.md) e contenenti componenti o risorse differenti.

 

 



