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
# <a name="processing-a-result-set"></a><span data-ttu-id="128ba-103">Elaborazione di un set di risultati</span><span class="sxs-lookup"><span data-stu-id="128ba-103">Processing a Result Set</span></span>

<span data-ttu-id="128ba-104">Un set di risultati viene restituito come una serie di righe.</span><span class="sxs-lookup"><span data-stu-id="128ba-104">A result set is returned as a series of rows.</span></span> <span data-ttu-id="128ba-105">Ogni riga può contenere o meno un attributo specificato.</span><span class="sxs-lookup"><span data-stu-id="128ba-105">Each row may or may not contain a given attribute.</span></span> <span data-ttu-id="128ba-106">Con il provider di OLE DB, il set di risultati viene visualizzato in modo analogo a un set di risultati SQL normale.</span><span class="sxs-lookup"><span data-stu-id="128ba-106">With the OLE DB provider, the result set appears similar to a normal SQL result set.</span></span> <span data-ttu-id="128ba-107">Se si usa ADO per la query, [ADODB. ](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) L'oggetto recordset viene utilizzato per attraversare il set di risultati.</span><span class="sxs-lookup"><span data-stu-id="128ba-107">If you use ADO for the query, the [ADODB.Recordset](/sql/ado/reference/ado-api/recordset-object-ado?view=sql-server-ver15) object is used for traversing the result set.</span></span> <span data-ttu-id="128ba-108">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (disponibile solo da linguaggi che supportano le associazioni vtable) contiene membri per lo spazio dei cursori di riga e il controllo dei valori delle proprietà in una determinata riga.</span><span class="sxs-lookup"><span data-stu-id="128ba-108">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) (available only from languages that support vtable bindings) contains members for moving the row cursor and checking property values in a given row.</span></span> <span data-ttu-id="128ba-109">In alternativa, è possibile usare [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) per ottenere e impostare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="128ba-109">Alternatively, you can use [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) to get and set properties.</span></span>

 

 