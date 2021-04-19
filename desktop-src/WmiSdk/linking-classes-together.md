---
description: I provider WMI sono in genere progettati per fornire informazioni su un oggetto gestito specifico in un singolo computer.
ms.assetid: 9f23d599-ac37-4bfb-a3dc-0cef67e68b05
ms.tgt_platform: multiple
title: Collegamento di classi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c36956d20d9390462577332e7ac7b644d4ffc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317551"
---
# <a name="linking-classes-together"></a>Collegamento di classi

I provider WMI sono in genere progettati per fornire informazioni su un oggetto gestito specifico in un singolo computer. Se è presente una proprietà comune che può fungere da chiave per identificare in modo univoco tutte le istanze di origine diverse, utilizzare il [provider di visualizzazione](view-provider.md) per combinare le proprietà di classi, spazi dei nomi o computer diversi in una singola classe.

È necessario prima [registrare il provider di visualizzazione](registering-the-view-provider.md). Dopo la registrazione, è possibile creare i seguenti tipi di classi di visualizzazione:

-   [Visualizzazione join](creating-a-new-instance-from-old-properties.md)

    Istanze di classi diverse connesse da un valore di proprietà comune.

-   [Visualizzazione associazione](associating-instances-between-namespaces.md)

    Viste delle classi di associazione esistenti attraverso il limite dello spazio dei nomi.

-   [Visualizzazione Unione](creating-a-union-view-class.md)

    Unione di una o più istanze.

 

 



