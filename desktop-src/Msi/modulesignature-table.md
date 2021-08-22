---
description: La tabella ModuleSignature è una tabella obbligatoria.
ms.assetid: 09802282-72ad-43f1-8cce-4cdc68b01e87
title: Tabella ModuleSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f269215fef06af5eeacc80f1356c2ad2226c20075c1d09f1e128c062438508
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945339"
---
# <a name="modulesignature-table"></a>Tabella ModuleSignature

La tabella ModuleSignature è una tabella obbligatoria. Contiene tutte le informazioni necessarie per identificare un modulo di merge. Lo strumento di unione aggiunge questa tabella al file .msi, se non ne esiste già una. La tabella ModuleSignature in un modulo di unione include una sola riga contenente ModuleID, Language e Version. Tuttavia, la tabella ModuleSignature in un file .msi contiene queste informazioni per ogni file con estensione msm unito.

Gli strumenti di unione e verifica controllano la tabella ModuleSignature nei file di .msi per determinare se sono presenti tutti i moduli unione dipendenti richiesti dal modulo di merge corrente (vedere [Tabella ModuleDependency](moduledependency-table.md)) e se il pacchetto di installazione è stato precedentemente unito a eventuali moduli unione in conflitto (vedere [Tabella ModuleExclusion).](moduleexclusion-table.md)

La tabella ModuleSignature contiene le colonne seguenti.



| Colonna   | Tipo                         | Chiave | Nullable |
|----------|------------------------------|-----|----------|
| ModuleID | [Identificatore](identifier.md) | S   | N        |
| Linguaggio | [Integer](integer.md)       | S   | N        |
| Versione  | [Version](version.md)       |     | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>Moduleid
</dt> <dd>

Identificatore che identifica in modo univoco il modulo unione. Due moduli unione non possono avere lo stesso ModuleID a meno che il modulo di merge non sia completamente compatibile con il relativo predecessore. È possibile creare un GUID per questo campo usando un'utilità come GUIDGEN. La colonna ModuleID è una chiave primaria per la tabella e pertanto deve seguire la convenzione di denominazione in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md). Ad esempio, se il nome leggibile del modulo di unione è MyLibrary e il GUID è {880DE2F0-CDD8-11D1-A849-006097ABDE17}, la voce nella colonna ModuleID diventa MyLibrary.880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Lingua
</dt> <dd>

L'identificatore di lingua specifica la lingua predefinita per il modulo di unione. L'identificatore di lingua è in formato decimale, ad esempio l'inglese (Stati Uniti) è 1033. Il linguaggio usato dal modulo di unione può essere modificato applicando una trasformazione al modulo di merge prima dell'unione.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versione
</dt> <dd>

Il campo Version contiene una stringa che descrive le versioni principale e secondaria del modulo unione.

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Più moduli unione in linguaggio](multiple-language-merge-modules.md)
</dt> </dl>

 

 



