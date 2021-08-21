---
description: IgnoreChange ControlEvent viene pubblicato dal controllo DirectoryList quando la cartella selezionata viene modificata da una directory a un'altra nel controllo. Questo evento deve essere creato nella tabella EventMapping.
ms.assetid: 4d3128a1-cbe3-457c-83b5-8f6ec1a7ba29
title: IgnoreChange ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8efc2750c4d1e2bd85f7c31348f507917f828725de95658095e964b22a110a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634459"
---
# <a name="ignorechange-controlevent"></a>IgnoreChange ControlEvent

IgnoreChange ControlEvent viene pubblicato dal [controllo DirectoryList](directorylist-control.md) quando la cartella selezionata viene modificata da una directory a un'altra nel controllo. Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia utente [*ridotta o*](r-gly.md) un'interfaccia utente [*di base.*](b-gly.md) Per informazioni, vedere [Interfaccia utente Levels.](user-interface-levels.md)

## <a name="published-by"></a>Pubblicato da

[Elenco directory](directorylist-control.md)

## <a name="argument"></a>Argomento

Questo ControlEvent non usa un argomento .

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Il [controllo DirectoryCombo usa](directorycombo-control.md) in genere IgnoreChange ControlEvent.

 

 



