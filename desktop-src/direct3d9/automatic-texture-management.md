---
description: La gestione delle trame è il processo che consente di determinare le trame necessarie per il rendering in un determinato momento e di assicurarsi che tali trame siano caricate nella memoria video.
ms.assetid: ea6d64ee-f570-49eb-b5fd-67fcde3f8ddc
title: Gestione automatica trame (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c65168947acb05c8437836ba0b27765a9b03d3ba97fd223f50eb9a99ab8c50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751401"
---
# <a name="automatic-texture-management-direct3d-9"></a>Gestione automatica trame (Direct3D 9)

La gestione delle trame è il processo che consente di determinare le trame necessarie per il rendering in un determinato momento e di assicurarsi che tali trame siano caricate nella memoria video. Come per qualsiasi algoritmo, gli schemi di gestione delle trame variano a seconda della complessità, ma qualsiasi approccio alla gestione delle trame comporta le attività chiave seguenti.

-   Rilevamento della quantità di memoria trame disponibile.
-   Calcolo delle trame necessarie per il rendering e delle quali non lo sono.
-   Determinare quali risorse trame esistenti possono essere ricaricate con un'altra immagine di trama e quali superfici devono essere distrutte e sostituite con nuove risorse di trama.

Direct3D implementa la gestione delle trame supportata dal sistema per garantire che le trame siano caricate per ottenere prestazioni ottimali. Le risorse di trama gestite da Direct3D vengono definite trame gestite.

Il gestore delle trame tiene traccia delle trame con un timestamp che identifica l'ultima volta che la trama è stata usata. Usa quindi un algoritmo usato meno di recente per determinare quali trame devono essere rimosse. Le priorità delle trame vengono usate come tie breaker quando due trame sono destinate alla rimozione dalla memoria. Se due trame hanno lo stesso valore di priorità, la trama usata meno di recente viene rimossa. Tuttavia, se due trame hanno lo stesso timestamp, la trama con priorità più bassa viene rimossa per prima.

È necessario la gestione automatica delle trame per le superfici di trama quando vengono create. Per recuperare una trama gestita in un'applicazione C++, creare una risorsa trama chiamando [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) e specificando D3DPOOL MANAGED per il \_ parametro Pool. Non è consentito specificare dove si vuole creare la trama. Non è possibile usare i flag D3DPOOL DEFAULT o \_ D3DPOOL \_ SYSTEMMEM quando si crea una trama gestita. Dopo aver creato la trama gestita, è possibile chiamare il metodo [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) per impostarla su una fase nella catena di trame del dispositivo di rendering.

È possibile assegnare una priorità alle trame gestite chiamando il metodo [**IDirect3DResource9::SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) per la superficie di trama.

Direct3D scarica automaticamente le trame nella memoria video in base alle esigenze. Il sistema potrebbe memorizzare nella cache le trame gestite nella memoria video locale o non locale, a seconda della disponibilità della memoria video non locale o di altri fattori. Il percorso della cache delle trame gestite non viene comunicato all'applicazione, né queste informazioni sono necessarie per usare la gestione automatica delle trame. Se l'applicazione usa più trame di quelle che possono essere presenti nella memoria video, Direct3D rimuove le trame meno recenti dalla memoria video per fare spazio alle nuove trame. Se si usa di nuovo una trama rimossa, il sistema usa la superficie di trama originale della memoria di sistema per ricaricare la trama nella cache della memoria video. Anche se è necessario ricaricare la trama, riduce anche le prestazioni dell'applicazione.

È possibile modificare dinamicamente la copia originale della memoria di sistema della trama aggiornando o bloccando la risorsa trama. Quando il sistema rileva una superficie dirty, dopo il completamento di un aggiornamento o quando la superficie viene sbloccata, gestione trame aggiorna automaticamente la copia della memoria video della trama. L'effetto sulle prestazioni incorso è simile al ricaricamento di una trama rimossa.

Quando si immette un nuovo livello in un gioco, l'applicazione potrebbe dover scaricare tutte le trame gestite dalla memoria video (chiamando [**IDirect3DDevice9::EvictManagedResources**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-evictmanagedresources)).

Per altre informazioni sulla gestione delle risorse, vedere [Gestione delle risorse (Direct3D 9).](managing-resources.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trame Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
