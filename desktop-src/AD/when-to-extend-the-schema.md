---
title: Quando estendere lo schema
description: Estendere lo schema solo se nessuna classe di oggetti esistente soddisfa i requisiti dell'applicazione. L'estensione dello schema è un'operazione complessa. Le modifiche dello schema vengono replicate in ogni controller di dominio nella foresta aziendale. Prendere in considerazione questo problema con attenzione.
ms.assetid: 92231f31-d2af-4c3b-981e-e55cc478899d
ms.tgt_platform: multiple
keywords:
- Quando estendere lo schema AD
- schema AD, quando estendere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042665069b06804dd648798debca6e0cee5628e115f5f512718ea0a51cc765ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024329"
---
# <a name="when-to-extend-the-schema"></a>Quando estendere lo schema

Estendere lo schema solo se nessuna classe di oggetti esistente soddisfa i requisiti dell'applicazione. L'estensione dello schema è un'operazione complessa. Le modifiche dello schema vengono replicate in ogni controller di dominio nella foresta aziendale. Prendere in considerazione questo problema con attenzione.

Lo schema può essere esteso in tre modi:

-   Derivare una nuova sottoclasse da una classe esistente. La sottoclasse include tutti gli attributi della superclasse e gli attributi specificati. Derivare da una classe esistente:
    -   Quando la classe esistente richiede attributi aggiuntivi, ma in caso contrario è accettabile.
    -   Quando non è necessaria la possibilità di trasformare gli oggetti esistenti della classe in una nuova classe. Non è possibile aggiungere una sottoclasse a un oggetto esistente.
    -   Per utilizzare lo snap-in Directory Manager esistente per gestire gli attributi estesi degli oggetti.
-   Aggiungere attributi a una classe esistente e/o aggiungere oggetti padre per la classe. Quando si aggiungono più attributi, eseguire questa operazione in modo strutturato definendo una classe ausiliaria e aggiungendo tale classe ausiliaria alla classe esistente.
-   La modifica di una classe esistente è necessaria quando un'applicazione richiede la possibilità di estendere gli oggetti esistenti della classe. Ad esempio, per aggiungere dati specifici dell'applicazione all'oggetto User, estendere normalmente la classe User, perché è necessario gestire gli utenti esistenti e non solo gli utenti speciali creati dall'applicazione.
-   Creare una nuova classe con gli attributi necessari. Creare una nuova classe. una classe derivata da "Top" quando nessuna classe esistente soddisfa i requisiti operativi.

Quando si sottoclassa una classe esistente, tutti gli elementi dell'interfaccia utente associati alla classe originale non verranno ereditati dalla sottoclasse. Ad esempio, se si sottoclassa un oggetto utente, le pagine delle proprietà e le voci di menu associate all'utente non vengono ereditate. Per questo motivo, è preferibile estendere un oggetto esistente o creare una classe ausiliaria anziché creare una sottoclasse.

Se si sottoclassa una classe esistente o si modifica una classe esistente, è necessario estendere strumenti come lo snap-in Utenti e computer di Active Directory per gestire gli attributi estesi degli oggetti. Per altre informazioni, vedere [Extending the Interfaccia utente for Directory Objects](extending-the-user-interface-for-directory-objects.md).

 

 




