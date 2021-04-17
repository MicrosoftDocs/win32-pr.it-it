---
title: DPI elevato per le app desktop in Windows 8.1
description: DPI elevato per le app desktop in Windows 8.1
ms.assetid: 1E92D3C8-C117-463A-AF31-12D3CAA31E2A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6c223e9dc39cda9a109280926a5eb47a8fffcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300054"
---
# <a name="high-dpi-for-desktop-apps-in-windows-81"></a>DPI elevato per le app desktop in Windows 8.1

## <a name="platforms"></a>Piattaforme

<dl> Client-Windows 8.1  
Server-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrizione

In Windows 8.1 le applicazioni desktop dovrebbero essere eseguite su schermi con scalabilità del 200% oltre alla scalabilità 100%, 125% e 150% supportata in Windows 8. Inoltre, le applicazioni desktop vengono ridimensionate in base al monitoraggio anziché a un singolo fattore di scala applicato a tutte le visualizzazioni. Gli sviluppatori possono anche chiamare le nuove API in Windows 8.1 per ottenere i fattori di scala per monitoraggio.

## <a name="manifestations"></a>Manifestazioni

Gli utenti possono usare nuovi schermi ad alta densità con Windows 8.1 per un'esperienza visiva eccezionale che sfrutta i vantaggi dei dati pixel più elevati. Se le applicazioni non gestiscono valori DPI alti, Windows ne eseguirà la scalabilità per l'utente. Inoltre, gli utenti possono usare una combinazione di schermi ad alta e bassa densità sullo stesso computer e Windows ridimensiona il contenuto in modo appropriato per ogni visualizzazione. Si tratta di un miglioramento rispetto a Windows 8, in cui il contenuto può essere troppo grande in alcune visualizzazioni.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Poiché Windows ridimensiona le app che non si ridimensionano, gli sviluppatori in genere non sono in grado di eseguire altre attività, ma gli sviluppatori che investono nella scrittura di applicazioni che supportano valori DPI elevati avranno un vantaggio competitivo, dal momento che tali applicazioni avranno un aspetto migliore sui nuovi computer con DPI e i monitor desktop a risoluzione elevata.

## <a name="solution"></a>Soluzione

La creazione di un'applicazione in grado di sfruttare i vantaggi di DPI elevati è un'attività di progettazione e implementazione complessa. Vedere i collegamenti seguenti per informazioni sull'esercitazione, compilare contenuto della presentazione e supporto analogo.

## <a name="tests"></a>Test

Anche se gli sviluppatori non scelgono di sfruttare i vantaggi del valore DPI elevato, devono testare l'applicazione in base al 100%, al 125%, al 150% e al 200% di ridimensionamento per assicurarsi che l'esperienza dell'utente finale sia soddisfacente e competitiva.

## <a name="resources"></a>Risorse

-   [White paper e Esercitazione su DPI alti in Windows 8.1](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   [Programmi di esempio per desktop Windows](https://www.microsoft.com/?ref=go)
-   [COMPILAZIONE della sessione di break-out 2013 su DPI elevato in Windows 8.1](https://channel9.msdn.com/Events/Build/2013/4-184)

 

 