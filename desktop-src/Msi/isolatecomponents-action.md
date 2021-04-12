---
description: L'azione IsolateComponents installa una copia di un componente (in genere una DLL condivisa) in una posizione privata per l'uso da parte di un'applicazione specifica, in genere un file con estensione exe.
ms.assetid: 3f39ad5d-5539-48cc-8369-bd4d3127fbdd
title: Azione IsolateComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fe36f8c30e67591662ca2fce6c0b0ac2150ebb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348981"
---
# <a name="isolatecomponents-action"></a>Azione IsolateComponents

L'azione IsolateComponents installa una copia di un componente (in genere una DLL condivisa) in una posizione privata per l'uso da parte di un'applicazione specifica, in genere un file con estensione exe. Questo consente di isolare l'applicazione da altre copie del componente che possono essere installate in un percorso condiviso nel computer. Per ulteriori informazioni, vedere [componenti isolati](isolated-components.md).

L'azione fa riferimento a ogni record della [tabella IsolatedComponent](isolatedcomponent-table.md) e associa i file del componente elencato nel \_ campo Shared Component con il componente elencato nel \_ campo applicazione componente. Il programma di installazione installa i file di componente \_ condivisi nella stessa directory dell' \_ applicazione Component. Il programma di installazione genera un file in questa directory, con una lunghezza pari a zero byte, con il nome di nome file breve del file di chiave per l' \_ applicazione componente (in genere si tratta dello stesso nome del file con estensione exe) aggiunto con. local. L'azione IsolatedComponent non influisce sull'installazione dell' \_ applicazione Component. La disinstallazione dell' \_ applicazione componente consente inoltre di rimuovere i \_ file condivisi del componente e il file. local dalla directory.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione IsolateComponents può essere utilizzata solo nella [tabella InstallUISequence](installuisequence-table.md) e nella [tabella InstallExecuteSequence](installexecutesequence-table.md). Questa azione deve essere successiva all'azione [CostInitialize](costinitialize-action.md) e prima dell' [azione CostFinalize secondo](costfinalize-action.md).

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="remarks"></a>Commenti

Se la colonna Condition per l'azione IsolateComponents restituisce true o viene lasciato vuoto, il programma di installazione isola tutti i componenti elencati nella [tabella IsolatedComponent](isolatedcomponent-table.md). Se la colonna Condition restituisce false, il programma di installazione ignora la tabella IsolatedComponent e condivide i componenti normalmente. Per condizionare questa azione, è possibile usare la proprietà [**RedirectedDllSupport**](redirecteddllsupport.md) . Per ulteriori informazioni, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).

 

 



