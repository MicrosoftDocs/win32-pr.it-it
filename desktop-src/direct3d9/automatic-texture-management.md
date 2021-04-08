---
description: La gestione delle trame è il processo che consente di determinare quali trame sono necessarie per il rendering in un determinato momento e di garantire che tali trame vengano caricate nella memoria video.
ms.assetid: ea6d64ee-f570-49eb-b5fd-67fcde3f8ddc
title: Gestione automatica delle trame (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0eb14eede197661bc127a062229ebed31274ae8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878186"
---
# <a name="automatic-texture-management-direct3d-9"></a>Gestione automatica delle trame (Direct3D 9)

La gestione delle trame è il processo che consente di determinare quali trame sono necessarie per il rendering in un determinato momento e di garantire che tali trame vengano caricate nella memoria video. Come per qualsiasi algoritmo, gli schemi di gestione delle trame variano in complessità, ma qualsiasi approccio alla gestione delle trame comporta le seguenti attività principali.

-   Rilevamento della quantità di memoria di trama disponibile.
-   Calcolo di quali trame sono necessarie per il rendering e quali non lo sono.
-   Determinare le risorse di trama esistenti che è possibile ricaricare con un'altra immagine di trama e quali superfici devono essere distrutte e sostituite con nuove risorse di trama.

Direct3D implementa la gestione delle trame supportata dal sistema per garantire il caricamento delle trame per prestazioni ottimali. Le risorse di trama gestite da Direct3D sono denominate trame gestite.

Il gestore di trame tiene traccia delle trame con un timestamp che identifica la data e l'ora dell'ultimo utilizzo della trama. USA quindi un algoritmo usato meno di recente per determinare quali trame rimuovere. Le priorità di trama vengono usate come interruttori di associazione quando due trame sono destinate alla rimozione dalla memoria. Se due trame hanno lo stesso valore di priorità, la trama usata meno di recente viene rimossa. Tuttavia, se due trame hanno lo stesso timestamp, viene rimossa per prima la trama con una priorità più bassa.

Si richiede la gestione automatica delle trame per le superfici di trama durante la creazione. Per recuperare una trama gestita in un'applicazione C++, creare una risorsa di trama chiamando [**IDirect3DDevice9:: createTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) e specificando la D3DPOOL \_ gestita per il parametro del pool. Non è consentito specificare il percorso in cui si vuole creare la trama. \_ \_ Quando si crea una trama gestita, non è possibile usare i flag D3DPOOL default o D3DPOOL SYSTEMMEM. Dopo aver creato la trama gestita, è possibile chiamare il metodo [**IDirect3DDevice9:: setexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) per impostarlo su una fase nella trama a cascata del dispositivo di rendering.

È possibile assegnare una priorità alle trame gestite chiamando il metodo [**IDirect3DResource9:: sepriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) per la superficie della trama.

Direct3D Scarica automaticamente le trame nella memoria video, in base alle esigenze. Il sistema può memorizzare nella cache le trame gestite nella memoria video locale o non locale, a seconda della disponibilità di memoria video non locale o di altri fattori. Il percorso della cache delle trame gestite non viene comunicato all'applicazione, né queste informazioni sono necessarie per usare la gestione automatica delle trame. Se l'applicazione usa più trame di quanto possa adattarsi alla memoria video, Direct3D rimuove le trame precedenti dalla memoria video per fare spazio alle nuove trame. Se si usa nuovamente una trama rimossa, il sistema usa la superficie di trama della memoria di sistema originale per ricaricare la trama nella cache video-memory. Sebbene il ricaricamento della trama sia necessario, diminuisce anche le prestazioni dell'applicazione.

È possibile modificare dinamicamente la copia di memoria di sistema originale della trama aggiornando o bloccando la risorsa di trama. Quando il sistema rileva una superficie sporca, dopo il completamento di un aggiornamento o quando la superficie è sbloccata, il gestore di trame aggiorna automaticamente la copia della memoria video della trama. L'impatto sulle prestazioni è simile al ricaricamento di una trama rimossa.

Quando si immette un nuovo livello in un gioco, è possibile che l'applicazione debba scaricare tutte le trame gestite dalla memoria video (chiamando [**IDirect3DDevice9:: EvictManagedResources**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-evictmanagedresources)).

Per ulteriori informazioni sulla gestione delle risorse, vedere [gestione delle risorse (Direct3D 9)](managing-resources.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
