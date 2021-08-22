---
description: La procedura seguente illustra come eseguire il debug di un monitoraggio.
ms.assetid: 499f409c-e25a-4ab3-b0aa-e6b308fc7169
title: Debug di un monitoraggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7ce15252470b280a988f81fe221218778a0fa5e4851db0d3e419d1653fbe92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144204"
---
# <a name="debugging-a-monitor"></a>Debug di un monitoraggio

La procedura seguente illustra come eseguire il debug di un monitoraggio.

**Per eseguire il debug di un monitoraggio**

1.  Installare la DLL di monitoraggio e il file del database di programma (con estensione pdb) generato durante la compilazione del monitoraggio nel percorso corretto. Per [altri dettagli, vedere Installing a Monitor to Network Monitor](installing-a-monitor-to-network-monitor.md) (Installazione di un monitoraggio Network Monitor per altri dettagli).
2.  Verificare che il servizio di controllo monitoraggio sia configurato come server anziché come servizio selezionando Pannello di controllo, Servizi.
3.  Aprire un prompt dei comandi e passare alla directory Network Monitor. Digitare:

    **Mcsvc.exe /RegServer**

    Al termine della sessione di debug del monitoraggio, è possibile ripristinare la condizione predefinita di MCSVC digitando:

    **Mcsvc.exe /Service**

4.  In Microsoft Visual Studio avviare Microsoft Visual C++.
5.  Dall'opzione di **menu** **File**, Apri selezionare il nome della DLL di monitoraggio.
6.  Dopo Microsoft Visual C++ caricamento, fare clic **su Project**, **Impostazioni**.
7.  Fare clic **sulla scheda Debug** in **Eseguibile** per la sessione di debug e digitare il percorso completo Mcsvc.exe. Ad esempio, C: \\ Programmi \\ Netmon2 \\Mcsvc.exe.
8.  Impostare i punti di interruzione nel codice.

> [!Note]  
> Non usare una finestra di messaggio per monitorare il debug. Se MCSVC è in esecuzione come servizio, la finestra popup non verrà visualizzata e MCSVC verrà bloccato.

 

 

 



