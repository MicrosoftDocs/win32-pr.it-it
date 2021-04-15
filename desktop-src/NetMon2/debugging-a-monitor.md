---
description: Nella procedura seguente viene illustrato come eseguire il debug di un monitoraggio.
ms.assetid: 499f409c-e25a-4ab3-b0aa-e6b308fc7169
title: Debug di un monitoraggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641818b7f1cd1740c2732ced5527a2e278793a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529017"
---
# <a name="debugging-a-monitor"></a>Debug di un monitoraggio

Nella procedura seguente viene illustrato come eseguire il debug di un monitoraggio.

**Per eseguire il debug di un monitoraggio**

1.  Installare la DLL di monitoraggio e il file di database di programma (con estensione pdb) generato al momento della compilazione del monitoraggio nel percorso corretto. Per ulteriori informazioni, vedere [installazione di un monitoraggio per Network Monitor](installing-a-monitor-to-network-monitor.md) .
2.  Verificare che il servizio di controllo di monitoraggio sia configurato come server anziché come servizio selezionando Pannello di controllo, servizi.
3.  Aprire un prompt dei comandi e passare alla directory Network Monitor. Digitare:

    **Mcsvc.exe/RegServer**

    Al termine della sessione di debug del monitoraggio, è possibile ripristinare la condizione predefinita di MCSVC digitando:

    **Mcsvc.exe/Service**

4.  In Microsoft Visual Studio avviare Microsoft Visual C++.
5.  Nel **file** **aprire** l'opzione di menu, quindi selezionare il nome della DLL di monitoraggio.
6.  Dopo il caricamento di Microsoft Visual C++, fare clic su **progetto**, **Impostazioni**.
7.  Fare clic sulla scheda **debug** in **eseguibile** per la sessione di debug e digitare il percorso completo di Mcsvc.exe. Ad esempio, C: \\ Program Files \\ Netmon2 \\Mcsvc.exe.
8.  Impostare i punti di interruzione nel codice.

> [!Note]  
> Non utilizzare una finestra di messaggio per il debug del monitoraggio. Se il MCSVC è in esecuzione come servizio, il popup non verrà visualizzato e MCSVC apparirà in blocco.

 

 

 



