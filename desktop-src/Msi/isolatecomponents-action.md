---
description: L'azione IsolateComponents installa una copia di un componente (in genere una DLL condivisa) in un percorso privato per l'uso da parte di un'applicazione specifica (in genere un .exe).
ms.assetid: 3f39ad5d-5539-48cc-8369-bd4d3127fbdd
title: Azione IsolateComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2919a026fb8243d7f2f73bc856390865ea3bed19e228da780e39f9dce68bc3f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629734"
---
# <a name="isolatecomponents-action"></a>Azione IsolateComponents

L'azione IsolateComponents installa una copia di un componente (in genere una DLL condivisa) in un percorso privato per l'uso da parte di un'applicazione specifica (in genere un .exe). In questo modo l'applicazione viene isolata da altre copie del componente che possono essere installate in un percorso condiviso nel computer. Per altre informazioni, vedere [Componenti isolati](isolated-components.md).

L'azione fa riferimento a ogni record della tabella [IsolatedComponent](isolatedcomponent-table.md) e associa i file del componente elencati nel campo Componente condiviso al componente elencato nel \_ campo Applicazione \_ componente. Il programma di installazione installa i file di Componente \_ condiviso nella stessa directory dell'applicazione \_ componente. Il programma di installazione genera un file in questa directory di lunghezza pari a zero byte, con il nome breve del file di chiave per l'applicazione componente (in genere si tratta dello stesso nome file del .exe) aggiunto con \_ .local. L'azione IsolatedComponent non influisce sull'installazione di Applicazione \_ componente. La disinstallazione \_ dell'applicazione componente rimuove anche i file condivisi \_ del componente e il file con estensione local dalla directory.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

L'azione IsolateComponents può essere usata solo nella [tabella InstallUISequence](installuisequence-table.md) e [nella tabella InstallExecuteSequence](installexecutesequence-table.md). Questa azione deve essere eseguita dopo [l'azione CostInitialize](costinitialize-action.md) e prima [dell'azione CostFinalize](costfinalize-action.md).

## <a name="actiondata-messages"></a>Messaggi ActionData

Non sono presenti messaggi ActionData.

## <a name="remarks"></a>Commenti

Se la colonna Condizione per l'azione IsolateComponents restituisce True o viene lasciata vuota, il programma di installazione isola tutti i componenti elencati nella [tabella IsolatedComponent](isolatedcomponent-table.md). Se la colonna Condizione restituisce False, il programma di installazione ignora la tabella IsolatedComponent e condivide i componenti consueti. La [**proprietà RedirectedDllSupport**](redirecteddllsupport.md) può essere usata per condizionare questa azione. Per altre informazioni, vedere [Uso di una tabella di sequenza](using-a-sequence-table.md).

 

 



