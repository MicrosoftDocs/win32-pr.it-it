---
description: Combinazione di zero o più opzioni di blocco che descrivono il tipo di blocco da eseguire.
ms.assetid: 46a611bd-a1ec-4967-b68d-72661d1b5cad
title: D3DLOCK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea3a60318aad8ae0fadcf02d5dea76f6aa62548
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748730"
---
# <a name="d3dlock"></a>D3DLOCK

Combinazione di zero o più opzioni di blocco che descrivono il tipo di blocco da eseguire.



|                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definire                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Eliminazione di D3DLOCK \_           | L'applicazione elimina tutta la memoria all'interno dell'area bloccata. Per i buffer dei vertici e degli indici, l'intero buffer verrà rimosso. Questa opzione è valida solo quando la risorsa viene creata con utilizzo dinamico (vedere [D3DUSAGE](d3dusage.md)).                                                                                                                                                                                                                                                                                                                                                           |
| \_DONOTWAIT D3DLOCK         | Consente a un'applicazione di ottenere i cicli della CPU se il driver non è in grado di bloccare immediatamente la superficie. Se questo flag è impostato e il driver non è in grado di bloccare immediatamente la superficie, la chiamata di blocco restituirà D3DERR \_ WASSTILLDRAWING. Questo flag può essere utilizzato solo quando si blocca una superficie creata utilizzando [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateRenderTarget**](/windows/desktop/api)o [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface). Questo flag può essere usato anche con un buffer nascosto.            |
| D3DLOCK \_ nessun \_ \_ aggiornamento Dirty | Per impostazione predefinita, un blocco su una risorsa aggiunge un'area dirty a tale risorsa. Questa opzione impedisce qualsiasi modifica allo stato dirty della risorsa. Le applicazioni devono usare questa opzione quando hanno informazioni aggiuntive sul set di aree modificate durante l'operazione di blocco.                                                                                                                                                                                                                                                                                                                    |
| Nosovrascrive D3DLOCK \_       | Indica che la memoria a cui è stato fatto riferimento in una chiamata di disegno dall'ultimo blocco senza questo flag non verrà modificata durante il blocco. In questo modo è possibile abilitare le ottimizzazioni quando l'applicazione aggiunge dati a una risorsa. Se si specifica questo flag, il driver restituirà immediatamente se la risorsa è in uso. in caso contrario, il driver deve terminare utilizzando la risorsa prima di tornare al blocco.                                                                                                                                                                                            |
| \_NOSYSLOCK D3DLOCK         | Il comportamento predefinito di un blocco di memoria video consiste nel riservare una sezione critica a livello di sistema, garantendo che non venga apportata alcuna modifica alla modalità di visualizzazione per la durata del blocco. Questa opzione fa in modo che la sezione critica a livello di sistema non venga mantenuta per tutta la durata del blocco.<br/> L'operazione di blocco richiede molto tempo, ma può consentire al sistema di eseguire altre mansioni, ad esempio lo spostamento del cursore del mouse. Questa opzione è utile per i blocchi di lunga durata, ad esempio il blocco del buffer nascosto per il rendering del software che altrimenti influirà negativamente sulla velocità di risposta del sistema.<br/> |
| D3DLOCK \_ ReadOnly          | L'applicazione non effettuerà la scrittura nel buffer. In questo modo le risorse archiviate in formati non nativi consentono di salvare il passaggio di ricompressione durante lo sblocco.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |             |
|--------------------------|-------------|
| Intestazione                   | d3d9types. h |
| Sistema operativo minimo | Windows 98  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[**Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[**LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**LockIndexBuffer**](id3dxbasemesh--lockindexbuffer.md)
</dt> <dt>

[**LockVertexBuffer**](id3dxbasemesh--lockvertexbuffer.md)
</dt> <dt>

**LockVertexBuffer**
</dt> <dt>

[**LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

[**LockAttributeBuffer**](id3dxpatchmesh--lockattributebuffer.md)
</dt> <dt>

[**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md)
</dt> <dt>

[**LockVertexBuffer**](id3dxpatchmesh--lockvertexbuffer.md)
</dt> </dl>

 

 
