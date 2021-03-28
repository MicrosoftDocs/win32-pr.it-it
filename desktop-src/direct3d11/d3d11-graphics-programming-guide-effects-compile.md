---
title: Compilare un effetto (Direct3D 11)
description: Dopo aver creato un effetto, il passaggio successivo consiste nel compilare il codice per verificare la presenza di problemi di sintassi.
ms.assetid: 7624d55e-6466-4156-8f31-30f0d25a2883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3df304a7b657af19984008bd90a1be4bfe5219c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963200"
---
# <a name="compile-an-effect-direct3d-11"></a>Compilare un effetto (Direct3D 11)

Dopo aver creato un effetto, il passaggio successivo consiste nel compilare il codice per verificare la presenza di problemi di sintassi.

A tale scopo, chiamare una delle API di compilazione ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md)o [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ). Queste API richiamano l'effetto del compilatore fxc.exe, che compila il codice HLSL. Questo è il motivo per cui la sintassi per il codice in un effetto è molto simile a quella del codice HLSL. (Ci sono alcune eccezioni che verranno gestite successivamente). Il compilatore compilatore/HLSL di effetti, fxc.exe, è disponibile nell'SDK nella cartella Utilities, in modo che gli shader (o gli effetti) possano essere compilati offline se si sceglie. Vedere la documentazione per l'esecuzione del compilatore dalla riga di comando.

-   [Esempio](#example)
-   [Includes](#includes)
-   [Ricerca di file di inclusione](#searching-for-include-files)
-   [Macro](#macros)
-   [Flag shader HLSL](#hlsl-shader-flags)
-   [Flag FX](#fx-flags)
-   [Verifica degli errori](#checking-errors)
-   [Argomenti correlati](#related-topics)

## <a name="example"></a>Esempio

Di seguito è riportato un esempio di compilazione di un file di effetti.


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, NULL, &pBlob, &pErrorBlob, NULL );
```



## <a name="includes"></a>Includes

Un parametro delle API di compilazione è un'interfaccia di inclusione. Generare uno di questi se si desidera includere un comportamento personalizzato quando il compilatore legge un file di inclusione. Il compilatore esegue questo comportamento personalizzato ogni volta che crea o compila un effetto (che usa il puntatore di inclusione). Per implementare il comportamento di inclusione personalizzato, derivare una classe dall'interfaccia [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) . In questo modo viene fornita la classe con due metodi: [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) e [**Close**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close). Implementare il comportamento personalizzato in questi metodi.

## <a name="searching-for-include-files"></a>Ricerca di file di inclusione

Il puntatore passato dal compilatore nel parametro *pParentData* al metodo [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) del gestore di inclusione potrebbe non puntare al contenitore che include il \# file di inclusione necessario al compilatore per compilare il codice dello shader. Ovvero, il compilatore potrebbe passare **null** in *pParentData*. Pertanto, è consigliabile che il gestore di inclusione cerchi un elenco di percorsi di inclusione per il contenuto. Il gestore di inclusione può aggiungere dinamicamente nuovi percorsi di inclusione poiché riceve tali percorsi nelle chiamate al metodo **Open** .

Nell'esempio seguente si supponga che i file di inclusione del codice dello shader siano entrambi archiviati nella directory *somewhereelse* Quando il compilatore chiama il metodo [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) del gestore di inclusione per aprire e leggere il contenuto di *somewhereelse \\ foo. h*, il gestore di inclusione può salvare il percorso della directory **somewhereelse** . Successivamente, quando il compilatore chiama il metodo **Open** del gestore di inclusione per aprire e leggere il contenuto di *bar. h*, il gestore di inclusione può eseguire automaticamente la ricerca nella directory *somewhereelse* per *barra. h*.


```
Main.hlsl:
#include "somewhereelse\foo.h"

Foo.h:
#include "bar.h"
```



## <a name="macros"></a>Macro

La compilazione degli effetti può anche portare un puntatore a macro definite altrove. Si supponga, ad esempio, di voler modificare l'effetto in BasicHLSL10 per usare due macro: zero e uno. Il codice di effetto che usa le due macro è illustrato di seguito.


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



Di seguito è illustrata la dichiarazione per le due macro.


```
D3D10_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



Le macro sono una matrice con terminazione NULL di macro. dove ogni macro viene definita utilizzando uno struct [**della \_ \_ macro dello shader D3D10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .

Modificare la chiamata dell'effetto di compilazione per portare un puntatore alle macro.


```
D3DX11CompileFromFile( str, Shader_Macros, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );    
```



## <a name="hlsl-shader-flags"></a>Flag shader HLSL

I flag shader specificano i vincoli dello shader per il compilatore HLSL. Questi flag influiscono sul codice generato dal compilatore shader nei modi seguenti:

-   Ottimizzare le dimensioni del codice.
-   Inclusione di informazioni di debug, che impedisce il controllo di flusso.
-   Influiscono sulla destinazione di compilazione e sul fatto che uno shader possa essere eseguito su hardware legacy.

Questi flag possono essere combinati logicamente se non sono state specificate due caratteristiche in conflitto. Per un elenco dei flag, vedere [ \_ costanti shader D3D10](/windows/desktop/direct3d10/d3d10-shader).

## <a name="fx-flags"></a>Flag FX

Usare questi flag quando si crea un effetto per definire il comportamento di compilazione o l'effetto di Runtime. Per un elenco dei flag, vedere [ \_ costanti degli effetti D3D10](/windows/desktop/direct3d10/d3d10-effect).

## <a name="checking-errors"></a>Verifica degli errori

Se durante la compilazione si verifica un errore, l'API restituisce un'interfaccia che contiene gli errori del compilatore di effetti. Questa interfaccia è denominata [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)). Non è leggibile direttamente; Tuttavia, restituendo un puntatore al buffer che contiene i dati (ovvero una stringa), è possibile visualizzare gli eventuali errori di compilazione.

Questo esempio contiene un errore in BasicHLSL. FX, la prima dichiarazione di variabile si verifica due volte.


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



Questo errore induce il compilatore a restituire l'errore seguente, come illustrato nello screenshot seguente del finestra Espressioni di controllo in Microsoft Visual Studio.

![screenshot della finestra espressioni di controllo di Visual Studio con un errore 0x01997fb8](images/effect-compile-errors-2.jpg)

Poiché il compilatore restituisce l'errore in un puntatore LPVOID, eseguirne il cast in una stringa di caratteri nell'finestra Espressioni di controllo.

Ecco il codice che restituisce l'errore dalla compilazione non riuscita.


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3DBlob*   l_pBlob_Effect = NULL;
ID3DBlob*   l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );      

LPVOID l_pError = NULL;
if( pErrorBlob )
{
    l_pError = pErrorBlob->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di un effetto (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 