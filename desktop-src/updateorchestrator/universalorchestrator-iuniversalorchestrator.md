---
title: Interfaccia IUniversalOrchestrator
description: Interfaccia COM che fornisce metodi per consentire a un client di comunicare con Universal Orchestrator.
ms.date: 01/14/2021
ms.topic: reference
ms.openlocfilehash: f3635f76236eb6c7a11bfa62311003b7d76357a9fbacc9fde85f0bdffed0c129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966139"
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