---
description: Utilizzare la procedura seguente per eseguire il debug di esperti scritti in Microsoft Visual C++.
ms.assetid: 7356fcae-3cfe-4a5b-86dd-bebee859fa19
title: Debug di un esperto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1a7e6b3998eb18d3ea9c5ef25600a6fc08f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314177"
---
# <a name="debugging-an-expert"></a>Debug di un esperto

Utilizzare la procedura seguente per eseguire il debug di esperti scritti in Microsoft Visual C++.

**Debug di un esperto**

1.  Installare l'esperto (file DLL) e il file di database di programma (con estensione pdb) generato durante la compilazione dell'esperto nella posizione corretta. Per ulteriori informazioni, vedere [installazione di un esperto in Network Monitor 2,1](installing-an-expert-to-network-monitor-2-1.md).
2.  Avviare Microsoft Visual C++.
3.  Scegliere **Apri** dal menu **file** e selezionare il nome della DLL di esperti.
4.  Al termine del caricamento di Microsoft Visual C++, fare clic sul menu **progetto** , quindi su **Impostazioni**.
5.  Fare clic su **debug**. In **eseguibile per sessione di debug** Digitare il percorso completo di Netmon.exe, ad esempio:

    ``` syntax
    C:\Program files\Netmon2\Netmon.exe
    ```

6.  Impostare i punti di interruzione nel codice.

 

 



