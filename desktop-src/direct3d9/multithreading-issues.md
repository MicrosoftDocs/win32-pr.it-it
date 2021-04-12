---
description: Le applicazioni Direct3D a schermo intero forniscono un handle di finestra per la fase di esecuzione di Direct3D.
ms.assetid: 66a9e14f-46c8-45e8-ae0e-4d8cf5106acc
title: Problemi di multithreading (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8d163698e6cc1b4855668d255ed46fd28700d1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401111"
---
# <a name="multithreading-issues-direct3d-9"></a>Problemi di multithreading (Direct3D 9)

Le applicazioni Direct3D a schermo intero forniscono un handle di finestra per la fase di esecuzione di Direct3D. La finestra è agganciata dal runtime. Ciò significa che tutti i messaggi passati alla routine del messaggio della finestra dell'applicazione sono stati prima esaminati dalla procedura di gestione dei messaggi della fase di esecuzione di Direct3D.

Le modifiche alla modalità di visualizzazione sono interessate dalle routine di supporto incorporate nel sistema operativo sottostante. Quando si verificano modifiche alla modalità, il sistema trasmette diversi messaggi a tutte le applicazioni. Nelle applicazioni Direct3D, i messaggi vengono ricevuti nel thread della routine della finestra, che non è necessariamente lo stesso thread che ha chiamato [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) o [**IDirect3D9:: CreateDevice**](/windows/desktop/api) o la versione finale di [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9), che può causare una modifica della modalità di visualizzazione. Il runtime Direct3D mantiene internamente diverse sezioni critiche. Poiché almeno una di queste sezioni critiche viene mantenuta nel commutatore di modalità causato da **IDirect3DDevice9:: Reset** o **IDirect3D9:: CreateDevice**, queste sezioni critiche vengono ancora mantenute quando l'applicazione riceve i messaggi della finestra correlati alla modifica in modalità.

Questa progettazione ha alcune implicazioni per le applicazioni multithreading. In particolare, un'applicazione deve assicurarsi di separare fortemente i thread di gestione dei messaggi della finestra dai relativi thread Direct3D. Un'applicazione che causa una modifica della modalità in un thread ma che esegue chiamate Direct3D su un thread diverso nella relativa routine della finestra è in pericolo di deadlock.

Per questi motivi, Direct3D è progettato in modo che i metodi [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset), [**IDirect3D9:: CreateDevice**](/windows/desktop/api), [**IDirect3DDevice9:: TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)o la versione finale di [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) possano essere chiamati solo dallo stesso thread che gestisce i messaggi della finestra.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Suggerimenti per la programmazione](programming-tips.md)
</dt> </dl>

 

 
