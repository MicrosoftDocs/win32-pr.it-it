---
description: Uso di trame compresse (Direct3D 9)
ms.assetid: 60892a8b-93f4-43ba-87ef-d5c7cc6fb8c6
title: Uso di trame compresse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 643b0618043f12ff3e1a84b806c86edb780ad929
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747602"
---
# <a name="using-compressed-textures-direct3d-9"></a>Uso di trame compresse (Direct3D 9)

## <a name="determining-support-for-compressed-textures"></a>Determinazione del supporto per le trame compresse

Per eseguire il test dell'adapter, specificare qualsiasi formato pixel che usa DXT1, DXT2, DXT3, DXT4 o DXT5. Se [**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) restituisce D3D \_ OK, il dispositivo può creare una trama direttamente da una superficie di trama compressa che usa tale formato. In tal caso, è possibile usare le superfici di trama compresse direttamente con Direct3D chiamando il metodo [**IDirect3DDevice9:: setexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) . Nell'esempio di codice riportato di seguito viene illustrato come determinare se l'adapter supporta un formato di trama compresso.


```
BOOL IsCompressedTextureFormatOk( D3DFORMAT TextureFormat, 
                                  D3DFORMAT AdapterFormat ) 
{
    HRESULT hr = pD3D->CheckDeviceFormat( D3DADAPTER_DEFAULT,
                                          D3DDEVTYPE_HAL,
                                          AdapterFormat,
                                          0,
                                          D3DRTYPE_TEXTURE,
                                          TextureFormat);

    return SUCCEEDED( hr );
}
```



Se il dispositivo non supporta la texturing da superfici di trama compresse, è comunque possibile archiviare i dati di trama in una superficie di formato compresso, ma è necessario convertire le trame compresse in un formato supportato prima di poterle usare per il texturing.

## <a name="creating-compressed-textures"></a>Creazione di trame compresse

Dopo aver creato un dispositivo che supporta un formato di trama compresso sulla scheda, è possibile creare una risorsa di trama compressa. Chiamare [**IDirect3DDevice9:: createTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) e specificare un formato di trama compresso per il parametro format.

Prima di caricare un'immagine in un oggetto trama, recuperare un puntatore alla superficie della trama chiamando il metodo [**IDirect3DTexture9:: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) .

A questo punto è possibile usare qualsiasi funzione D3DXLoadSurfacexxx per caricare un'immagine nell'area recuperata tramite [**IDirect3DTexture9:: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel). Queste funzioni gestiscono la conversione da e verso formati di trama compressi.

È possibile creare e convertire file di trama compressi (DDS) usando l'editor di trame DirectX (Dxtex.exe) fornito con DirectX SDK. È possibile ottenere Dxtex.exe e ottenere informazioni su di esso da DirectX SDK. Per informazioni su DirectX SDK, vedere [dove è DirectX SDK?](../directx-sdk--august-2009-.md).

Il vantaggio di questo comportamento è che un'applicazione può copiare il contenuto di una superficie compressa in un file senza calcolare la quantità di spazio di archiviazione necessaria per una superficie di una particolare larghezza e altezza nel formato specifico.

La tabella seguente illustra i cinque tipi di trame compresse. Per altre informazioni sulla modalità di archiviazione dei dati, vedere [formati di trama compressi (Direct3D 9)](compressed-texture-formats.md). Queste informazioni sono necessarie solo se si scrivono routine di compressione personalizzate.



| FOURCC | Descrizione        | Alfa premoltiplicato? |
|--------|--------------------|----------------------|
| DXT1   | Alfa opaco/1 bit | N/D                  |
| DXT2   | Alfa esplicito     | Sì                  |
| DXT3   | Alfa esplicito     | No                   |
| DXT4   | Alfa interpolata | Sì                  |
| DXT5   | Alfa interpolata | No                   |



 

Quando si trasferiscono i dati da un formato NonPremultiplied a un formato premoltiplicato, Direct3D ridimensiona i colori in base ai valori alfa. Il trasferimento dei dati da un formato premoltiplicato a un formato NonPremultiplied non è supportato. Se si tenta di trasferire i dati da un'origine alfa premoltiplicata a una destinazione NonPremultiplied Alpha, il metodo restituisce D3DERR \_ INVALIDCALL. Se si trasferiscono i dati da un'origine alfa premoltiplicata a una destinazione senza Alpha, i componenti del colore di origine, che sono stati ridimensionati da Alpha, vengono copiati così come sono.

## <a name="decompressing-compressed-texture-surfaces"></a>Decompressione delle superfici di trama compresse

Come per la compressione di una superficie di trama, la decompressione di una trama compressa viene eseguita tramite i servizi di copia Direct3D.

Per copiare una superficie di trama compressa in una superficie di trama non compressa, usare la funzione [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md). Questa funzione gestisce la compressione da e verso le superfici compresse e non compresse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse di trama compresse](compressed-texture-resources.md)
</dt> </dl>

 

 
