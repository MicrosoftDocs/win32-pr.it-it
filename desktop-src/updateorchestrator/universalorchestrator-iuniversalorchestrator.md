---
title: Interfaccia IUniversalOrchestrator
description: Interfaccia COM che fornisce metodi per consentire a un client di comunicare con l'agente di orchestrazione universale.
ms.date: 01/14/2021
ms.topic: interface
ms.openlocfilehash: 6fa5dfd9f7853159645fbe3b543c228450f4e1c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/21/2021
ms.locfileid: "106320073"
---
# <a name="iuniversalorchestrator-interface"></a>Interfaccia IUniversalOrchestrator

> [!NOTE] 
> Questa API appartiene all'API dell'agente di orchestrazione universale.

**IUniversalOrchestrator** è un'interfaccia com che fornisce i metodi seguenti per consentire a un client di comunicare con l'agente di orchestrazione universale.

## <a name="methods"></a>Metodi

|Metodo | Descrizione |
|---|---|
|[:: Pianificazioni](universalorchestrator-schedulework.md) | Registra il lavoro in sospeso con l'agente di orchestrazione universale. |
|[::WorkCompleted](universalorchestrator-workcompleted.md) | Informa l'agente di orchestrazione universale che tutto il lavoro è completo. |
|[::HasMoratoriumPassed](universalorchestrator-hasmoratoriumpassed.md) | Esegue una query sull'agente di orchestrazione universale per determinare se funziona immediatamente dopo la nuova esperienza del dispositivo. |


## <a name="requirements"></a>Requisiti

| Requisito | Versione |
|---|---|
| Client minimo supportato | Windows 10 1903 |
|   |   |