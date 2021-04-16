---
description: Direzione della transizione
ms.assetid: d18525de-bb75-4c5e-b387-cfec7ba03df7
title: Direzione della transizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d43ec4258d2f23c8b8961e3e1b8fd3d554b057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104566292"
---
# <a name="transition-direction"></a>Direzione della transizione

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Una transizione passa da input a a input B e da Time t ₀ a t ₁. Pertanto, la *direzione* di una transizione può indicare uno dei due elementi seguenti:

-   Mapping dei livelli della sequenza temporale agli input.
-   Progressione nel tempo.

Il primo è la *direzione di input* e il secondo è la *direzione di avanzamento*. È possibile controllare entrambe le direzioni.

-   Direzione di input: per impostazione predefinita, una transizione passa dalla composizione dei livelli di priorità inferiore al livello che contiene la transizione. Per invertire questa direzione, chiamare il metodo [**IAMTimelineTrans:: SetSwapInputs**](iamtimelinetrans-setswapinputs.md) .
-   Direzione avanzamento: la maggior parte delle transizioni supporta una proprietà di **stato** standard, che specifica la percentuale della transizione che viene riflessa nell'output in un determinato momento. Per impostazione predefinita, il valore della proprietà **Progress** passa da 0,0 a 1,0 per la durata della transizione. Per invertire lo stato di avanzamento, impostare la proprietà **stato** su vai da 1,0 a 0,0.

Il diagramma seguente illustra la differenza tra direzione di input e direzione di avanzamento. Vengono mostrate quattro variazioni in una transizione standard di [cancellazione SMPTE](smpte-wipe-transition.md) .

![Cancella direzioni](images/wipedirections.png)

La transizione si trova nella traccia 1. Per impostazione predefinita, la cancellazione passa da sinistra a destra e da Track 0 a Track 1. Lo scambio degli input causa la cancellazione della cancellazione dalla traccia 1 alla traccia 0, ma ancora da sinistra verso destra. Invertendo lo stato, la transizione va da destra a sinistra. È possibile combinare entrambi, come illustrato all'estrema sinistra.

Per ulteriori informazioni sul rendering delle transizioni DES, vedere [il modello di sequenza temporale](the-timeline-model.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo degli effetti e delle transizioni](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



