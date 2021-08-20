---
title: Valori DPI alti per le app desktop in Windows 8.1
description: Valori DPI alti per le app desktop in Windows 8.1
ms.assetid: 1E92D3C8-C117-463A-AF31-12D3CAA31E2A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbef80ce11de41ca50b7cf5ce4076b294b9331b62be417686f7ba0a3a63b98dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852427"
---
# <a name="high-dpi-for-desktop-apps-in-windows-81"></a>Valori DPI alti per le app desktop in Windows 8.1

## <a name="platforms"></a>Piattaforme

<dl> Client - Windows 8.1  
Server - Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrizione

In Windows 8.1 è previsto che le applicazioni desktop siano eseguite su schermi con scalabilità del 200%, oltre al 100%, al 125% e al 150% supportato in Windows 8. Inoltre, le applicazioni desktop vengono ridimensionate in base al monitor anziché a un singolo fattore di scala applicato a tutti i monitor. Gli sviluppatori possono anche chiamare nuove API in Windows 8.1 per ottenere fattori di scala per monitor.

## <a name="manifestations"></a>Manifestazioni

Gli utenti possono usare nuovi schermi ad alta densità con Windows 8.1 per un'esperienza visiva eccezionale che sfrutta i dati pixel più elevati. Se le applicazioni non gestiscono valori DPI elevati, Windows scalabilità per l'utente. Inoltre, gli utenti possono usare una combinazione di schermi ad alta e bassa densità nello stesso computer e Windows il contenuto verrà ridimensionato in modo appropriato per ogni schermo. Si tratta di un miglioramento rispetto Windows 8, in cui il contenuto può essere troppo grande in alcuni schermi.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Poiché Windows ridimensiona le app che non si ridimensionano, gli sviluppatori in genere non devono eseguire operazioni aggiuntive, ma gli sviluppatori che investono nella scrittura di applicazioni che supportano valori DPI elevati avranno un vantaggio competitivo, perché queste applicazioni avranno un aspetto migliore sui nuovi portatili con valori DPI alti e sui monitor desktop.

## <a name="solution"></a>Soluzione

Creare un'applicazione in grado di sfruttare valori DPI elevati è un'attività di progettazione e implementazione complessa. Vedere i collegamenti seguenti per informazioni sull'esercitazione, il contenuto della presentazione BUILD e un supporto simile.

## <a name="tests"></a>Test

Anche se gli sviluppatori non scelgono di sfruttare il valore DPI elevato per le proprie applicazioni, devono testare l'applicazione al 100%, al 125%, al 150% e al 200% per assicurarsi che l'esperienza dell'utente finale sia soddisfacente e competitivo.

## <a name="resources"></a>Risorse

-   [White paper ed esercitazione su valori DPI elevati in Windows 8.1](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   [Windows di esempio desktop](https://www.microsoft.com/?ref=go)
-   [Build 2013 break-out session on high DPI in Windows 8.1](https://channel9.msdn.com/Events/Build/2013/4-184)

 

 