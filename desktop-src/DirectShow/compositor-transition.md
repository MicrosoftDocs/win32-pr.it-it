---
description: Transizione del Compositor
ms.assetid: 7903ecd7-88fb-4277-82ee-a7f71cae0412
title: Transizione del Compositor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75488e9dbdea4926c515f52352b42f68a2bfa679
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104551979"
---
# <a name="compositor-transition"></a>Transizione del Compositor

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

La transizione del Compositor compone un sottorettangolo dal primo piano in un rettangolo designato in background, senza alterare il resto dello sfondo. Usare questa transizione per creare effetti a schermata doppia o immagine in immagine.

Nell'immagine seguente viene illustrata la transizione del Compositor:

![transizione del Compositor](images/trans-compositor.png)

ID classe (CLSID): {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}

Nome variabile CLSID: CLSID \_ DxtCompositor

Nome descrittivo: "DxtCompositor"

Proprietà



| Proprietà   | Type | Predefinito | Descrizione                                                    |
|------------|------|---------|----------------------------------------------------------------|
| Altezza     | long | 0       | Altezza, in pixel, del rettangolo di destinazione.                     |
| OffsetX    | long | 0       | Offset orizzontale del rettangolo di destinazione, espresso in pixel.          |
| OffsetY    | long | 0       | Offset verticale del rettangolo di destinazione, espresso in pixel.            |
| SrcHeight  | long | 0       | Altezza del sottorettangolo sull'origine, in pixel.       |
| SrcOffsetX | long | 0       | Coordinata x del sottorettangolo sull'origine, espressa in pixel. |
| SrcOffsetY | long | 0       | Coordinata y del sottorettangolo sull'origine, espressa in pixel. |
| SrcWidth   | long | 0       | Larghezza del sottorettangolo sull'origine, in pixel.        |
| Larghezza      | long | 0       | Larghezza, in pixel, del rettangolo di destinazione.                      |



 

Nel diagramma seguente vengono illustrate queste proprietà:

![Proprietà compositor](images/compmeasure.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Transizioni ed effetti](transitions-and-effects.md)
</dt> </dl>

 

 



