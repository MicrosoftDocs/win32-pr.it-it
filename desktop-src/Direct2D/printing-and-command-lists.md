---
title: Elenchi di stampa e comandi
description: Direct2D \ 32; il controllo di stampa è un nuovo componente del modulo Direct2D in Windows 8.
ms.assetid: C51ACCDE-B205-4F79-A2FD-D112BAAD1616
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6beb16a24c972016686e2dffe915a947128a63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399148"
---
# <a name="printing-and-command-lists"></a>Elenchi di stampa e comandi

Il [](./direct2d-portal.md) [**controllo di stampa**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) Direct2D è un nuovo componente del modulo Direct2D in Windows 8. Questo componente consente alle app Direct2D di riutilizzare le chiamate di disegno Direct2D (in termini di modifiche di stato e primitive di rendering) per fornire risultati di stampa simili a quelli visualizzati sullo schermo.

L'interfaccia [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) rappresenta un processo di stampa virtuale: è possibile creare un controllo di stampa [Direct2D](./direct2d-portal.md) per avviare un nuovo processo di stampa, passare il contenuto Direct2D per ogni pagina che si desidera stampare, quindi chiudere il controllo di stampa per completare un processo di stampa.

> [!Note]  
> Un controllo di stampa viene mappato a un solo processo di stampa e non può essere riutilizzato.

Il controllo di stampa [Direct2D](./direct2d-portal.md) converte e ottimizza il contenuto Direct2D passato per il sottosistema di stampa, che funziona con le stampanti reali per fornire la stampa effettiva. Tutti i dettagli specifici della stampa sono nascosti dalle app Direct2D, il che significa che le app Direct2D possono stampare senza sapere quali dispositivi stanno disegnando o come i disegni vengono convertiti in stampa.

Per stampare con [Direct2D](./direct2d-portal.md), è necessario preparare un elenco di comandi Direct2D per ogni pagina che si desidera stampare, quindi passare l'elenco dei comandi al controllo di stampa Direct2D. Per preparare l'elenco dei comandi Direct2D, è sufficiente creare e impostare un elenco di comandi come destinazione del disegno del contesto di dispositivo corrente, quindi disegnarlo nel contesto di dispositivo, esattamente come se si sta disegnando in una destinazione bitmap per la visualizzazione. Per altre informazioni su dispositivi e destinazioni, vedere [dispositivi e contesti di dispositivo](devices-and-device-contexts.md) .

Il diagramma seguente illustra l'interazione tra l'app, il contesto di dispositivo, la destinazione bitmap, la destinazione dell'elenco di comandi e il controllo di stampa.

> [!Note]  
> I componenti di stampa Sub-System e stampante di Windows sono in grigio perché sono completamente nascosti dalle app [Direct2D](./direct2d-portal.md) .

![diagramma che mostra il modo in cui il comando e la stampa interagiscono con un'applicazione e Direct2D.](images/d2dprintcontroldiagram.png)

## <a name="example"></a>Esempio

Il processo completo di stampa del contenuto Direct2D include i passaggi seguenti.

1.  Creare un controllo di stampa per avviare un processo di stampa.
2.  Aggiungere una pagina al controllo di stampa passando un elenco di comandi.
3.  Ripetere il passaggio 2 per ogni pagina nel resto del documento
4.  Chiudere il controllo di stampa per completare il processo di stampa.

Di seguito è riportato un esempio di codice che illustra il processo.

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

[Miglioramento delle prestazioni delle applicazioni e della stampa Direct2D](improving-direct2d-performance.md)