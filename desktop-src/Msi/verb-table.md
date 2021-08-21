---
description: La tabella Verb contiene informazioni sui verbi di comando associate alle estensioni di file che devono essere generate come parte dell'annuncio del prodotto. Ogni riga genera un set di chiavi e valori del Registro di sistema.
ms.assetid: 3749095c-f0c0-498c-969f-a6c445cfdd62
title: Tabella dei verbi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fc546cd3db5fecb3861120fa15b1ffa3f21327b889599b77a1b067193c886c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499111"
---
# <a name="verb-table"></a>Tabella dei verbi

La tabella Verb contiene informazioni sui verbi di comando associate alle estensioni di file che devono essere generate come parte dell'annuncio del prodotto. Ogni riga genera un set di chiavi e valori del Registro di sistema.

La tabella Verb include le colonne seguenti.



| Colonna      | Tipo                       | Chiave | Nullable |
|-------------|----------------------------|-----|----------|
| Estensione\_ | [Text](text.md)           | S   | N        |
| Verbo        | [Text](text.md)           | S   | N        |
| Sequenza    | [Integer](integer.md)     | N   | Y        |
| Comando     | [Formattato](formatted.md) | N   | S        |
| Argomento    | [Formattato](formatted.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Estensione\_
</dt> <dd>

Estensione associata alla riga della tabella. Questa colonna è una chiave esterna per la prima colonna della [tabella Extension](extension-table.md).

</dd> <dt>

<span id="Verb"></span><span id="verb"></span><span id="VERB"></span>Verbo
</dt> <dd>

Verbo per il comando.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenza
</dt> <dd>

Sequenza dei comandi. Solo i verbi per cui la colonna Sequence è non Null vengono usati per preparare un elenco ordinato per il valore predefinito della chiave della shell. Il verbo con il valore più basso in questa colonna diventa il verbo predefinito.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Comando
</dt> <dd>

Testo localizzabile visualizzato nel menu di scelta rapida.

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>discussione
</dt> <dd>

Valore per gli argomenti del comando.

Si noti che la risoluzione delle proprietà nel campo Argomento è limitata. Una proprietà formattata come Proprietà in questo campo può essere risolta solo se la proprietà ha già il valore previsto quando viene installato il componente proprietario \[  \] del verbo. Ad esempio, per risolvere l'argomento "MyDoc.doc" nel valore corretto, lo stesso processo deve installare il file MyDoc.doc e il componente proprietario del \[ \# \] verbo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene indicata quando viene eseguita [l'azione RegisterExtensionInfo](registerextensioninfo-action.md) o [UnregisterExtensionInfo.](unregisterextensioninfo-action.md)

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



