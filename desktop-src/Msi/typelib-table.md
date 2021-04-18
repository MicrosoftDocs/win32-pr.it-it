---
description: La tabella TypeLib contiene le informazioni che devono essere inserite nella registrazione del registro di sistema delle librerie dei tipi.
ms.assetid: 86b827ed-e707-4627-9488-78eafb444d32
title: Tabella TypeLib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0aa8949df75162ffb7107b633ab766d276c4b42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305628"
---
# <a name="typelib-table"></a>Tabella TypeLib

La tabella TypeLib contiene le informazioni che devono essere inserite nella registrazione del registro di sistema delle librerie dei tipi.

La tabella TypeLib contiene le colonne seguenti.



| Colonna      | Tipo                               | Chiave | Nullable |
|-------------|------------------------------------|-----|----------|
| LibID       | [GUID](guid.md)                   | S   | N        |
| Linguaggio    | [Integer](integer.md)             | S   | N        |
| Componente\_ | [Identificatore](identifier.md)       | S   | N        |
| Versione     | [DoubleInteger](doubleinteger.md) | N   | S        |
| Descrizione | [Text](text.md)                   | N   | S        |
| Directory\_ | [Identificatore](identifier.md)       | N   | S        |
| Funzionalità\_   | [Identificatore](identifier.md)       | N   | N        |
| Costo        | [DoubleInteger](doubleinteger.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LibID
</dt> <dd>

GUID che identifica la libreria.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Linguaggio
</dt> <dd>

Lingua della libreria dei tipi. Deve essere un numero non negativo.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella prima colonna della tabella dei [componenti](component-table.md). Questa colonna identifica il componente che appartiene alla funzionalità \_ il cui file di chiave è la libreria dei tipi registrata.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versione
</dt> <dd>

Questa è la versione della libreria. Le versioni principale e secondaria vengono codificate nel valore integer a quattro byte. La versione secondaria si trova negli otto bit inferiori. La versione principale è la metà di sedici bit.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Descrizione localizzabile della libreria.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_
</dt> <dd>

Chiave esterna nella prima colonna della tabella di [directory](directory-table.md). In questa colonna viene identificato il percorso della Guida per la libreria dei tipi. Questa colonna viene ignorata durante la pubblicità.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_
</dt> <dd>

Chiave esterna nella prima colonna della tabella delle [funzionalità](feature-table.md). In questa colonna viene specificata la funzionalità che deve essere installata per rendere operativa la libreria dei tipi.

</dd> <dt>

<span id="Cost"></span><span id="cost"></span><span id="COST"></span>Costo
</dt> <dd>

Costo associato alla registrazione della libreria dei tipi in byte. Deve essere un numero non negativo o null.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene definita quando viene eseguita l'azione [RegisterTypeLibraries](registertypelibraries-action.md) o [UnregisterTypeLibraries](unregistertypelibraries-action.md) .

Il programma di installazione scrive tutte le informazioni di registrazione della libreria dei tipi nel \_ \_ percorso del registro di sistema HKLM (hKey local machine). Questo è il caso anche per le installazioni per utente. Non è possibile registrare le librerie di tipi in percorsi per utente (HKCU).

Gli autori dei pacchetti di installazione si sconsigliano vivamente di utilizzare la tabella TypeLib. Devono invece registrare le librerie dei tipi usando la tabella [del registro di sistema](registry-table.md) . I motivi per evitare la registrazione automatica includono:

-   Se un'installazione che utilizza la tabella TypeLib ha esito negativo ed è necessario eseguirne il rollback, è possibile che il rollback non ripristini il computer nello stesso stato esistente prima del rollback. Le librerie di tipi registrate prima del rollback potrebbero non essere registrate dopo il rollback.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
</dl>

 

 



