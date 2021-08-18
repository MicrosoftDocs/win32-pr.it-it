---
description: I provider WMI sono in genere progettati per fornire informazioni su un oggetto gestito specifico in un singolo computer.
ms.assetid: 9f23d599-ac37-4bfb-a3dc-0cef67e68b05
ms.tgt_platform: multiple
title: Collegamento di classi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da48ab6b816eece1184915026ca32ed152b896f0555ca6c546d0b8ed4d6a7640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131223"
---
# <a name="linking-classes-together"></a>Collegamento di classi

I provider WMI sono in genere progettati per fornire informazioni su un oggetto gestito specifico in un singolo computer. Se è presente una proprietà comune che può essere utilizzata come chiave per [](view-provider.md) identificare in modo univoco tutte le diverse istanze di origine, usare il provider di visualizzazione per combinare le proprietà di classi, spazi dei nomi o computer diversi in un'unica classe.

È innanzitutto necessario [registrare il provider di visualizzazione](registering-the-view-provider.md). Dopo la registrazione, è possibile creare i tipi di classi di visualizzazione seguenti:

-   [Visualizzazione join](creating-a-new-instance-from-old-properties.md)

    Istanze di classi diverse connesse da un valore di proprietà comune.

-   [Visualizzazione associazione](associating-instances-between-namespaces.md)

    Visualizzazioni delle classi di associazione esistenti attraverso il limite dello spazio dei nomi.

-   [Visualizzazione Unione](creating-a-union-view-class.md)

    Unione di una o più istanze di .

 

 



