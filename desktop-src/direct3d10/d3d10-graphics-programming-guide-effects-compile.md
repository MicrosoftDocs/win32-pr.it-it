---
description: Una volta creato un effetto, il primo passaggio consiste nel compilare il codice per verificare la presenza di problemi di sintassi.
ms.assetid: b8d8a0b7-b520-44e4-8691-6eb46202c092
title: Compilare un effetto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab6183f2f71b07c482fa24efc4f9fed199216d75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225578"
---
# <a name="compile-an-effect-direct3d-10"></a>Compilare un effetto (Direct3D 10)

Una volta creato un effetto, il primo passaggio consiste nel compilare il codice per verificare la presenza di problemi di sintassi. Questa operazione viene eseguita chiamando una delle API di compilazione, ad esempio D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory. Queste API richiamano il compilatore Effect fxc.exe che è il compilatore usato per compilare il codice HLSL. Questo è il motivo per cui la sintassi per il codice in un effetto è molto simile a quella del codice HLSL (ci sono alcune eccezioni che verranno gestite successivamente). Il compilatore HLSL (fxc.exe) Effect si trova nell'SDK nella cartella Utilities, in modo che sia possibile compilare gli shader (o gli effetti) offline se lo si sceglie. Vedere la documentazione per l'esecuzione del compilatore dalla riga di comando.

-   [Includes](#includes)
-   [Macro](#macros)
-   [Flag shader HLSL](#hlsl-shader-flags)
-   [Flag FX](#fx-flags)
-   [Verifica degli errori](#checking-errors)
-   [Argomenti correlati](#related-topics)

Di seguito è riportato un esempio di compilazione di un file di effetti (dall'esempio BasicHLSL10).


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX10CompileEffectFromFile( str, NULL, NULL, "fx_4_0", 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors, NULL );
```



## <a name="includes"></a>Includes

Un parametro è un'interfaccia di inclusione. Generare uno di questi se si desidera includere un comportamento personalizzato durante la lettura di un file di inclusione. Questo comportamento personalizzato viene eseguito ogni volta che viene creato un effetto (che usa il puntatore di inclusione) o quando viene compilato un effetto (che usa il puntatore di inclusione). Per implementare il comportamento di inclusione personalizzato, derivare una classe dall'interfaccia di inclusione. In questo modo sono disponibili i due metodi di classe: Open e Close. Implementare il comportamento personalizzato nei metodi Open e Close.

## <a name="macros"></a>Macro

La compilazione degli effetti può anche portare un puntatore a macro definite altrove. Si supponga, ad esempio, di modificare l'effetto in BasicHLSL10 per usare due macro: zero e uno. Il codice di effetto che usa le due macro è illustrato di seguito.


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



Di seguito è illustrata la dichiarazione per le due macro.


```
D3D_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



Le macro sono una matrice di macro con terminazione NULL. dove ogni macro viene definita con uno struct di [**\_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .

Infine, modificare la chiamata dell'effetto di compilazione per portare un puntatore alle macro.


```
D3DX10CreateEffectFromFile( str, Shader_Macros, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &g_pEffect10, NULL );
```



## <a name="hlsl-shader-flags"></a>Flag shader HLSL

I flag shader specificano i vincoli dello shader per il compilatore HLSL. Questi flag influiscano sul codice generato dal compilatore shader, tra cui:

-   Considerazioni sulle dimensioni: ottimizzare il codice.
-   Considerazioni sul debug: incluse le informazioni di debug, impedendo il controllo di flusso.
-   Considerazioni sull'hardware: la destinazione di compilazione e se uno shader può essere eseguito su hardware legacy.

In generale, questi flag possono essere combinati logicamente, supponendo che non siano state specificate due caratteristiche in conflitto. Per un elenco dei flag, vedere [costanti degli effetti (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).

## <a name="fx-flags"></a>Flag FX

Questi flag utilizzati durante la creazione di un effetto per definire il comportamento di compilazione o l'effetto di Runtime. Per un elenco dei flag, vedere [costanti degli effetti (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).

## <a name="checking-errors"></a>Verifica degli errori

Se durante la compilazione si verifica un errore, l'API restituisce un'interfaccia che contiene gli errori restituiti dal compilatore di effetti. Questa interfaccia è denominata ID3D10Blob. Tuttavia, non è direttamente leggibile, restituendo un puntatore al buffer che contiene i dati (ovvero una stringa), è possibile visualizzare gli eventuali errori di compilazione.

In questo esempio è stato introdotto un errore nell'effetto BasicHLSL. FX copiando la prima dichiarazione di variabile due volte.


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



Questo errore ha impedito al compilatore di restituire l'errore seguente, come illustrato nello screenshot seguente della finestra espressioni di controllo in Microsoft Visual Studio.

![screenshot della finestra espressioni di controllo di Visual Studio](images/effect-compile-errors-2.jpg)

Poiché l'errore viene restituito in un puntatore LPVOID, eseguirne il cast in una stringa di caratteri nella finestra espressioni di controllo.

Di seguito è riportato il codice utilizzato per restituire l'errore dalla compilazione non riuscita.


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3D10Blob* l_pBlob_Effect = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX10CompileEffectFromFile( str, NULL, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors );

LPVOID l_pError = NULL;
if( l_pBlob_Errors )
{
    l_pError = l_pBlob_Errors->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di un effetto (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



