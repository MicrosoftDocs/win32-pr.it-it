---
description: Direzione della transizione
ms.assetid: d18525de-bb75-4c5e-b387-cfec7ba03df7
title: Direzione della transizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2097f13225c7691780646d77a18d048a48e31eda498955bdc53a0c954728c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951495"
---
# <a name="transition-direction"></a>Direzione della transizione

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Una transizione passa dall'input A all'input B e da t₀ a t₁. Di conseguenza, *la direzione* di una transizione può significare una delle due cose seguenti:

-   Mapping dei livelli della sequenza temporale agli input.
-   Progressione nel tempo.

Il primo è la direzione *di input* e il secondo è la direzione dello stato di *avanzamento.* È possibile controllare entrambe le direzioni.

-   Direzione di input: per impostazione predefinita, una transizione passa dal composito dei livelli con priorità inferiore al livello che contiene la transizione. Per invertire questa direzione, chiamare il [**metodo IAMTimelineTrans::SetSwapInputs.**](iamtimelinetrans-setswapinputs.md)
-   Direzione dello stato: la maggior parte delle transizioni supporta una proprietà **Progress** standard, che specifica la percentuale della transizione riflessa nell'output in un determinato momento. Per impostazione predefinita, il valore della proprietà **Progress** va da 0,0 a 1,0 per la durata della transizione. Per invertire lo stato di avanzamento, impostare la **proprietà Progress** in modo che passi da 1.0 a 0.0.

Il diagramma seguente illustra la differenza tra la direzione di input e la direzione di avanzamento. Mostra quattro varianti in una transizione [di cancellazione SMPTE](smpte-wipe-transition.md) standard.

![cancellare le indicazioni](images/wipedirections.png)

La transizione si trova sulla traccia 1. Per impostazione predefinita, la cancellazione va da sinistra a destra e dalla traccia 0 alla traccia 1. Lo scambio di input fa sì che la cancellazione passa dalla traccia 1 alla traccia 0, ma da sinistra a destra. Invertindo lo stato di avanzamento, la transizione passa da destra a sinistra. È possibile combinare entrambe le combinazioni, come illustrato all'estrema sinistra.

Per altre informazioni sul modo in cui DES esegue il rendering delle transizioni, vedere [Il modello di sequenza temporale](the-timeline-model.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di effetti e transizioni](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



