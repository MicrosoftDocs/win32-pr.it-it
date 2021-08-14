---
description: L'hardware corrente non implementa necessariamente tutte le funzionalità abilitate dall'interfaccia Direct3D. L'applicazione deve testare l'hardware dell'utente e modificare le strategie di rendering di conseguenza.
ms.assetid: 7b5f586c-616c-4351-b6b9-5c0179db5d8b
title: Considerazioni sull'hardware per la texturing (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41344d1ee091a1d2d619e366de549d58b69aebf234b89b6cf8115511703b799
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522802"
---
# <a name="hardware-considerations-for-texturing-direct3d-9"></a>Considerazioni sull'hardware per la texturing (Direct3D 9)

L'hardware corrente non implementa necessariamente tutte le funzionalità abilitate dall'interfaccia Direct3D. L'applicazione deve testare l'hardware dell'utente e modificare le strategie di rendering di conseguenza.

Molte schede di acceleratore 3D non supportano valori iterato diffusi come argomenti per le unità di fusione. Tuttavia, l'applicazione può introdurre dati di colore iterato quando esegue la fusione delle trame.

Alcuni componenti hardware 3D potrebbero non avere una fase di fusione associata alla prima trama. Su questi adattatori, l'applicazione deve eseguire la fusione nella seconda e nella terza fase della trama nel set di trame correnti.

A causa delle limitazioni nella maggior parte dell'hardware attuale, poche schede di visualizzazione possono eseguire l'interpolazione mipmap trilineare tramite l'interfaccia di fusione di più trame offerta da [**IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) L'applicazione può usare la fusione di trame multipass per ottenere gli stessi effetti o ridurre il livello alla modalità di filtro mipmap D3DTEXF POINT, ampiamente \_ supportata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
