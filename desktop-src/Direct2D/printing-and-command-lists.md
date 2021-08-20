---
title: Elenchi di stampa e comandi
description: Il controllo Direct2D \ 32;print è un nuovo componente nel modulo Direct2D in Windows 8.
ms.assetid: C51ACCDE-B205-4F79-A2FD-D112BAAD1616
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0026071ce8e78fc2ea946e0fffff2993e32ab48a2a20d4de6cdb12ca9b1eaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075050"
---
# <a name="printing-and-command-lists"></a>Elenchi di stampa e comandi

Il [controllo di stampa Direct2D](./direct2d-portal.md) [](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) è un nuovo componente nel modulo Direct2D in Windows 8. Questo componente consente alle app Direct2D di riutilizzare le chiamate di disegno Direct2D (in termini di modifiche dello stato e rendering delle primitive) per fornire risultati di stampa simili a quelli visualizzati sullo schermo.

[**L'interfaccia ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) rappresenta un processo di stampa virtuale: è possibile creare un controllo di stampa [Direct2D](./direct2d-portal.md) per avviare un nuovo processo di stampa, passare il contenuto Direct2D per ogni pagina da stampare, quindi chiudere il controllo di stampa per completare un processo di stampa.

> [!Note]  
> Un controllo di stampa viene mappato a un solo processo di stampa e non è possibile riusarlo.

Il controllo di stampa [Direct2D](./direct2d-portal.md) converte e ottimizza il contenuto Direct2D passato per il sottosistema di stampa, che funziona con le stampanti reali per distribuire la stampa effettiva. Tutti i dettagli specifici della stampa sono nascosti dalle app Direct2D, il che significa che le app Direct2D possono stampare senza conoscere i dispositivi a cui disegnano o il modo in cui i disegni vengono convertiti in stampa.

Per stampare con [Direct2D,](./direct2d-portal.md)è necessario preparare un elenco di comandi Direct2D per ogni pagina da stampare, quindi passare tale elenco di comandi al controllo di stampa Direct2D. Per preparare l'elenco di comandi Direct2D, è sufficiente creare e impostare un elenco di comandi come destinazione di disegno del contesto di dispositivo corrente e quindi disegnare in tale contesto di dispositivo, esattamente come se si disegna su una destinazione bitmap per la visualizzazione. Per [altre informazioni su dispositivi e](devices-and-device-contexts.md) destinazioni, vedere Dispositivi e contesti di dispositivo.

Il diagramma seguente illustra l'interazione tra l'app, il contesto del dispositivo, la destinazione bitmap, la destinazione dell'elenco di comandi e il controllo di stampa.

> [!Note]  
> I Windows stampa Sub-System e Stampante sono in grigio perché sono completamente nascosti dalle [app Direct2D.](./direct2d-portal.md)

![diagramma che illustra l'interazione tra l'elenco comandi e la stampa con un'app e direct2d.](images/d2dprintcontroldiagram.png)

## <a name="example"></a>Esempio

Il processo completo di stampa del contenuto Direct2D include i passaggi seguenti.

1.  Creare un controllo di stampa per avviare un processo di stampa.
2.  Aggiungere una pagina al controllo di stampa passando un elenco di comandi.
3.  Ripetere il passaggio 2 per ogni pagina nel resto del documento
4.  Chiudere il controllo di stampa per completare il processo di stampa.

Ecco un esempio di codice che mostra il processo.

```cpp
ID2D1CommandList* commandList;
// Skip command list creation and drawing for simplicity.

// Set print control properties.
D2D1_PRINT_CONTROL_PROPERTIES printControlProperties;
printControlProperties.rasterDPI = 150.0f; // Use the default rasterization DPI for all unsupported Direct2D commands 
                                                                                                                                                                            //  or options.
printControlProperties.fontSubset = D2D1_PRINT_FONT_SUBSET_MODE_DEFAULT; // Using the default font subset strategy.
printControlProperties.colorSpace = D2D1_COLOR_SPACE_SRGB; // Color space for vector graphics in Direct2D print control.

// Create a Direct2D Print Control to initiate a print job.
ID2D1PrintControl* d2dPrintControl;
d2dDevice->CreatePrintControl(
    wicFactory,
    documentTarget,
    printControlProperties,
    &d2dPrintControl
    );

// Add Direct2D drawing commands encapsulated in a command list.
// You can add in more pages by calling this API multiple times.
d2dPrintControl->AddPage(commandList);

// Close the print control to complete a print job.
d2dPrintControl->Close();
```

## <a name="related-topics"></a>Argomenti correlati

[**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)

[**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)

[Miglioramento delle prestazioni delle applicazioni Direct2D e della stampa](improving-direct2d-performance.md)