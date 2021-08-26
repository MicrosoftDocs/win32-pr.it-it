---
description: Le risorse necessarie per la personalizzazione di un'applicazione, ad esempio i modelli aziendali, possono essere distribuite con l'applicazione includendo una trasformazione con il pacchetto di installazione dell'applicazione.
ms.assetid: 3d9328d0-4d95-449c-bf2b-5487f7ba5971
title: Uso delle trasformazioni per aggiungere risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2999371079ac57d0e44800c9374d496db6eb400864fed3422d88f2b03731724
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038991"
---
# <a name="using-transforms-to-add-resources"></a>Uso delle trasformazioni per aggiungere risorse

Le risorse necessarie per la personalizzazione di un'applicazione, ad esempio i modelli aziendali, possono essere distribuite con l'applicazione includendo una trasformazione con il pacchetto di installazione dell'applicazione. Quando si distribuiscono risorse, ad esempio file, chiavi del Registro di sistema o collegamenti, è necessario seguire le regole seguenti usando una trasformazione.

-   La trasformazione deve aggiungere uno o più nuovi componenti al database di installazione per contenere le risorse aggiuntive. La trasformazione non deve aggiungere risorse a un componente già esistente nell'installazione.
-   La trasformazione deve aggiungere una o più nuove funzionalità al database di installazione per contenere questi nuovi componenti. Queste nuove funzionalità non devono essere padre di alcuna funzionalità esistente, ma possono essere introdotte insieme. Alle nuove funzionalità devono essere dati nomi univoci in tutte le altre trasformazioni per questo prodotto. Nessuna trasformazione deve mai aggiungere una funzionalità a questo prodotto con lo stesso nome elencato nella colonna Funzionalità della tabella [Funzionalità](feature-table.md) e contenente componenti o risorse diversi.

 

 



