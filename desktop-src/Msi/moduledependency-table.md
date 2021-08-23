---
description: La tabella ModuleDependency mantiene un elenco di altri moduli unione necessari per il corretto funzionamento di questo modulo unione.
ms.assetid: 36418331-bec7-40c9-8fdf-fe4b958a1443
title: Tabella ModuleDependency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d527ba5874c8fffb0234dbf8f041f424b7bf9aecff5e8f29005324f2a17fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628585"
---
# <a name="moduledependency-table"></a>Tabella ModuleDependency

La tabella ModuleDependency mantiene un elenco di altri moduli unione necessari per il corretto funzionamento di questo modulo unione. Questa tabella consente a uno strumento di unione o verifica di garantire che i moduli unione necessari siano inclusi nel database del programma di installazione dell'utente. Lo strumento controlla facendo riferimento incrociato a questa tabella con la tabella ModuleSignature nel database del programma di installazione.

La tabella ModuleDependency include le colonne seguenti.



| Colonna           | Tipo                         | Chiave | Nullable |
|------------------|------------------------------|-----|----------|
| ModuleID         | [Identificatore](identifier.md) | S   | N        |
| ModuleLanguage   | [Integer](integer.md)       | S   | N        |
| RequiredID       | [Identificatore](identifier.md) | S   | N        |
| RequiredLanguage | [Integer](integer.md)       | S   | N        |
| RequiredVersion  | [Version](version.md)       |     | S        |



 

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

<span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>RequiredID
</dt> <dd>

Identificatore del modulo unione richiesto dal modulo unione in ModuleID.

</dd> <dt>

<span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>RequiredLanguage
</dt> <dd>

ID lingua numerico del modulo unione in RequiredID. La colonna RequiredLanguage può specificare l'ID lingua per una singola lingua, ad esempio 1033 per l'inglese degli Stati Uniti, oppure specificare l'ID lingua per un gruppo di lingue, ad esempio 9 per qualsiasi inglese. Se il campo contiene un ID lingua del gruppo, qualsiasi modulo unione con un codice lingua in tale gruppo soddisfa la dipendenza. Se RequiredLanguage è impostato su 0, qualsiasi modulo unione che soddisfa gli altri requisiti soddisfa la dipendenza.

</dd> <dt>

<span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion
</dt> <dd>

Versione del modulo unione in RequiredID. Se questo campo è Null, qualsiasi versione riempie la dipendenza.

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

 

 



