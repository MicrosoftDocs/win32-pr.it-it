---
description: L'evento SetInstallLevel modifica il livello di installazione sul valore specificato dall'argomento .
ms.assetid: 71cfd516-4a92-446c-bd8f-a3a04dba0bb2
title: Evento di controllo SetInstallLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3e7632e666dc169318e04cbcaf979aa82432d028cc6b7230e6a5e711350ef35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625109"
---
# <a name="setinstalllevel-controlevent"></a>Evento di controllo SetInstallLevel

L'evento SetInstallLevel modifica il livello di installazione sul valore specificato dall'argomento .

Questo evento può essere pubblicato da un [controllo PushButton o](pushbutton-control.md) [selectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia [*utente ridotta*](r-gly.md) o un'interfaccia utente [*di base.*](b-gly.md) Per informazioni, vedere [Livelli Interfaccia utente.](user-interface-levels.md)

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Intero che rappresenta il nuovo valore del livello di installazione.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Nessuno.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo PushButton](pushbutton-control.md) in una finestra di dialogo modale è associato a questo evento nella [tabella ControlEvent](controlevent-table.md) per modificare il livello di installazione.

 

 



