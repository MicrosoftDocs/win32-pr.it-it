---
description: Combinazione di zero o più opzioni di blocco che descrivono il tipo di blocco da eseguire.
ms.assetid: 46a611bd-a1ec-4967-b68d-72661d1b5cad
title: D3DLOCK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e4fcf8db9e60a30aee060dcc483b8d01e59b1c
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343196"
---
# <a name="d3dlock"></a>D3DLOCK

Combinazione di zero o più opzioni di blocco che descrivono il tipo di blocco da eseguire.



| \#Definire                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DLOCK \_ DISCARD           | L'applicazione rimuove tutta la memoria all'interno dell'area bloccata. Per i buffer dei vertici e degli indici, l'intero buffer verrà eliminato. Questa opzione è valida solo quando la risorsa viene creata con l'utilizzo dinamico (vedere [D3DUSAGE).](d3dusage.md)                                                                                                                                                                                                                                                                                                                                                           |
| D3DLOCK \_ DONOTWAIT         | Consente a un'applicazione di recuperare i cicli della CPU se il driver non riesce a bloccare immediatamente la superficie. Se questo flag è impostato e il driver non può bloccare immediatamente la superficie, la chiamata di blocco restituirà D3DERR \_ WASSTILLDRAWING. Questo flag può essere usato solo quando si blocca una superficie creata usando [**CreateOffscreenPlainSurface,**](/windows/desktop/api) [**CreateRenderTarget**](/windows/desktop/api)o [**CreateDepthStencilSurface.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) Questo flag può essere usato anche con un buffer nascosto.            |
| D3DLOCK \_ NO \_ DIRTY \_ UPDATE | Per impostazione predefinita, un blocco su una risorsa aggiunge un'area dirty a tale risorsa. Questa opzione impedisce qualsiasi modifica allo stato dirty della risorsa. Le applicazioni devono usare questa opzione quando hanno informazioni aggiuntive sul set di aree modificate durante l'operazione di blocco.                                                                                                                                                                                                                                                                                                                    |
| D3DLOCK \_ NOOVERWRITE       | Indica che la memoria a cui si è fatto riferimento in una chiamata di disegno dall'ultimo blocco senza questo flag non verrà modificata durante il blocco. In questo modo è possibile abilitare le ottimizzazioni quando l'applicazione aggiunge dati a una risorsa. Se si specifica questo flag, il driver può restituire immediatamente se la risorsa è in uso. In caso contrario, il driver deve completare l'uso della risorsa prima di restituire il blocco.                                                                                                                                                                                            |
| D3DLOCK \_ NOSYSLOCK         | Il comportamento predefinito di un blocco di memoria video è riservare una sezione critica a livello di sistema, garantendo che non si verifichino modifiche della modalità di visualizzazione per la durata del blocco. Questa opzione fa sì che la sezione critica a livello di sistema non sia mantenuta per la durata del blocco.<br/> L'operazione di blocco richiede molto tempo, ma può consentire al sistema di eseguire altri compiti, ad esempio lo spostamento del cursore del mouse. Questa opzione è utile per i blocchi di lunga durata, ad esempio il blocco del buffer nascosto per il rendering software che in caso contrario influirebbe negativamente sulla velocità di risposta del sistema.<br/> |
| D3DLOCK \_ READONLY          | L'applicazione non scriverà nel buffer. Ciò consente alle risorse archiviate in formati non nativi di salvare il passaggio di ricompressione durante lo sblocco.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="constant-information"></a>Informazioni costanti



|  Requisito                        | Valore            |
|--------------------------|-------------|
| Intestazione                   | d3d9types.h |
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

[**Archivio protetto**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[**Archivio protetto**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
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

 

 
