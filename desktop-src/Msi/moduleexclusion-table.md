---
description: La tabella ModuleExclusion mantiene un elenco di altri moduli merge che non sono compatibili nello stesso database del programma di installazione.
ms.assetid: c28d9afa-152c-43b5-9892-7a38fae8c593
title: Tabella ModuleExclusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fb4cc136937d5a01bd16a42c138532dd524ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401769"
---
# <a name="moduleexclusion-table"></a>Tabella ModuleExclusion

La tabella ModuleExclusion mantiene un elenco di altri moduli merge che non sono compatibili nello stesso database del programma di installazione. Questa tabella consente a uno strumento di merge o di verifica di verificare che i moduli merge in conflitto non siano Uniti nel database del programma di installazione dell'utente. Lo strumento esegue il controllo incrociato della tabella con la tabella ModuleSignature nel database del programma di installazione.

La tabella ModuleExclusion include le colonne seguenti.



| Colonna             | Tipo                         | Chiave | Nullable |
|--------------------|------------------------------|-----|----------|
| ModuleID           | [Identificatore](identifier.md) | S   | N        |
| ModuleLanguage     | [Integer](integer.md)       | S   | N        |
| ExcludedID         | [Identificatore](identifier.md) | S   | N        |
| ExcludedLanguage   | [Integer](integer.md)       | S   | N        |
| ExcludedMinVersion | [Versione](version.md)       |     | S        |
| ExcludedMaxVersion | [Versione](version.md)       |     | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

Identificatore del modulo merge. Si tratta di una chiave esterna nella [tabella ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="ModuleLanguage"></span><span id="modulelanguage"></span><span id="MODULELANGUAGE"></span>ModuleLanguage
</dt> <dd>

ID della lingua decimale del modulo merge in ModuleID. Si tratta di una chiave esterna nella [tabella ModuleSignature](modulesignature-table.md).

</dd> <dt>

<span id="ExcludedID"></span><span id="excludedid"></span><span id="EXCLUDEDID"></span>ExcludedID
</dt> <dd>

Identificatore di un modulo merge escluso.

</dd> <dt>

<span id="ExcludedLanguage"></span><span id="excludedlanguage"></span><span id="EXCLUDEDLANGUAGE"></span>ExcludedLanguage
</dt> <dd>

ID lingua numerica del modulo merge in ExcludedID. La colonna ExcludedLanguage può specificare l'ID lingua per una sola lingua, ad esempio 1033 per l'inglese (Stati Uniti), oppure specificare l'ID lingua per un gruppo di lingue, ad esempio 9 per qualsiasi lingua inglese. La colonna ExcludedLanguage può accettare ID di lingua negativi. Il significato del valore nella colonna ExcludedLanguage è il seguente.



| ExcludedLanguage | Significato                                                              |
|------------------|----------------------------------------------------------------------|
| > 0           | Escludi gli ID lingua specificati da ExcludedLanguage.              |
| = 0              | Escludere nessun ID di lingua.                                             |
| < 0           | Escludere tutti gli ID lingua eccetto quelli specificati da ExcludedLanguage. |



 

</dd> <dt>

<span id="ExcludedMinVersion"></span><span id="excludedminversion"></span><span id="EXCLUDEDMINVERSION"></span>ExcludedMinVersion
</dt> <dd>

Versione minima esclusa da un intervallo. Se il campo ExcludedMinVersion è null, vengono escluse tutte le versioni precedenti a ExcludedMaxVersion. Se ExcludedMinVersion e ExcludedMaxVersion sono null, non esiste alcuna esclusione in base alla versione.

</dd> <dt>

<span id="ExcludedMaxVersion"></span><span id="excludedmaxversion"></span><span id="EXCLUDEDMAXVERSION"></span>ExcludedMaxVersion
</dt> <dd>

Versione massima esclusa da un intervallo. Se il campo ExcludedMaxVersion è null, tutte le versioni dopo ExcludedMinVersion vengono escluse. Se ExcludedMinVersion e ExcludedMaxVersion sono null, non esiste alcuna esclusione in base alla versione.

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

 

 



