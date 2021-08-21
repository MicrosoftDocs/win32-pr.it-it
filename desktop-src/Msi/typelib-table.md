---
description: La tabella TypeLib contiene le informazioni che devono essere inserite nella registrazione del Registro di sistema delle librerie dei tipi.
ms.assetid: 86b827ed-e707-4627-9488-78eafb444d32
title: Tabella TypeLib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862bc37e325f8c615e8158cfa431c927841f6b33c403c804726cea8fee6f0469
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500001"
---
# <a name="typelib-table"></a>Tabella TypeLib

La tabella TypeLib contiene le informazioni che devono essere inserite nella registrazione del Registro di sistema delle librerie dei tipi.

La tabella TypeLib include le colonne seguenti.



| Colonna      | Tipo                               | Chiave | Nullable |
|-------------|------------------------------------|-----|----------|
| LibID       | [GUID](guid.md)                   | S   | N        |
| Linguaggio    | [Integer](integer.md)             | S   | N        |
| Componente\_ | [Identificatore](identifier.md)       | S   | N        |
| Versione     | [DoubleInteger](doubleinteger.md) | N   | S        |
| Descrizione | [Text](text.md)                   | N   | S        |
| Directory\_ | [Identificatore](identifier.md)       | N   | S        |
| Funzionalità\_   | [Identificatore](identifier.md)       | N   | N        |
| Cost        | [DoubleInteger](doubleinteger.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="LibID"></span><span id="libid"></span><span id="LIBID"></span>LibID
</dt> <dd>

GUID che identifica la libreria.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Lingua
</dt> <dd>

Linguaggio della libreria dei tipi. Deve essere un numero non negativo.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella prima colonna della [tabella Component](component-table.md). Questa colonna identifica il componente appartenente a Feature \_ il cui file di chiave è la libreria dei tipi da registrare.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versione
</dt> <dd>

Questa è la versione della libreria. Le versioni principale e secondaria sono codificate nel valore integer a quattro byte. La versione secondaria si trova negli otto bit inferiori. La versione principale è al centro dei sedici bit.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Descrizione localizzabile della libreria.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_
</dt> <dd>

Chiave esterna nella prima colonna della [tabella Directory](directory-table.md). Questa colonna identifica il percorso della Guida per la libreria dei tipi. Questa colonna viene ignorata durante la pubblicità.

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_
</dt> <dd>

Chiave esterna nella prima colonna della [tabella Funzionalità](feature-table.md). Questa colonna specifica la funzionalità che deve essere installata perché la libreria dei tipi sia operativa.

</dd> <dt>

<span id="Cost"></span><span id="cost"></span><span id="COST"></span>Costo
</dt> <dd>

Costo associato alla registrazione della libreria dei tipi in byte. Deve essere un numero non negativo o null.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene indicata quando viene eseguita [l'azione RegisterTypeLibraries](registertypelibraries-action.md) o [UnregisterTypeLibraries.](unregistertypelibraries-action.md)

Il programma di installazione scrive tutte le informazioni di registrazione della libreria dei tipi nel percorso del Registro di sistema \_ HKEY LOCAL \_ MACHINE (HKLM). Questo è il caso anche per le installazioni per utente. Le librerie dei tipi non possono essere registrate in percorsi per utente (HKCU).

Gli autori di pacchetti di installazione sono fortemente sconsigliati di usare la tabella TypeLib. Devono invece registrare le librerie dei tipi usando la [tabella Del Registro di](registry-table.md) sistema. I motivi per evitare la registrazione automatica includono:

-   Se un'installazione che usa la tabella TypeLib ha esito negativo e deve essere eseguito il rollback, è possibile che il rollback non ripristini il computer allo stesso stato esistente prima del rollback. Le librerie dei tipi registrate prima del rollback potrebbero non essere registrate dopo il rollback.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
</dl>

 

 



