---
description: La tabella ModuleExclusion mantiene un elenco di altri moduli unione incompatibili nello stesso database del programma di installazione.
ms.assetid: c28d9afa-152c-43b5-9892-7a38fae8c593
title: Tabella ModuleExclusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 008d10e65d81b5668821e1a999cf08f5a10c55db3372a4b0230d560462a977c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996441"
---
# <a name="moduleexclusion-table"></a>Tabella ModuleExclusion

La tabella ModuleExclusion mantiene un elenco di altri moduli unione incompatibili nello stesso database del programma di installazione. Questa tabella consente a uno strumento di unione o verifica di verificare che i moduli unione in conflitto non siano uniti nel database del programma di installazione dell'utente. Lo strumento controlla facendo riferimento incrociato a questa tabella con la tabella ModuleSignature nel database del programma di installazione.

La tabella ModuleExclusion include le colonne seguenti.



| Colonna             | Tipo                         | Chiave | Nullable |
|--------------------|------------------------------|-----|----------|
| ModuleID           | [Identificatore](identifier.md) | S   | N        |
| ModuleLanguage     | [Integer](integer.md)       | S   | N        |
| ExcludedID         | [Identificatore](identifier.md) | S   | N        |
| Lingua esclusa   | [Integer](integer.md)       | S   | N        |
| ExcludedMinVersion | [Version](version.md)       |     | S        |
| ExcludedMaxVersion | [Version](version.md)       |     | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>Moduleid
</dt> <dd>

Identificatore del modulo unione. Si tratta di una chiave esterna nella [tabella ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage
</dt> <dd>

ID lingua decimale del modulo unione in ModuleID. Si tratta di una chiave esterna nella [tabella ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>ExcludedID
</dt> <dd>

Identificatore di un modulo unione escluso.

</dd> <dt>

<span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage
</dt> <dd>

ID lingua numerico del modulo unione in ExcludedID. La colonna ExcludedLanguage può specificare l'ID lingua per una singola lingua, ad esempio 1033 per l'inglese degli Stati Uniti, oppure specificare l'ID lingua per un gruppo di lingue, ad esempio 9 per qualsiasi inglese. La colonna ExcludedLanguage può accettare ID lingua negativi. Il significato del valore nella colonna ExcludedLanguage è il seguente.



| Lingua esclusa | Significato                                                              |
|------------------|----------------------------------------------------------------------|
| > 0           | Escludere gli ID di lingua specificati da ExcludedLanguage.              |
| = 0              | Non escludere id lingua.                                             |
| < 0           | Escludere tutti gli ID lingua tranne quelli specificati da ExcludedLanguage. |



 

</dd> <dt>

<span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion
</dt> <dd>

Versione minima esclusa da un intervallo. Se il campo ExcludedMinVersion è Null, vengono escluse tutte le versioni precedenti a ExcludedMaxVersion. Se sia ExcludedMinVersion che ExcludedMaxVersion sono Null, non esiste alcuna esclusione in base alla versione.

</dd> <dt>

<span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion
</dt> <dd>

Versione massima esclusa da un intervallo. Se il campo ExcludedMaxVersion è Null, vengono escluse tutte le versioni successive a ExcludedMinVersion. Se sia ExcludedMinVersion che ExcludedMaxVersion sono Null, non esiste alcuna esclusione in base alla versione.

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

 

 



