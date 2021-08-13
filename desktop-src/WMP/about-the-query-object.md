---
title: Informazioni sull'oggetto Query
description: Informazioni sull'oggetto Query
ms.assetid: 41488036-bdcf-4fe6-8f7e-f0897157d3d9
keywords:
- Windows Media Player,Oggetto Query
- Windows Media Player a oggetti, oggetto Query
- modello a oggetti,oggetto Query
- Windows Media Player ActiveX, oggetto Query
- ActiveX, oggetto Query
- Windows Media Player Controllo ActiveX mobile, oggetto Query
- Windows Media Player Mobile, oggetto Query
- Oggetto query
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d649263f981d02e106466c6e0fcada99c316054d4bf6e0acc0faca641c75dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470401"
---
# <a name="about-the-query-object"></a>Informazioni sull'oggetto Query

**L'oggetto Query** rappresenta una query composta. Per creare un nuovo oggetto **Query** vuoto, chiamare *mediaCollection*. **createQuery**. Dopo aver creato un **oggetto Query,** è possibile chiamare **addCondition** per aggiungere una condizione alla query composta. Ogni chiamata successiva a **addCondition** aggiunge una nuova condizione alla query esistente usando la logica AND.

Si supponga, ad esempio, di voler creare una query che rappresenta tutti i supporti digitali in cui **WM/Genre** è uguale a "Jazz" e **Author** contiene "Jim". È possibile creare una query composta per rappresentare queste condizioni usando il codice JScript seguente:


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");
```



Per aggiungere una condizione a una query composta usando la logica OR, è necessario chiamare **Query.beginNextGroup**. Questo metodo segnala che il gruppo di condizioni precedente è stato completato e che la chiamata successiva a **addCondition** rappresenta l'inizio di un nuovo gruppo di condizioni.

Ad esempio, per creare una query che rappresenta tutti i supporti digitali in cui **WM/Genre** è uguale a "Jazz" e **Author** contiene "Jim" o **Author** contiene "Dave", è possibile usare il codice di esempio seguente:


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



Per eseguire la query composta, chiamare **MediaCollection.getPlaylistByQuery**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**MediaCollection.getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**Modello a oggetti lettore per linguaggi di scripting**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Oggetto Query**](query-object.md)
</dt> </dl>

 

 




