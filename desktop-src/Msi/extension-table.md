---
description: La tabella di estensione contiene informazioni sui server di estensione del nome di file che devono essere generati come parte dell'annuncio del prodotto. Ogni riga genera un set di chiavi e valori del registro di sistema.
ms.assetid: 924858b7-8956-4636-b7c7-c902aa822ee1
title: Tabella di estensione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef52f7248f44dcb63255244bbd8abd4ac8181d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309484"
---
# <a name="extension-table"></a>Tabella di estensione

La tabella di estensione contiene informazioni sui server di estensione del nome di file che devono essere generati come parte dell'annuncio del prodotto. Ogni riga genera un set di chiavi e valori del registro di sistema.

La tabella di estensione contiene le colonne mostrate nella tabella seguente.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Estensione   | [Text](text.md)             | S   | N        |
| Componente\_ | [Identificatore](identifier.md) | S   | N        |
| ProgId\_    | [Text](text.md)             | N   | S        |
| MIME\_      | [Text](text.md)             | N   | S        |
| Funzionalità\_   | [Identificatore](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Estensione
</dt> <dd>

Estensione associata alla riga della tabella. L'estensione può avere una lunghezza di 255 caratteri. Immettere l'estensione in questo campo senza il periodo precedente.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna per la prima colonna della tabella dei [componenti](component-table.md) . Questa colonna fa riferimento al componente che controlla l'installazione dell'estensione.

</dd> <dt>

<span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>ProgId\_
</dt> <dd>

ID programma associato a questa estensione. Si tratta di una chiave esterna nella tabella [ProgID](progid-table.md) .

</dd> <dt>

<span id="MIME_"></span><span id="mime_"></span>MIME\_
</dt> <dd>

Tipo di contenuto da scrivere per la colonna di estensione.

Chiave esterna per la prima colonna della tabella [MIME](mime-table.md) .

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_
</dt> <dd>

Chiave esterna nella prima colonna della tabella delle [funzionalità](feature-table.md) che specifica la funzionalità che fornisce il server di estensione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Viene fatto riferimento alla tabella di estensione quando viene eseguita l'azione [RegisterExtensionInfo](registerextensioninfo-action.md) o [UnRegisterExtensionInfo](unregisterextensioninfo-action.md) .

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE15](ice15.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE69](ice69.md)  
</dl>

 

 



