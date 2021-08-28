---
description: Transizione Compositor
ms.assetid: 7903ecd7-88fb-4277-82ee-a7f71cae0412
title: Transizione Compositor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 763194308ea01a31e132aebccdfca84f06dae56e9c01b47c689b03215cdb2698
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084296"
---
# <a name="compositor-transition"></a>Transizione Compositor

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

La transizione Compositor composita un sottorettangolo dal primo piano in un rettangolo designato sullo sfondo, senza modificare il resto dello sfondo. Usare questa transizione per creare effetti a schermo diviso o da immagine in immagine.

L'immagine seguente mostra la transizione compositor:

![transizione compositor](images/trans-compositor.png)

ID classe (CLSID): {BB44391D-6ABD-422f-9E2E-385C9DFF51FC}

Nome variabile CLSID: CLSID \_ DxtCompositor

Nome descrittivo: "DxtCompositor"

Proprietà



| Proprietà   | Type | Predefinito | Descrizione                                                    |
|------------|------|---------|----------------------------------------------------------------|
| Altezza     | long | 0       | Altezza del rettangolo di destinazione, in pixel.                     |
| OffsetX    | long | 0       | Offset orizzontale del rettangolo di destinazione, in pixel.          |
| OffsetY    | long | 0       | Offset verticale del rettangolo di destinazione, in pixel.            |
| SrcHeight  | long | 0       | Altezza del sottorettangolo sull'origine, in pixel.       |
| SrcOffsetX | long | 0       | Coordinata x del sottorettangolo sull'origine, in pixel. |
| SrcOffsetY | long | 0       | Coordinata y del sottorettangolo sull'origine, in pixel. |
| SrcWidth   | long | 0       | Larghezza del sottorettangolo nell'origine, in pixel.        |
| Larghezza      | long | 0       | Larghezza del rettangolo di destinazione, in pixel.                      |



 

Il diagramma seguente illustra queste proprietà:

![Proprietà compositor](images/compmeasure.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Transizioni ed effetti](transitions-and-effects.md)
</dt> </dl>

 

 



