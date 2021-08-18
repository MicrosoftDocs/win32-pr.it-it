---
description: La tabella Extension contiene informazioni sui server di estensione di file che devono essere generati come parte dell'annuncio del prodotto. Ogni riga genera un set di chiavi e valori del Registro di sistema.
ms.assetid: 924858b7-8956-4636-b7c7-c902aa822ee1
title: Tabella delle estensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d664df812b723d7ab6c9b966b09fac8c57a35b655e123f720fdb87bdf431146
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821741"
---
# <a name="extension-table"></a>Tabella delle estensioni

La tabella Extension contiene informazioni sui server di estensione di file che devono essere generati come parte dell'annuncio del prodotto. Ogni riga genera un set di chiavi e valori del Registro di sistema.

La tabella Extension contiene le colonne illustrate nella tabella seguente.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Estensione   | [Text](text.md)             | S   | N        |
| Componente\_ | [Identificatore](identifier.md) | S   | N        |
| Progid\_    | [Text](text.md)             | N   | S        |
| MIME\_      | [Text](text.md)             | N   | S        |
| Funzionalità\_   | [Identificatore](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Estensione
</dt> <dd>

Estensione associata alla riga della tabella. L'estensione può contenere fino a 255 caratteri. Immettere l'estensione in questo campo senza il punto precedente.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna alla prima colonna della [tabella Component.](component-table.md) Questa colonna fa riferimento al componente che controlla l'installazione dell'estensione.

</dd> <dt>

<span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>Progid\_
</dt> <dd>

ID programma associato a questa estensione. Si tratta di una chiave esterna nella [tabella ProgId.](progid-table.md)

</dd> <dt>

<span id="MIME_"></span><span id="mime_"></span>Mime\_
</dt> <dd>

Tipo di contenuto da scrivere per la colonna Estensione.

Chiave esterna alla prima colonna della [tabella MIME.](mime-table.md)

</dd> <dt>

<span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Funzionalità\_
</dt> <dd>

Chiave esterna nella prima colonna della tabella [Feature](feature-table.md) che specifica la funzionalità che fornisce il server di estensione.

</dd> </dl>

## <a name="remarks"></a>Commenti

La tabella Extension viene indicata quando viene eseguita [l'azione RegisterExtensionInfo](registerextensioninfo-action.md) o [UnRegisterExtensionInfo.](unregisterextensioninfo-action.md)

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

 

 



