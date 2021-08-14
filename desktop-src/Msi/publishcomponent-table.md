---
description: La tabella PublishComponent associa i componenti elencati nella tabella Component a una stringa di testo qualificatore e a un GUID ID categoria.
ms.assetid: 4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4
title: Tabella PublishComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0abd7567e8327aa36a120fd5a13115cb191e1660566e9d480446295dca53cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376384"
---
# <a name="publishcomponent-table"></a>Tabella PublishComponent

La tabella PublishComponent associa i componenti elencati nella [tabella Component](component-table.md) a una stringa di testo qualificatore e a un GUID ID categoria. I componenti con funzionalità parallele raggruppati in questo modo vengono definiti componenti qualificati. Vedere [Componenti qualificati](qualified-components.md). Questo fornisce al programma di installazione un metodo per il riferimento indiretto a livello singolo quando si fa riferimento ai componenti. Vedere [Uso di componenti qualificati](using-qualified-components.md).

La tabella PublishComponent include le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Componentid | [GUID](guid.md)             | S   | N        |
| Qualifier   | [Text](text.md)             | S   | N        |
| Componente\_ | [Identificatore](identifier.md) | S   | N        |
| AppData     | [Text](text.md)             | N   | S        |
| Funzionalità\_   | [Identificatore](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>Componentid
</dt> <dd>

GUID stringa [che](guid.md) rappresenta la categoria di componenti raggruppati. Si noti che il titolo di questa colonna è fuorviante. Si tratta del GUID per la categoria di componenti qualificati e non corrisponde al GUID visualizzato nella colonna ComponentId della [tabella Component](component-table.md). In questo caso si riferisce a un server che fornisce la funzionalità di un componente ai client esterni anziché al componente stesso.

</dd> <dt>

<span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Qualificatore
</dt> <dd>

Stringa di testo che qualifica il valore nella colonna ComponentId. Un qualificatore viene usato per distinguere più forme dello stesso componente, ad esempio un componente implementato in più linguaggi. Si tratta delle stringhe di testo del qualificatore restituite da [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella colonna uno della [tabella Componente](component-table.md). Questo identificatore fa riferimento al record del componente completo nella tabella Component.

</dd> <dt>

<span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>Appdata
</dt> <dd>

Testo localizzabile facoltativo che descrive il componente completo di questo record. La stringa viene in genere analizzata dall'applicazione e può essere visualizzata all'utente. Deve descrivere il componente completo. Può essere recuperato con [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_
</dt> <dd>

Chiave esterna nella colonna 1 della [tabella Funzionalità](feature-table.md). Questa è la funzionalità che usa questo componente completo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene indicata quando viene eseguita [l'azione PublishComponents](publishcomponents-action.md) o [UnpublishComponents.](unpublishcomponents-action.md)

Si noti che il nome di questa tabella è fuorviante. Questa tabella non è necessaria per creare un annuncio. Per informazioni su come impostare [](feature-table.md) lo stato di installazione dei componenti da [annunciare,](component-table.md) vedere la colonna Attributi della tabella Componente e la tabella Funzionalità.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE22](ice22.md)  
[ICE32](ice32.md)  
</dl>

 

 



