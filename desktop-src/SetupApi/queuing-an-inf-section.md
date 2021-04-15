---
description: Oltre ad accodare singolarmente le operazioni sui file, è anche possibile accodare tutti i file elencati in una sezione INF.
ms.assetid: 456e1a19-7e9b-40c8-9295-42bb8f740f58
title: Accodamento di una sezione INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5566931131885cf6f300b5a6386639bbd564e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529778"
---
# <a name="queuing-an-inf-section"></a>Accodamento di una sezione INF

Oltre ad accodare singolarmente le operazioni sui file, è anche possibile accodare tutti i file elencati in una sezione INF.

È possibile accodare tutti i file elencati in una sezione **copia file** di un file inf chiamando [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona). Affinché questa funzione abbia esito positivo, la sezione **copia file** deve essere nel formato corretto e il file inf, o uno dei file accodati, deve contenere le sezioni **SourceDisksFiles** e **SourceDisksNames** .

Analogamente, se si desidera eliminare tutti i file specificati in una sezione dei file di **eliminazione** di un file inf, è possibile chiamare [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona). Per rinominare tutti i file in una sezione **Rinomina file** di un file inf, usare [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).

 

 



