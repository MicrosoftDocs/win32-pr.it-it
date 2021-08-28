---
description: Usare la procedura seguente per eseguire il debug di esperti scritti in Microsoft Visual C++.
ms.assetid: 7356fcae-3cfe-4a5b-86dd-bebee859fa19
title: Debug di un esperto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cdd54484d8dc7d36bf1162433fc98d7d72565d9810c7e0ed838e9193510ac88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064141"
---
# <a name="debugging-an-expert"></a>Debug di un esperto

Usare la procedura seguente per eseguire il debug di esperti scritti in Microsoft Visual C++.

**Debug di un esperto**

1.  Installare l'esperto (file DLL) e il file di database di programma (con estensione pdb) generato quando l'esperto è stato compilato nel percorso corretto. Per altri dettagli, vedere [Installing an Expert to Network Monitor 2.1 (Installazione di un esperto Network Monitor 2.1).](installing-an-expert-to-network-monitor-2-1.md)
2.  Avviare Microsoft Visual C++.
3.  Scegliere **Apri** dal menu File **e** selezionare il nome della DLL esperta.
4.  Dopo Microsoft Visual C++ caricamento, fare clic sul menu **Project** e quindi fare clic **su Impostazioni**.
5.  Fare clic **su Debug**. In **Eseguibile per la sessione di debug** digitare il percorso completo Netmon.exe, ad esempio:

    ``` syntax
    C:\Program files\Netmon2\Netmon.exe
    ```

6.  Impostare i punti di interruzione nel codice.

 

 



