---
title: Compilazione di shader
description: Verranno ora esaminati i vari modi per compilare il codice e le convenzioni dello shader per le estensioni di file per il codice dello shader.
ms.assetid: a4e6b7cd-c5cc-4165-ba73-205155e449c9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ea71da99dd68769324b07d3fc76a0c5ca00009d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337998"
---
# <a name="compiling-shaders"></a>Compilazione di shader

> [!NOTE]
> Questo argomento descrive il `FXC.EXE` compilatore usato per i modelli shader da 2 a 5,1. Per il modello di shader 6, usare `DXC.EXE` invece, che è documentato in [uso di dxc.exe e dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll).

Microsoft Visual Studio 2012 ora può compilare il codice dello shader dai \* file HLSL inclusi nel progetto C++.

Come parte del processo di compilazione, Visual Studio 2012 USA il compilatore di codice [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL per compilare i file con estensione HLSL in file oggetto shader binari o in matrici di byte definite nei file di intestazione. Il modo in cui il compilatore di codice HLSL compila ogni file con estensione HLSL nel progetto dipende dalla modalità con cui si specifica la proprietà dei **file ouput** per il file. Per altre informazioni sulle pagine delle proprietà di HLSL, vedere [pagine delle proprietà di HLSL](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).

Il metodo Compile usato in genere dipende dalle dimensioni del \* file con estensione HLSL. Se si include una grande quantità di codice byte in un'intestazione, si aumentano le dimensioni e il tempo di caricamento iniziale dell'app. Si impone anche che tutto il codice byte risieda in memoria anche dopo la creazione dello shader, che spreca le risorse. Tuttavia, quando si include il codice byte in un'intestazione, è possibile ridurre la complessità del codice e semplificare la creazione dello shader.

Verranno ora esaminati i vari modi per compilare il codice e le convenzioni dello shader per le estensioni di file per il codice dello shader.

-   [Uso delle estensioni di file di codice dello shader](#using-shader-code-file-extensions)
-   [Compilazione in fase di compilazione in file oggetto](#compiling-at-build-time-to-object-files)
-   [Compilazione in fase di compilazione in file di intestazione](#compiling-at-build-time-to-header-files)
-   [Compilazione con D3DCompileFromFile](#compiling-with-d3dcompilefromfile)
-   [Argomenti correlati](#related-topics)
-   [Argomenti correlati](#related-topics)

## <a name="using-shader-code-file-extensions"></a>Uso delle estensioni di file di codice dello shader

Per conformarsi alla convenzione Microsoft, usare le estensioni di file seguenti per il codice dello shader:

-   Un file con estensione HLSL include il codice sorgente[HLSL](dx-graphics-hlsl-reference.md)(High Level Shading Language).
-   Un file con estensione CSO include un oggetto shader compilato.
-   Un file con estensione h è un file di intestazione, ma in un contesto di codice dello shader questo file di intestazione definisce una matrice di byte che include i dati dello shader.

## <a name="compiling-at-build-time-to-object-files"></a>Compilazione in fase di compilazione in file oggetto

Se si compilano i file con estensione HLSL in file oggetto shader binari, l'app deve leggere i dati dei file oggetto (. CSO è l'estensione predefinita per questi file oggetto), assegnare i dati a matrici di byte e creare oggetti shader da tali matrici di byte. Per creare, ad esempio, un vertex shader ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader) \* \* ), chiamare il metodo [**ID3D11Device:: CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) con una matrice di byte che contiene il codice byte del vertex shader compilato. Nell' [esempio di esercitazione Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) viene illustrato come creare oggetti shader da matrici di byte ottenute da file oggetto shader binari. cso. In questo esempio di codice dell' [esempio di esercitazione Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample), la proprietà **file ouput** per il file SimpleVertexShader. HLSL specifica di compilare il file oggetto SimpleVertexShader. cso.

```cpp
        auto vertexShaderBytecode = reader->ReadData("SimpleVertexShader.cso");
        ComPtr<ID3D11VertexShader> vertexShader;
        DX::ThrowIfFailed(
            m_d3dDevice->CreateVertexShader(
                vertexShaderBytecode->Data,
                vertexShaderBytecode->Length,
                nullptr,
                &vertexShader
                )
```

## <a name="compiling-at-build-time-to-header-files"></a>Compilazione in fase di compilazione in file di intestazione

Se si compilano i file con estensione HLSL in matrici di byte definite nei file di intestazione, è necessario includere i file di intestazione nel codice. L' [esempio Media Extensions](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) Mostra come creare oggetti shader dalle matrici di byte definite nei file di intestazione e da includere nel progetto in fase di compilazione. In questo esempio di codice dell' [esempio Media Extensions](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample)la proprietà **file ouput** per il file PixelShader. HLSL specifica di compilare la matrice di byte *g \_ Psshader* definita nel file di intestazione PixelShader. h.


```C++
#       include "PixelShader.h"
        ComPtr<ID3D11PixelShader> m_pPixelShader;
        hr = pDevice->CreatePixelShader(g_psshader, sizeof(g_psshader), nullptr, &m_pPixelShader);
```



## <a name="compiling-with-d3dcompilefromfile"></a>Compilazione con D3DCompileFromFile

È anche possibile usare la funzione [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) in fase di esecuzione per compilare il codice dello shader. Per altre informazioni su come eseguire questa operazione, vedere [procedura: compilare uno shader](/windows/desktop/direct3d11/how-to--compile-a-shader).

> [!Note]  
> Le app di Windows Store supportano l'uso di [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) per lo sviluppo, ma non per la distribuzione.

 

## <a name="related-topics"></a>Argomenti correlati

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 