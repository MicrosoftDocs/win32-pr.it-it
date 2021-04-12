---
title: Elaborazione di un set di risultati
description: Un set di risultati viene restituito come una serie di righe.
ms.assetid: e0949c1c-a31a-440a-ae10-2934ffeb7128
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ad422494fd2d384b612989e9e36cec7110e021
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339230"
---
# <a name="processing-a-result-set"></a>Elaborazione di un set di risultati

Un set di risultati viene restituito come una serie di righe. Ogni riga può contenere o meno un attributo specificato. Con il provider di OLE DB, il set di risultati viene visualizzato in modo analogo a un set di risultati SQL normale. Se si usa ADO per la query, [ADODB. ](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) L'oggetto recordset viene utilizzato per attraversare il set di risultati. [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (disponibile solo da linguaggi che supportano le associazioni vtable) contiene membri per lo spazio dei cursori di riga e il controllo dei valori delle proprietà in una determinata riga. In alternativa, è possibile usare [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) per ottenere e impostare le proprietà.

 

 