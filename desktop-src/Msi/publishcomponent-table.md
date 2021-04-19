---
description: La tabella PublishComponent associa i componenti elencati nella tabella Component con una stringa di testo qualificatore e un GUID ID categoria.
ms.assetid: 4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4
title: Tabella PublishComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb0edfd811873242629c36257fdce5a80fe9d91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311731"
---
# <a name="publishcomponent-table"></a>Tabella PublishComponent

La tabella PublishComponent associa i componenti elencati nella [tabella Component](component-table.md) con una stringa di testo qualificatore e un GUID ID categoria. I componenti con funzionalità parallele raggruppate in questo modo vengono definiti componenti qualificati. Vedere [componenti qualificati](qualified-components.md). Questa operazione fornisce al programma di installazione un metodo per il reindirizzamento a livello singolo quando si fa riferimento ai componenti. Vedere [uso di componenti qualificati](using-qualified-components.md).

La tabella PublishComponent include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| ComponentId | [GUID](guid.md)             | S   | N        |
| Qualifier   | [Text](text.md)             | S   | N        |
| Componente\_ | [Identificatore](identifier.md) | S   | N        |
| AppData     | [Text](text.md)             | N   | S        |
| Funzionalità\_   | [Identificatore](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId
</dt> <dd>

[GUID](guid.md) di stringa che rappresenta la categoria di componenti raggruppati. Si noti che il titolo di questa colonna è fuorviante. Si tratta del GUID per la categoria di componenti qualificati e non è lo stesso GUID visualizzato nella colonna ComponentId della [tabella dei componenti](component-table.md). Qui si riferisce a un server che fornisce la funzionalità di un componente ai client esterni anziché al componente stesso.

</dd> <dt>

<span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Qualificatore
</dt> <dd>

Stringa di testo che qualifica il valore nella colonna ComponentId. Un qualificatore viene utilizzato per distinguere più forme dello stesso componente, ad esempio un componente implementato in più lingue. Queste sono le stringhe di testo qualificatore restituite da [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella colonna uno della [tabella dei componenti](component-table.md). Questo identificatore fa riferimento al record del componente completo nella tabella dei componenti.

</dd> <dt>

<span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>AppData
</dt> <dd>

Testo localizzabile facoltativo che descrive il componente completo di questo record. La stringa viene comunemente analizzata dall'applicazione e può essere visualizzata all'utente. Dovrebbe descrivere il componente completo. Questa operazione può essere recuperata con [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_
</dt> <dd>

Chiave esterna nella colonna uno della [tabella delle funzionalità](feature-table.md). Questa è la funzionalità che usa questo componente qualificato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene definita quando viene eseguita l'azione [PublishComponents](publishcomponents-action.md) o [UnpublishComponents](unpublishcomponents-action.md) .

Si noti che il nome di questa tabella è fuorviante. Questa tabella non è necessaria per creare un annuncio pubblicitario. Per informazioni su come impostare lo stato di installazione dei componenti da pubblicizzare, vedere la colonna attributi della [tabella](component-table.md) dei componenti e della [tabella delle funzionalità](feature-table.md) .

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE22](ice22.md)  
[ICE32](ice32.md)  
</dl>

 

 



