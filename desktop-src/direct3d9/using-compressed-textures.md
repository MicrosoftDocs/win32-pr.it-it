---
description: Uso di trame compresse (Direct3D 9)
ms.assetid: 60892a8b-93f4-43ba-87ef-d5c7cc6fb8c6
title: Uso di trame compresse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f506cef8147ee5ef1fb0c99cf862254564240bb112e954884cc7a2a07d2d12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044019"
---
# <a name="using-compressed-textures-direct3d-9"></a>Uso di trame compresse (Direct3D 9)

## <a name="determining-support-for-compressed-textures"></a>Determinazione del supporto per trame compresse

Per testare l'adattatore, specificare qualsiasi formato pixel che usa DXT1, DXT2, DXT3, DXT4 o DXT5. Se [**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) restituisce D3D OK, il dispositivo può creare la trama direttamente da una superficie di trama compressa che \_ usa tale formato. In tal caso, è possibile usare le superfici di trama compresse direttamente con Direct3D chiamando il metodo [**IDirect3DDevice9::SetTexture.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) Nell'esempio di codice seguente viene illustrato come determinare se l'adattatore supporta un formato di trama compresso.


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



Se il dispositivo non supporta la trametura da superfici di trama compresse, è comunque possibile archiviare i dati delle trame in una superficie in formato compresso, ma è necessario convertire le trame compresse in un formato supportato prima che possano essere usate per la texturing.

## <a name="creating-compressed-textures"></a>Creazione di trame compresse

Dopo aver creato un dispositivo che supporta un formato di trama compresso nell'adattatore, è possibile creare una risorsa trama compressa. Chiamare [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) e specificare un formato di trama compresso per il parametro Format.

Prima di caricare un'immagine in un oggetto trama, recuperare un puntatore alla superficie di trama chiamando il metodo [**IDirect3DTexture9::GetSurfaceLevel.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)

È ora possibile usare qualsiasi funzione D3DXLoadSurfacexxx per caricare un'immagine sulla superficie recuperata tramite [**IDirect3DTexture9::GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel). Queste funzioni gestiscono la conversione da e verso formati di trama compressi.

È possibile creare e convertire file di trama compressa (DDS) usando l'editor di trame DirectX (Dxtex.exe) fornito con DirectX SDK. È possibile ottenere Dxtex.exe informazioni da DirectX SDK. Per informazioni su DirectX SDK, vedere [Dove si trova DirectX SDK?](../directx-sdk--august-2009-.md).

Il vantaggio di questo comportamento è che un'applicazione può copiare il contenuto di una superficie compressa in un file senza calcolare la quantità di spazio di archiviazione necessaria per una superficie di una determinata larghezza e altezza nel formato specifico.

La tabella seguente illustra i cinque tipi di trame compresse. Per altre informazioni sulla modalità di archiviazione dei dati, vedere [Formati di trama compressa (Direct3D 9).](compressed-texture-formats.md) Queste informazioni sono necessarie solo se si scrivono routine di compressione personali.



| FOURCC | Descrizione        | Alpha premoltilied? |
|--------|--------------------|----------------------|
| DXT1   | Alfa opaco/a 1 bit | N/A                  |
| DXT2   | Alfa esplicito     | Sì                  |
| DXT3   | Alfa esplicito     | No                   |
| DXT4   | Alfa interpolato | Sì                  |
| DXT5   | Alfa interpolato | No                   |



 

Quando si trasferiscono dati da un formato non premoltilied a un formato premoltilied, Direct3D ridimensiona i colori in base ai valori alfa. Il trasferimento di dati da un formato premoltilied a un formato non premoltilied non è supportato. Se si tenta di trasferire dati da un'origine alfa premoltimullied a una destinazione alfa non premoltilied, il metodo restituisce D3DERR \_ INVALIDCALL. Se si trasferiscono dati da un'origine alfa premoltilied a una destinazione senza alfa, i componenti del colore di origine, che sono stati ridimensionati in base al valore alfa, vengono copiati così com'è.

## <a name="decompressing-compressed-texture-surfaces"></a>Decompressione di superfici trame compresse

Come per la compressione di una superficie di trama, la decompressione di una trama compressa viene eseguita tramite i servizi di copia Direct3D.

Per copiare una superficie di trama compressa in una superficie di trama non compressa, usare la funzione [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md). Questa funzione gestisce la compressione da e verso superfici compresse e non compresse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse trame compresse](compressed-texture-resources.md)
</dt> </dl>

 

 
