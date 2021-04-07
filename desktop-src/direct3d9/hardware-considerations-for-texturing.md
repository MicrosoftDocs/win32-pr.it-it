---
description: L'hardware corrente non implementa necessariamente tutte le funzionalità abilitate dall'interfaccia Direct3D. L'applicazione deve testare l'hardware dell'utente e modificare di conseguenza le strategie di rendering.
ms.assetid: 7b5f586c-616c-4351-b6b9-5c0179db5d8b
title: Considerazioni sull'hardware per la funzionalità di texturing (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f1ba8bea85cc3657478767aac7c7ffc2abebbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103875897"
---
# <a name="hardware-considerations-for-texturing-direct3d-9"></a>Considerazioni sull'hardware per la funzionalità di texturing (Direct3D 9)

L'hardware corrente non implementa necessariamente tutte le funzionalità abilitate dall'interfaccia Direct3D. L'applicazione deve testare l'hardware dell'utente e modificare di conseguenza le strategie di rendering.

Molte schede di accelerazione 3D non supportano i valori di iterazione diffusi come argomenti per la fusione di unità. Tuttavia, l'applicazione può introdurre dati di colore iterati quando esegue la fusione di trame.

Alcuni componenti hardware 3D potrebbero non avere una fase di fusione associata alla prima trama. In questi adapter, l'applicazione deve eseguire la fusione nella seconda e terza fase della trama nel set di trame correnti.

A causa delle limitazioni della maggior parte dell'hardware odierno, poche schede video possono eseguire l'interpolazione trilineare mipmap tramite l'interfaccia di combinazione di più trame offerta da [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9). L'applicazione può usare la combinazione di trame MultiPASS per ottenere gli stessi effetti o per ridurre la \_ modalità di filtro mipmap del punto D3DTEXF, che è ampiamente supportata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
