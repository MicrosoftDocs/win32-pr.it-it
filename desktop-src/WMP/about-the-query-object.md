---
title: Informazioni sull'oggetto query
description: Informazioni sull'oggetto query
ms.assetid: 41488036-bdcf-4fe6-8f7e-f0897157d3d9
keywords:
- Windows Media Player, oggetto query
- Modello a oggetti di Windows Media Player, oggetto query
- modello a oggetti, oggetto query
- Controllo ActiveX Windows Media Player, oggetto query
- Controllo ActiveX, oggetto query
- Controllo ActiveX Windows Media Player Mobile, oggetto query
- Windows Media Player Mobile, oggetto query
- Oggetto query
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a26f60c38e053b91c7e56f5cbd7ccaf2ba0fe2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710792"
---
# <a name="about-the-query-object"></a>Informazioni sull'oggetto query

L'oggetto **query** rappresenta una query composta. Si crea un nuovo oggetto **query** vuoto chiamando *mediacollection*. **CreateQuery**. Dopo aver creato un oggetto **query** , è possibile chiamare **addCondition** per aggiungere una condizione alla query composta. Ogni chiamata successiva a **addCondition** aggiunge una nuova condizione alla query esistente usando la logica and.

Si supponga, ad esempio, di voler creare una query che rappresenti tutti i supporti digitali in cui **WM/genre** è uguale a "Jazz" e l' **autore** contiene "Jim". È possibile creare una query composta per rappresentare queste condizioni usando il codice JScript seguente:


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");
```



Per aggiungere una condizione a una query composta usando la logica o, è necessario chiamare **query. beginNextGroup**. Questo metodo segnala che il gruppo di condizioni precedente è stato completato e che la chiamata successiva a **addCondition** rappresenta l'inizio di un nuovo gruppo di condizioni.

Ad esempio, per creare una query che rappresenti tutti i supporti digitali in cui **WM/genre** è uguale a "Jazz" e l' **autore** contiene "Jim" o l' **autore** contiene "Dave", è possibile usare il codice di esempio seguente:


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");

// Start the next condition group. This group will be
// combined with the previous group using a logical OR operation.
Query.beginNextGroup();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Dave");
```



Per eseguire la query composta, chiamare **mediacollection. getPlaylistByQuery**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Mediacollection. getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**Modello a oggetti del lettore per i linguaggi di scripting**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Oggetto query**](query-object.md)
</dt> </dl>

 

 




