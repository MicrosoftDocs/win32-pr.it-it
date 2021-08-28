---
description: Dopo aver creato un effetto, il primo passaggio consiste nel compilare il codice per verificare la presenza di problemi di sintassi.
ms.assetid: b8d8a0b7-b520-44e4-8691-6eb46202c092
title: Compilare un effetto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e0c4364fab67b0e0e7c97b7478a023f6394b5515e6f1d16cf2d352172af6c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128429"
---
# <a name="compile-an-effect-direct3d-10"></a>Compilare un effetto (Direct3D 10)

Dopo aver creato un effetto, il primo passaggio consiste nel compilare il codice per verificare la presenza di problemi di sintassi. Questa operazione viene eseguita chiamando una delle API di compilazione, ad esempio D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory. Queste API richiamano l'effetto del compilatore fxc.exe che è il compilatore usato per compilare il codice HLSL. Questo è il motivo per cui la sintassi per il codice in un effetto è molto simile al codice HLSL (alcune eccezioni verranno gestite in un secondo momento). A proposito, l'effetto compilatore/compilatore hlsl (fxc.exe) si trova nell'SDK nella cartella delle utilità, in modo che sia possibile compilare gli shader (o gli effetti) offline, se lo si desidera. Vedere la documentazione per l'esecuzione del compilatore dalla riga di comando.

-   [Includes](#includes)
-   [Macro](#macros)
-   [Flag di shader HLSL](#hlsl-shader-flags)
-   [Flag FX](#fx-flags)
-   [Controllo degli errori](#checking-errors)
-   [Argomenti correlati](#related-topics)

Di seguito è riportato un esempio di compilazione di un file di effetto (dall'esempio BasicHLSL10).


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX10CompileEffectFromFile( str, NULL, NULL, "fx_4_0", 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors, NULL );
```



## <a name="includes"></a>Includes

Un parametro è un'interfaccia di inclusione. Generarne uno se si vuole includere un comportamento personalizzato durante la lettura di un file di inclusione. Questo comportamento personalizzato viene eseguito ogni volta che viene creato un effetto (che usa il puntatore di inclusione) o quando viene compilato un effetto (che usa il puntatore di inclusione). Per implementare un comportamento di inclusione personalizzato, derivare una classe dall'interfaccia Include. In questo modo la classe fornisce due metodi: Open e Close. Implementare il comportamento personalizzato nei metodi Open e Close.

## <a name="macros"></a>Macro

La compilazione degli effetti può anche prendere un puntatore alle macro definite altrove. Si supponga, ad esempio, di voler modificare l'effetto in BasicHLSL10 per usare due macro: zero e una. Il codice dell'effetto che usa le due macro è illustrato di seguito.


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



Ecco la dichiarazione per le due macro.


```
D3D_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



Le macro sono una matrice di macro con terminazione NULL. dove ogni macro è definita con uno struct [**D3D \_ SHADER \_ MACRO.**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)

Infine, modificare la chiamata dell'effetto di compilazione per prendere un puntatore alle macro.


```
D3DX10CreateEffectFromFile( str, Shader_Macros, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &g_pEffect10, NULL );
```



## <a name="hlsl-shader-flags"></a>Flag di shader HLSL

I flag di shader specificano i vincoli dello shader per il compilatore HLSL. Questi flag influiscono sul codice generato dal compilatore shader, tra cui:

-   Considerazioni sulle dimensioni: ottimizzare il codice.
-   Considerazioni sul debug: incluse le informazioni di debug, impedendo il controllo di flusso.
-   Considerazioni sull'hardware: la destinazione di compilazione e se uno shader può essere eseguito o meno su hardware legacy.

In generale, questi flag possono essere combinati logicamente, presupponendo che non siano state specificate due caratteristiche in conflitto. Per un elenco dei flag, vedere [Costanti effetto (Direct3D 10).](d3d10-graphics-reference-effect-constants.md)

## <a name="fx-flags"></a>Flag FX

Questi flag vengono usati durante la creazione di un effetto per definire il comportamento di compilazione o di effetto di runtime. Per un elenco dei flag, vedere [Costanti effetto (Direct3D 10).](d3d10-graphics-reference-effect-constants.md)

## <a name="checking-errors"></a>Controllo degli errori

Se durante la compilazione si verifica un errore, l'API restituisce un'interfaccia che contiene gli errori restituiti dal compilatore dell'effetto. Questa interfaccia è denominata ID3D10Blob. Non è leggibile direttamente, tuttavia, se si restituisce un puntatore al buffer che contiene i dati (ovvero una stringa), è possibile visualizzare eventuali errori di compilazione.

In questo esempio è stato introdotto un errore nell'effetto BasicHLSL.fx copiando la prima dichiarazione di variabile due volte.


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



Questo errore ha causato la restituzione dell'errore seguente da parte del compilatore, come illustrato nello screenshot seguente della finestra Espressioni di controllo Microsoft Visual Studio.

![Screenshot della finestra Espressioni di controllo di Visual Studio](images/effect-compile-errors-2.jpg)

Poiché l'errore viene restituito in un puntatore LPVOID, eseguire il cast a una stringa di caratteri nella finestra Espressioni di controllo.

Ecco il codice usato per restituire l'errore dalla compilazione non riuscita.


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

 

 



