---
description: Ogni record della tabella IsolatedComponent associa il componente specificato nella \_ colonna applicazione componente (in genere un file con estensione exe) con il componente specificato nella \_ colonna condivisa componente (in genere una DLL condivisa).
ms.assetid: dc30e4c7-a938-4060-be4f-744de9c20fd9
title: Tabella IsolatedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3e6c5bdba6efc546a36e77fa793c0b397f6d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307261"
---
# <a name="isolatedcomponent-table"></a>Tabella IsolatedComponent

Ogni record della tabella IsolatedComponent associa il componente specificato nella \_ colonna applicazione componente (in genere un file con estensione exe) con il componente specificato nella \_ colonna condivisa componente (in genere una DLL condivisa). L' [azione IsolateComponents](isolatecomponents-action.md) installa una copia del componente \_ condiviso in una posizione privata per l'uso da parte \_ dell'applicazione componente. In questo modo l' \_ applicazione componente viene isolata da altre copie di componenti \_ condivisi che possono essere installate in un percorso condiviso nel computer. Vedere [componenti isolati](isolated-components.md).

Per collegare un componente \_ condiviso a più \_ applicazioni componente, includere un record separato per ogni coppia nella tabella IsolatedComponents. Il programma di installazione copia i file di componente \_ condivisi nella directory di ogni \_ applicazione componente installata.

La tabella IsolatedComponent include le colonne seguenti.



| Colonna                 | Tipo                         | Chiave | Nullable |
|------------------------|------------------------------|-----|----------|
| Componente \_ condiviso      | [Identificatore](identifier.md) | S   | N        |
| \_Applicazione componente | [Identificatore](identifier.md) | S   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Componente \_ condiviso
</dt> <dd>

Chiave esterna nella [tabella dei componenti](component-table.md). Componente che contiene il file condiviso, in genere una DLL. La DLL deve essere il file di chiave per questo componente. Deve trattarsi di un componente diverso da quello elencato nella \_ colonna applicazione componente.

Il componente condiviso controlla la registrazione per tutte le copie isolate del componente ed è necessario impostare il flag **msidbComponentAttributesSharedDllRefCount** nella colonna attributi della tabella dei componenti. Ciò garantisce che il programma di installazione possa gestire la durata del componente condiviso.

</dd> <dt>

<span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>\_Applicazione componente
</dt> <dd>

Chiave esterna nella [tabella dei componenti](component-table.md). Componente che contiene il file con estensione exe che carica il file condiviso. Il file con estensione exe deve essere il file di chiave per questo componente. Deve trattarsi di un componente diverso da quello elencato nella \_ colonna Shared Component.

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

 

 



