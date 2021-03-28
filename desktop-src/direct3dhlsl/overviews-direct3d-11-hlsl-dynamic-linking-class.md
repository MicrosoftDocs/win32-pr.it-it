---
title: Interfacce e classi
description: Il collegamento dinamico dello shader usa le interfacce HLSL (High-Level Shader Language) e le classi sintatticamente simili alle relative controparti C++.
ms.assetid: 124a358d-30ab-4efe-88ed-1ff277d17b25
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 71410caf7d80cb9dbcd0165c753d75cc8f5cbe00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399460"
---
# <a name="interfaces-and-classes"></a>Interfacce e classi

Il collegamento dinamico dello shader usa le interfacce HLSL (High-Level Shader Language) e le classi sintatticamente simili alle relative controparti C++. Ciò consente agli shader di fare riferimento a istanze di interfaccia astratte in fase di compilazione e di lasciare la risoluzione di tali istanze a classi concrete per l'applicazione in fase di esecuzione.

Le sezioni seguenti illustrano in dettaglio come configurare uno shader per l'uso di interfacce e classi e come inizializzare le istanze dell'interfaccia nel codice dell'applicazione.

-   [Dichiarazione di interfacce](#declaring-interfaces)
-   [Dichiarazione di classi](#declaring-classes)
-   [Dichiarazioni di istanze di interfaccia in uno shader](#interface-instance-declarations-in-a-shader)
-   [Dichiarazioni di istanze di classe in uno shader](#class-instance-declarations-in-a-shader)
-   [Inizializzazione di istanze di interfaccia in un'applicazione](#initializing-interface-instances-in-an-application)
-   [Argomenti correlati](#related-topics)

## <a name="declaring-interfaces"></a>Dichiarazione di interfacce

Un'interfaccia funziona in modo simile a una classe di base astratta in C++. Un'interfaccia viene dichiarata in uno shader usando la parola chiave Interface e contiene solo dichiarazioni di metodo. I metodi dichiarati in un'interfaccia saranno tutti metodi virtuali in tutte le classi derivate dall'interfaccia. Le classi derivate devono implementare tutti i metodi dichiarati in un'interfaccia. Si noti che le interfacce sono l'unico modo per dichiarare i metodi virtuali, non esiste una parola chiave virtuale come in C++ e le classi connot dichiarano metodi virtuali.

Nell'esempio di codice dello shader seguente vengono dichiarate due interfacce.


```
interface iBaseLight
{
   float3 IlluminateAmbient(float3 vNormal);
   float3 IlluminateDiffuse(float3 vNormal);
   float3 IlluminateSpecular(float3 vNormal, int specularPower );
};       

interface iBaseMaterial
{
   float3 GetAmbientColor(float2 vTexcoord);
   
   float3 GetDiffuseColor(float2 vTexcoord);

   int GetSpecularPower();

};
      
```



## <a name="declaring-classes"></a>Dichiarazione di classi

Una classe si comporta in modo analogo alle classi in C++. Una classe viene dichiarata con la parola chiave Class e può contenere variabili membro e metodi. Una classe può ereditare da zero o una classe e da zero o più interfacce. Le classi devono implementare o ereditare implementazioni per tutte le interfacce nella catena di ereditarietà oppure non è possibile creare un'istanza della classe.

Nell'esempio di codice dello shader seguente viene illustrato come derivare una classe da un'interfaccia e da un'altra classe.


```
class cAmbientLight : iBaseLight
{
   float3            m_vLightColor;     
   bool     m_bEnable;
   float3 IlluminateAmbient(float3 vNormal);
   float3 IlluminateDiffuse(float3 vNormal);
   float3 IlluminateSpecular(float3 vNormal, int specularPower );
};

class cHemiAmbientLight : cAmbientLight
{
   float4   m_vGroundColor;
   float4   m_vDirUp;
   float3 IlluminateAmbient(float3 vNormal);
};        
      
```



## <a name="interface-instance-declarations-in-a-shader"></a>Dichiarazioni di istanze di interfaccia in uno shader

Un'istanza dell'interfaccia funge da segnaposto per le istanze di classe che forniscono un'implementazione dei metodi dell'interfaccia. L'uso di un'istanza di un'interfaccia consente al codice dello shader di chiamare un metodo senza sapere quale implementazione di tale metodo verrà richiamato. Il codice dello shader dichiara una o più istanze per ogni interfaccia definita. Queste istanze vengono usate nel codice dello shader in modo analogo ai puntatori della classe base C++.

Nell'esempio di codice dello shader seguente viene illustrato come dichiarare diverse istanze di interfaccia e utilizzarle nel codice dello shader.


```
// Declare interface instances
iBaseLight     g_abstractAmbientLighting;
iBaseLight     g_abstractDirectLighting;
iBaseMaterial  g_abstractMaterial;

struct PS_INPUT
{
    float4 vPosition : SV_POSITION;
    float3 vNormal   : NORMAL;
    float2 vTexcoord : TEXCOORD0;
};

float4 PSMain( PS_INPUT Input ) : SV_TARGET
{ 
    float3 Ambient = (float3)0.0f;       
    Ambient = g_abstractMaterial.GetAmbientColor( Input.vTexcoord ) *         
        g_abstractAmbientLighting.IlluminateAmbient( Input.vNormal );

    float3 Diffuse = (float3)0.0f;  
    Diffuse += g_abstractMaterial.GetDiffuseColor( Input.vTexcoord ) * 
        g_abstractDirectLighting.IlluminateDiffuse( Input.vNormal );

    float3 Specular = (float3)0.0f;   
    Specular += g_abstractDirectLighting.IlluminateSpecular( Input.vNormal, 
        g_abstractMaterial.GetSpecularPower() );
     
    float3 Lighting = saturate( Ambient + Diffuse + Specular );
     
    return float4(Lighting,1.0f); 
}
```



## <a name="class-instance-declarations-in-a-shader"></a>Dichiarazioni di istanze di classe in uno shader

Ogni classe che verrà usata al posto di un'istanza di interfaccia deve essere dichiarata come variabile in un buffer costante o creata dall'applicazione in fase di esecuzione usando il metodo [**ID3D11ClassLinkage:: CreateClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) . Alle istanze di interfaccia verranno indirizzate le istanze di classe nel codice dell'applicazione. È possibile fare riferimento alle istanze della classe nel codice dello shader come qualsiasi altra variabile, ma una classe derivata da un'interfaccia viene in genere usata solo con un'istanza di interfaccia e non vi verrà fatto riferimento direttamente dal codice dello shader.

Nell'esempio di codice dello shader riportato di seguito viene illustrata la dichiarazione di più istanze di classe.


```
cbuffer cbPerFrame : register( b0 )
{
   cAmbientLight     g_ambientLight;
   cHemiAmbientLight g_hemiAmbientLight;
   cDirectionalLight g_directionalLight;
   cEnvironmentLight g_environmentLight;
   float4            g_vEyeDir;   
};        
      
```



## <a name="initializing-interface-instances-in-an-application"></a>Inizializzazione di istanze di interfaccia in un'applicazione

Le istanze di interfaccia vengono inizializzate nel codice dell'applicazione passando una matrice di collegamento dinamico che contiene le assegnazioni di interfaccia a uno dei metodi [**sul ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) .

Per creare una matrice di collegamento dinamico, attenersi alla procedura seguente:

1.  Creare un oggetto collegamento di classe usando [**CreateClassLinkage**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage).
    ```
    ID3D11ClassLinkage* g_pPSClassLinkage = NULL;            
    pd3dDevice->CreateClassLinkage( &g_pPSClassLinkage );
              
    ```

    

2.  Creare lo shader che utilizzerà il collegamento alla classe dinamica, passando l'oggetto del collegamento alla classe come parametro alla funzione create dello shader.
    ```
    pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
        pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader ) );            
              
    ```

    

3.  Creare un oggetto [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) usando la funzione [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) .
    ```
    ID3D11ShaderReflection* pReflector = NULL; 
    D3DReflect( pPixelShaderBuffer->GetBufferPointer(),                  
        pPixelShaderBuffer->GetBufferSize(), 
        IID_ID3D11ShaderReflection, (void**) &pReflector) );            
              
    ```

    

4.  Usare l'oggetto Reflection shader per ottenere il numero di istanze di interfaccia nello shader usando il metodo [**ID3D11ShaderReflection:: GetNumInterfaceSlots**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) .
    ```
    g_iNumPSInterfaces = pReflector->GetNumInterfaceSlots();             
              
    ```

    

5.  Creare una matrice sufficientemente grande da mantenere il numero di istanze di interfaccia nello shader.
    ```
    ID3D11ClassInstance** g_dynamicLinkageArray = NULL;            
    g_dynamicLinkageArray = 
        (ID3D11ClassInstance**) malloc( sizeof(ID3D11ClassInstance*) * g_iNumPSInterfaces );            
              
    ```

    

6.  Determinare l'indice nella matrice corrispondente a ogni istanza dell'interfaccia utilizzando [**ID3D11ShaderReflection:: GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) e [**ID3D11ShaderReflectionVariable:: GetInterfaceSlot**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot).
    ```
    ID3D11ShaderReflectionVariable* pAmbientLightingVar = 
        pReflector->GetVariableByName("g_abstractAmbientLighting");
        g_iAmbientLightingOffset = pAmbientLightingVar->GetInterfaceSlot(0);            
              
    ```

    

7.  Ottenere un'istanza della classe per ogni oggetto classe derivato da un'interfaccia nello shader utilizzando [**ID3D11ClassLinkage:: GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance).
    ```
    g_pPSClassLinkage->GetClassInstance( "g_hemiAmbientLight", 0, 
        &g_pHemiAmbientLightClass );            
              
    ```

    

8.  Impostare le istanze di interfaccia sulle istanze della classe impostando la voce corrispondente nella matrice del collegamento dinamico.
    ```
    g_dynamicLinkageArray[g_iAmbientLightingOffset] = g_pHemiAmbientLightClass;            
              
    ```

    

9.  Passare la matrice di collegamento dinamico come parametro a una chiamata di seshader.
    ```
    pd3dImmediateContext->PSSetShader( g_pPixelShader, g_dynamicLinkageArray, g_iNumPSInterfaces );            
              
    ```

    

## <a name="related-topics"></a>Argomenti correlati

[Collegamento dinamico](overviews-direct3d-11-hlsl-dynamic-linking.md)