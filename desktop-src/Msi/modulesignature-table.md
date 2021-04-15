---
description: La tabella ModuleSignature è una tabella obbligatoria.
ms.assetid: 09802282-72ad-43f1-8cce-4cdc68b01e87
title: Tabella ModuleSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75e3bb013472c49d18fa44b840ce07b11728faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529244"
---
# <a name="modulesignature-table"></a>Tabella ModuleSignature

La tabella ModuleSignature è una tabella obbligatoria. Contiene tutte le informazioni necessarie per identificare un modulo merge. Lo strumento merge aggiunge questa tabella al file con estensione msi, se non ne esiste già una. La tabella ModuleSignature in un modulo merge include solo una riga contenente ModuleID, Language e Version. Tuttavia, la tabella ModuleSignature in un file con estensione msi include una riga contenente queste informazioni per ogni file con estensione MSM di cui è stato eseguito il merge.

Strumenti di merge e verifica controllare la tabella ModuleSignature nei file con estensione msi per determinare se sono presenti tutti i moduli merge dipendenti richiesti dal modulo merge corrente (vedere la [tabella ModuleDependency](moduledependency-table.md)) e se il pacchetto di installazione è stato precedentemente Unito a eventuali moduli merge in conflitto (vedere la [tabella ModuleExclusion](moduleexclusion-table.md)).

La tabella ModuleSignature include le colonne seguenti.



| Colonna   | Tipo                         | Chiave | Nullable |
|----------|------------------------------|-----|----------|
| ModuleID | [Identificatore](identifier.md) | S   | N        |
| Linguaggio | [Integer](integer.md)       | S   | N        |
| Versione  | [Versione](version.md)       |     | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

Identificatore che identifica in modo univoco il modulo unione. Due moduli merge non possono avere lo stesso ModuleID, a meno che il modulo merge non sia completamente compatibile con il relativo predecessore. È possibile creare un GUID per questo campo usando un'utilità, ad esempio GUIDGEN. La colonna ModuleID è una chiave primaria per la tabella e pertanto deve seguire la convenzione di denominazione per la [denominazione delle chiavi primarie nei database del modulo merge](naming-primary-keys-in-merge-module-databases.md). Se, ad esempio, il nome leggibile del modulo merge è MyLibrary e il GUID è {880DE2F0-CDD8-11D1-A849-006097ABDE17}, la voce nella colonna ModuleID diventa MyLibrary. 880DE2F0 \_ CDD8 11D1 A849 \_ 006097ABDE17 \_ \_ .

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Linguaggio
</dt> <dd>

L'identificatore di lingua specifica la lingua predefinita per il modulo unione. L'identificatore di lingua è in formato decimale, ad esempio l'inglese (Stati Uniti) è 1033. Il linguaggio utilizzato dal modulo merge può essere modificato applicando una trasformazione al modulo merge prima dell'Unione.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>Versione
</dt> <dd>

Il campo versione contiene una stringa che descrive le versioni principale e secondaria del modulo merge.

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Moduli unione a più lingue](multiple-language-merge-modules.md)
</dt> </dl>

 

 



