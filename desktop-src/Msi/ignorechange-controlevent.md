---
description: Il ControlEvent IgnoreChange viene pubblicato dal controllo Directory quando la cartella selezionata viene modificata da una directory a un'altra nel controllo. Questo evento deve essere creato nella tabella EventMapping.
ms.assetid: 4d3128a1-cbe3-457c-83b5-8f6ec1a7ba29
title: ControlEvent IgnoreChange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db909552e97f29b8ebcd9d58ac8688474788ec0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310975"
---
# <a name="ignorechange-controlevent"></a>ControlEvent IgnoreChange

Il ControlEvent IgnoreChange viene pubblicato dal [controllo Directory](directorylist-control.md) quando la cartella selezionata viene modificata da una directory a un'altra nel controllo. Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

[Elenco di directory](directorylist-control.md)

## <a name="argument"></a>Argomento

Questo ControlEvent non usa un argomento.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Il [controllo DirectoryCombo](directorycombo-control.md) USA in genere il IgnoreChange ControlEvent.

 

 



