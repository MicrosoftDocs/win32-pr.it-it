---
description: Ogni record della tabella IsolatedComponent associa il componente specificato nella colonna Applicazione componente (in genere un .exe) al componente specificato nella colonna Componente condiviso (in genere una \_ \_ DLL condivisa).
ms.assetid: dc30e4c7-a938-4060-be4f-744de9c20fd9
title: Tabella IsolatedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9644f1e122464e1321d55c0b615892167e84a7e059472adc4f01ee6bac571720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805619"
---
# <a name="isolatedcomponent-table"></a>Tabella IsolatedComponent

Ogni record della tabella IsolatedComponent associa il componente specificato nella colonna Applicazione componente (in genere un .exe) al componente specificato nella colonna Componente condiviso (in genere una \_ \_ DLL condivisa). [L'azione IsolateComponents](isolatecomponents-action.md) installa una copia di Componente \_ condiviso in un percorso privato per l'uso da parte dell'applicazione \_ componente. In questo modo l'applicazione componente viene isolata da altre copie di Component Shared che possono \_ essere installate in un percorso condiviso nel \_ computer. Vedere [Componenti isolati.](isolated-components.md)

Per collegare un componente \_ condiviso a più applicazioni \_ componenti, includere un record separato per ogni coppia nella tabella IsolatedComponents. Il programma di installazione copia i file di Componente \_ condiviso nella directory di ogni applicazione componente \_ installata.

La tabella IsolatedComponent contiene le colonne seguenti.



| Colonna                 | Tipo                         | Chiave | Nullable |
|------------------------|------------------------------|-----|----------|
| Componente \_ condiviso      | [Identificatore](identifier.md) | S   | N        |
| Applicazione \_ componente | [Identificatore](identifier.md) | S   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Componente \_ condiviso
</dt> <dd>

Chiave esterna nella [tabella Component](component-table.md). Componente che contiene il file condiviso, in genere una DLL. La DLL deve essere il file di chiave per questo componente. Deve trattarsi di un componente diverso da quello elencato nella \_ colonna Applicazione componente .

Il componente condiviso controlla la registrazione per tutte le copie isolate del componente e deve avere il flag **msidbComponentAttributesSharedDllRefCount** impostato nella colonna Attributi della tabella Component. Ciò garantisce che il programma di installazione possa gestire la durata del componente condiviso.

</dd> <dt>

<span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>Applicazione \_ componente
</dt> <dd>

Chiave esterna nella [tabella Component](component-table.md). Componente che contiene il .exe che carica il file condiviso. Il .exe deve essere il file di chiave per questo componente. Deve trattarsi di un componente diverso da quello elencato nella colonna \_ Componente condiviso .

</dd> </dl>

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE62](ice62.md)  
[ICE66](ice66.md)  
[ICE97](ice97.md)  
</dl>

 

 



