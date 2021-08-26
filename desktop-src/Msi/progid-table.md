---
description: La tabella ProgId contiene informazioni per gli ID programma e gli ID programma indipendenti dalla versione che devono essere generati come parte dell'annuncio del prodotto.
ms.assetid: 66a7e170-6f70-4db7-98f4-8a074471b9f2
title: Tabella ProgId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbed8baea9bd8421757cf2e31f0ba06679db3394c95f732537a7e230c02b5ee8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042061"
---
# <a name="progid-table"></a>Tabella ProgId

La tabella ProgId contiene informazioni per gli ID programma e gli ID programma indipendenti dalla versione che devono essere generati come parte dell'annuncio del prodotto.

La tabella ProgId contiene le colonne seguenti.



| Colonna         | Tipo                         | Chiave | Nullable |
|----------------|------------------------------|-----|----------|
| ProgId         | [Text](text.md)             | S   | N        |
| ProgId \_ Padre | [Text](text.md)             | N   | S        |
| Classe\_        | [GUID](guid.md)             | N   | S        |
| Descrizione    | [Text](text.md)             | N   | S        |
| Icona\_         | [Identificatore](identifier.md) | N   | S        |
| IconIndex      | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>Progid
</dt> <dd>

ID programma o ID programma indipendente dalla versione. I ProgId elencati nella tabella ProgId vengono registrati se il CLSID elencato nella colonna Classe di questa tabella è pianificato per l'annuncio \_ o l'installazione. Quando il ProgId è selezionato per la registrazione, vengono selezionati anche tutti i ProgId che fanno riferimento a questa riga tramite la colonna Padre ProgId per \_ la registrazione.

</dd> <dt>

<span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>ProgId \_ Padre
</dt> <dd>

Definito solo per GLI ID programma indipendenti dalla versione. Questo campo è una chiave esterna nella colonna ProgId. Per definire un ID programma indipendente dalla versione, immettere il ProgId corrispondente nella colonna ProgId \_ Parent . Quando il ProgId è selezionato per l'installazione, vengono selezionati anche i ProgId indipendenti dalla versione corrispondenti associati tramite la colonna Padre ProgId \_ per la registrazione.

</dd> <dt>

<span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>Classe\_
</dt> <dd>

Chiave esterna facoltativa nella [tabella Class](class-table.md). Questa colonna deve essere Null per un ProgId indipendente dalla versione. Se il valore Class per un ProgId è Null, il ProgId viene registrato quando viene visualizzato nella colonna ProgId di una riga nella tabella Extension e all'estensione è associato almeno un verbo nella tabella \_ [Verbo](verb-table.md) [](extension-table.md) . I ProgId selezionati per la registrazione in questo modo non installano altri ProgId che fanno riferimento al ProgId corrente tramite il valore ProgId \_ Default.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Descrizione localizzata facoltativa dell'ID programma associato.

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icona\_
</dt> <dd>

Chiave esterna facoltativa nella tabella [Icon che](icon-table.md) specifica il file dell'icona associato a questo ProgId. Viene scritto sotto la chiave DefaultIcon associata a questo ProgId. Questa colonna deve essere Null per un ProgId indipendente dalla versione.

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Indice dell'icona nel file dell'icona. Questa colonna deve essere Null per un ProgId indipendente dalla versione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le [azioni RegisterProgIdInfo](registerprogidinfo-action.md) [e UnregisterProgIdInfo](unregisterprogidinfo-action.md) nelle tabelle [*di*](s-gly.md) sequenza elaborano le informazioni in questa tabella. Per informazioni sull'uso *delle tabelle di sequenza,* vedere [Using a Sequence Table](using-a-sequence-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE89](ice89.md)  
</dl>

 

 



