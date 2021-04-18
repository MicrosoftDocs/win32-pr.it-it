---
description: Il controllo SelectionTree usa l'evento SelectionNoItems per eliminare il testo della descrizione dell'elemento obsoleto o per disabilitare i pulsanti che diventano inutili. Questo evento deve essere creato nella tabella EventMapping.
ms.assetid: a79abd77-a6e5-4a1f-8a63-51644151404a
title: ControlEvent SelectionNoItems
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544dfcaad3d22b63d71703ea95d1aa4f09a1efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319431"
---
# <a name="selectionnoitems-controlevent"></a>ControlEvent SelectionNoItems

Il [controllo SelectionTree](selectiontree-control.md) usa l'evento SelectionNoItems per eliminare il testo della descrizione dell'elemento obsoleto o per disabilitare i pulsanti che diventano inutili. Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

Questo evento può influire solo sui controlli che si trovano nella stessa finestra di dialogo del controllo SelectionTree.

## <a name="published-by"></a>Pubblicato da

[SelectionTree controllare](selectiontree-control.md) se la selezione non include nodi.

## <a name="argument"></a>Argomento

Nessuna.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Elimina il testo della descrizione dell'elemento obsoleto o Disabilita i pulsanti obsoleti.

## <a name="typical-use"></a>Utilizzo tipico

Può essere usato per disabilitare i pulsanti Next, reset e DiskCost della finestra di [dialogo di selezione](selection-dialog.md) quando una selezione non contiene nodi e questi pulsanti diventano inutili.

 

 



