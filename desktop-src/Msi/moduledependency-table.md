---
description: La tabella ModuleDependency mantiene un elenco di altri moduli unione richiesti per il corretto funzionamento del modulo merge.
ms.assetid: 36418331-bec7-40c9-8fdf-fe4b958a1443
title: Tabella ModuleDependency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb0c550f8c5ae480a07ca10401d1d3b67c496ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313810"
---
# <a name="moduledependency-table"></a>Tabella ModuleDependency

La tabella ModuleDependency mantiene un elenco di altri moduli unione richiesti per il corretto funzionamento del modulo merge. Questa tabella consente uno strumento di Unione o verifica per garantire che i moduli unione necessari siano effettivamente inclusi nel database del programma di installazione dell'utente. Lo strumento esegue il controllo incrociato facendo riferimento a questa tabella con la tabella ModuleSignature nel database del programma di installazione.

La tabella ModuleDependency include le colonne seguenti.



| Colonna           | Tipo                         | Chiave | Nullable |
|------------------|------------------------------|-----|----------|
| ModuleID         | [Identificatore](identifier.md) | S   | N        |
| ModuleLanguage   | [Integer](integer.md)       | S   | N        |
| RequiredID       | [Identificatore](identifier.md) | S   | N        |
| RequiredLanguage | [Integer](integer.md)       | S   | N        |
| RequiredVersion  | [Versione](version.md)       |     | S        |



 

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

<span id="RequiredID"></span><span id="requiredid"></span><span id="REQUIREDID"></span>RequiredID
</dt> <dd>

Identificatore del modulo merge richiesto dal modulo merge in ModuleID.

</dd> <dt>

<span id="RequiredLanguage"></span><span id="requiredlanguage"></span><span id="REQUIREDLANGUAGE"></span>RequiredLanguage
</dt> <dd>

ID lingua numerica del modulo merge in RequiredID. La colonna RequiredLanguage può specificare l'ID lingua per una sola lingua, ad esempio 1033 per l'inglese (Stati Uniti), oppure specificare l'ID lingua per un gruppo di lingue, ad esempio 9 per qualsiasi lingua inglese. Se il campo contiene un ID lingua del gruppo, qualsiasi modulo merge con un codice lingua in tale gruppo soddisfa la dipendenza. Se RequiredLanguage è impostato su 0, qualsiasi modulo di merge che riempie gli altri requisiti soddisfa la dipendenza.

</dd> <dt>

<span id="RequiredVersion"></span><span id="requiredversion"></span><span id="REQUIREDVERSION"></span>RequiredVersion
</dt> <dd>

Versione del modulo merge in RequiredID. Se questo campo è null, qualsiasi versione compila la dipendenza.

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

 

 



