---
title: Panoramica dell'architettura grafica di Windows
description: Descrive le API grafiche C++/COM in Windows.
ms.assetid: 9654b18b-d615-455d-a92a-6fc2ccda469e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45ba44f54b947d923b888d51080ff0335119a1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "104132130"
---
# <a name="overview-of-the-windows-graphics-architecture"></a>Panoramica dell'architettura grafica di Windows

Windows offre diverse API C++/COM per la grafica. Queste API sono illustrate nella figura seguente.

![diagramma che mostra le API grafiche di Windows.](images/graphics01.png)

-   Graphics Device Interface (GDI) è l'interfaccia grafica originale per Windows. GDI è stato scritto per la prima volta in Windows a 16 bit, quindi è stato aggiornato per Windows a 32 bit e a 64 bit.
-   GDI+ è stato introdotto in Windows XP come successore per GDI. È possibile accedere alla libreria GDI+ tramite un set di classi C++ che esegue il wrapping delle funzioni C flat. Il .NET Framework fornisce inoltre una versione gestita di GDI+ nello spazio dei nomi **System. Drawing** .
-   Direct3D supporta la grafica 3D.
-   Direct2D è un'API moderna per la grafica 2D, il successore sia in GDI che in GDI+.
-   DirectWrite è un motore di rasterizzazione e layout di testo. Per creare il testo rasterizzato, è possibile utilizzare GDI o Direct2D.
-   DirectX Graphics Infrastructure (DXGI) esegue attività di basso livello, ad esempio la presentazione di frame per l'output. La maggior parte delle applicazioni non usa direttamente DXGI. Piuttosto, funge da livello intermedio tra il driver di grafica e Direct3D.

Direct2D e DirectWrite sono stati introdotti in Windows 7. Sono disponibili anche per Windows Vista e Windows Server 2008 tramite un aggiornamento della piattaforma. Per ulteriori informazioni, vedere [aggiornamento della piattaforma per Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).

Direct2D è l'obiettivo di questo modulo. Anche se GDI e GDI+ continuano a essere supportati in Windows, è consigliabile usare Direct2D e DirectWrite per i nuovi programmi. In alcuni casi, una combinazione di tecnologie potrebbe essere più pratica. Per queste situazioni, Direct2D e DirectWrite sono progettati per interagire con GDI.

Nelle sezioni successive vengono descritti alcuni dei vantaggi di Direct2D.

### <a name="hardware-acceleration"></a>Accelerazione hardware

Il termine *accelerazione hardware* si riferisce ai calcoli grafici eseguiti dalla GPU (Graphics Processing Unit), anziché dalla CPU. Le GPU moderne sono altamente ottimizzate per i tipi di calcolo utilizzati per il rendering della grafica. In generale, maggiore è il lavoro che viene spostato dalla CPU alla GPU, migliore sarà.

Sebbene GDI supporti l'accelerazione hardware per determinate operazioni, molte operazioni GDI sono associate alla CPU. Direct2D è sovrapposto a Direct3D e sfrutta al massimo l'accelerazione hardware fornita dalla GPU. Se la GPU non supporta le funzionalità necessarie per Direct2D, Direct2D esegue il fallback al rendering del software. In generale, Direct2D supera le prestazioni GDI e GDI+ nella maggior parte dei casi.

### <a name="transparency-and-anti-aliasing"></a>Trasparenza e anti-aliasing

Direct2D supporta la fusione alfa (trasparenza) completamente accelerata dall'hardware.

GDI ha un supporto limitato per la fusione alfa. La maggior parte delle funzioni GDI non supporta la fusione alfa, sebbene GDI supporti la fusione alfa durante un'operazione BitBlt. GDI+ supporta la trasparenza, ma la fusione alfa viene eseguita dalla CPU, quindi non trae vantaggio dall'accelerazione hardware.

La fusione alfa con accelerazione hardware consente anche l'anti-aliasing. L' *aliasing* è un artefatto causato dal campionamento di una funzione continua. Ad esempio, quando una linea curva viene convertita in pixel, l'aliasing può causare un aspetto irregolare. \[ 3 \] qualsiasi tecnica che riduce gli artefatti causati dall'aliasing è considerata una forma di anti-aliasing. In grafica, l'anti-aliasing viene eseguito fondendo i bordi con lo sfondo. Ecco ad esempio un cerchio disegnato da GDI e lo stesso cerchio disegnato da Direct2D.

![illustrazione delle tecniche di anti-aliasing in Direct2D.](images/graphics02.png)

L'immagine successiva mostra un dettaglio di ogni cerchio.

![dettaglio dell'immagine precedente.](images/graphics03.png)

Il cerchio disegnato da GDI (a sinistra) è costituito da pixel neri che approssimano una curva. Il cerchio disegnato da Direct2D (Right) usa la fusione per creare una curva più liscia.

GDI non supporta l'anti-aliasing quando disegna la geometria (linee e curve). GDI può creare testo con anti-aliasing utilizzando ClearType; in caso contrario, viene anche utilizzato un alias per il testo GDI. L'aliasing è particolarmente evidente per il testo, perché le righe frastagliate interrompono la progettazione del tipo di carattere, rendendo il testo meno leggibile. Sebbene GDI+ supporti l'anti-aliasing, viene applicato dalla CPU, pertanto le prestazioni non sono altrettanto valide di Direct2D.

### <a name="vector-graphics"></a>Grafica vettoriale

Direct2D supporta la *grafica vettoriale*. Nella grafica vettoriale le formule matematiche vengono usate per rappresentare linee e curve. Queste formule non dipendono dalla risoluzione dello schermo, quindi possono essere ridimensionate a dimensioni arbitrarie. La grafica vettoriale è particolarmente utile quando è necessario ridimensionare un'immagine per supportare diverse dimensioni di monitoraggio o risoluzioni dello schermo.

## <a name="next"></a>Prossima

[Gestione finestre desktop](the-desktop-window-manager.md)

 

 
