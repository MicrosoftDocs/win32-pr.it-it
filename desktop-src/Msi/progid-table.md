---
description: La tabella ProgId contiene informazioni per gli ID programma e gli ID del programma indipendenti dalla versione che devono essere generati come parte dell'annuncio del prodotto.
ms.assetid: 66a7e170-6f70-4db7-98f4-8a074471b9f2
title: Tabella ProgId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 293ce3748f691b664d55b0a1158a574472388202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968510"
---
# <a name="progid-table"></a>Tabella ProgId

La tabella ProgId contiene informazioni per gli ID programma e gli ID del programma indipendenti dalla versione che devono essere generati come parte dell'annuncio del prodotto.

La tabella ProgId contiene le colonne seguenti.



| Colonna         | Tipo                         | Chiave | Nullable |
|----------------|------------------------------|-----|----------|
| ProgId         | [Text](text.md)             | S   | N        |
| ProgId \_ padre | [Text](text.md)             | N   | S        |
| Classe\_        | [GUID](guid.md)             | N   | S        |
| Descrizione    | [Text](text.md)             | N   | S        |
| Icona\_         | [Identificatore](identifier.md) | N   | S        |
| IconIndex      | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="ProgId"></span><span id="progid"></span><span id="PROGID"></span>ProgId
</dt> <dd>

ID del programma o ID del programma indipendente dalla versione. I ProgId elencati nella tabella ProgId vengono registrati se il CLSID elencato nella \_ colonna classe di questa tabella è pianificato per l'annuncio o l'installazione. Quando il ProgId è selezionato per la registrazione, tutti i ProgId che fanno riferimento a questa riga tramite la \_ colonna padre ProgID sono selezionati anche per la registrazione.

</dd> <dt>

<span id="ProgId_Parent"></span><span id="progid_parent"></span><span id="PROGID_PARENT"></span>ProgId \_ padre
</dt> <dd>

Definito solo per gli ID del programma indipendenti dalla versione. Questo campo è una chiave esterna nella colonna ProgId. Per definire un ID del programma indipendente dalla versione, immettere il ProgId corrispondente nella \_ colonna padre ProgID. Quando il ProgId è selezionato per l'installazione, vengono selezionati anche i ProgId corrispondenti indipendenti dalla versione associati tramite la \_ colonna padre ProgID per la registrazione.

</dd> <dt>

<span id="Class_"></span><span id="class_"></span><span id="CLASS_"></span>Classe\_
</dt> <dd>

Chiave esterna facoltativa nella [tabella della classe](class-table.md). Questa colonna deve essere null per un ProgId indipendente dalla versione. Se il valore della classe \_ per un ProgID è null, il ProgID viene registrato quando viene visualizzato nella colonna ProgID di una riga nella [tabella di estensione](extension-table.md) e all'estensione è associato almeno un verbo nella [tabella dei verbi](verb-table.md). I ProgId selezionati per la registrazione in questo modo non installano altri ProgId che fanno riferimento al ProgId corrente tramite il \_ valore predefinito ProgID.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Descrizione localizzata facoltativa dell'ID del programma associato.

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icona\_
</dt> <dd>

Chiave esterna facoltativa nella [tabella delle icone](icon-table.md) che specifica il file icona associato a questo ProgID. Questa operazione viene scritta sotto la chiave DefaultIcon associata a questo ProgId. Questa colonna deve essere null per un ProgId indipendente dalla versione.

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Indice dell'icona nel file icona. Questa colonna deve essere null per un ProgId indipendente dalla versione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le azioni [RegisterProgIdInfo](registerprogidinfo-action.md) e [UnregisterProgIdInfo](unregisterprogidinfo-action.md) nelle [*tabelle di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella. Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE89](ice89.md)  
</dl>

 

 



