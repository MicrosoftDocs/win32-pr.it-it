---
title: Interfaccia IUniversalOrchestrator
description: Interfaccia COM che fornisce metodi per consentire a un client di comunicare con Universal Orchestrator.
ms.date: 01/14/2021
ms.topic: reference
ms.openlocfilehash: 5dbbaafb38ab9d790d32beca9b014f933d5d53d5
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991848"
---
# <a name="iuniversalorchestrator-interface"></a>Interfaccia IUniversalOrchestrator

> [!NOTE] 
> Questa API appartiene all'API Universal Orchestrator.

**IUniversalOrchestrator** è un'interfaccia COM che fornisce i metodi seguenti per consentire a un client di comunicare con Universal Orchestrator.

## <a name="methods"></a>Metodi

|Metodo | Descrizione |
|---|---|
|[::ScheduleWork](universalorchestrator-schedulework.md) | Registra il lavoro in sospeso con Universal Orchestrator. |
|[::WorkCompleted](universalorchestrator-workcompleted.md) | Informa Universal Orchestrator che tutto il lavoro è stato completato. |
|[::HasMoratoriumPassed](universalorchestrator-hasmoratoriumpassed.md) | Esegue una query su Universal Orchestrator per determinare se funziona immediatamente dopo il nuovo dispositivo Out of Box Experience. |


## <a name="requirements"></a>Requisiti

| Requisito | Versione |
|---|---|
| Client minimo supportato | Windows 10 1903 |
|   |   |