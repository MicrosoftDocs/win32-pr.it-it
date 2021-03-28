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
# <a name="interfaces-and-classes"></a><span data-ttu-id="7cd61-103">Interfacce e classi</span><span class="sxs-lookup"><span data-stu-id="7cd61-103">Interfaces and classes</span></span>

<span data-ttu-id="7cd61-104">Il collegamento dinamico dello shader usa le interfacce HLSL (High-Level Shader Language) e le classi sintatticamente simili alle relative controparti C++.</span><span class="sxs-lookup"><span data-stu-id="7cd61-104">Dynamic shader linkage makes use of high-level shader language (HLSL) interfaces and classes that are syntactically similar to their C++ counterparts.</span></span> <span data-ttu-id="7cd61-105">Ciò consente agli shader di fare riferimento a istanze di interfaccia astratte in fase di compilazione e di lasciare la risoluzione di tali istanze a classi concrete per l'applicazione in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7cd61-105">This allows shaders to reference abstract interface instances at compile time and leave resolution of those instances to concrete classes for the application at runtime.</span></span>

<span data-ttu-id="7cd61-106">Le sezioni seguenti illustrano in dettaglio come configurare uno shader per l'uso di interfacce e classi e come inizializzare le istanze dell'interfaccia nel codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7cd61-106">The following sections detail how to setup a shader to use interfaces and classes and how to initialize interface instances in application code.</span></span>

-   [<span data-ttu-id="7cd61-107">Dichiarazione di interfacce</span><span class="sxs-lookup"><span data-stu-id="7cd61-107">Declaring Interfaces</span></span>](#declaring-interfaces)
-   [<span data-ttu-id="7cd61-108">Dichiarazione di classi</span><span class="sxs-lookup"><span data-stu-id="7cd61-108">Declaring Classes</span></span>](#declaring-classes)
-   [<span data-ttu-id="7cd61-109">Dichiarazioni di istanze di interfaccia in uno shader</span><span class="sxs-lookup"><span data-stu-id="7cd61-109">Interface Instance Declarations in a Shader</span></span>](#interface-instance-declarations-in-a-shader)
-   [<span data-ttu-id="7cd61-110">Dichiarazioni di istanze di classe in uno shader</span><span class="sxs-lookup"><span data-stu-id="7cd61-110">Class Instance Declarations in a Shader</span></span>](#class-instance-declarations-in-a-shader)
-   [<span data-ttu-id="7cd61-111">Inizializzazione di istanze di interfaccia in un'applicazione</span><span class="sxs-lookup"><span data-stu-id="7cd61-111">Initializing Interface Instances in an Application</span></span>](#initializing-interface-instances-in-an-application)
-   [<span data-ttu-id="7cd61-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7cd61-112">Related topics</span></span>](#related-topics)

## <a name="declaring-interfaces"></a><span data-ttu-id="7cd61-113">Dichiarazione di interfacce</span><span class="sxs-lookup"><span data-stu-id="7cd61-113">Declaring interfaces</span></span>

<span data-ttu-id="7cd61-114">Un'interfaccia funziona in modo simile a una classe di base astratta in C++.</span><span class="sxs-lookup"><span data-stu-id="7cd61-114">An interface functions in a similar manner to an abstract base class in C++.</span></span> <span data-ttu-id="7cd61-115">Un'interfaccia viene dichiarata in uno shader usando la parola chiave Interface e contiene solo dichiarazioni di metodo.</span><span class="sxs-lookup"><span data-stu-id="7cd61-115">An interface is declared in a shader using the interface keyword and only contains method declarations.</span></span> <span data-ttu-id="7cd61-116">I metodi dichiarati in un'interfaccia saranno tutti metodi virtuali in tutte le classi derivate dall'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7cd61-116">The methods declared in an interface will all be virtual methods in any classes derived from the interface.</span></span> <span data-ttu-id="7cd61-117">Le classi derivate devono implementare tutti i metodi dichiarati in un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7cd61-117">Derived classes must implement all methods declared in an interface.</span></span> <span data-ttu-id="7cd61-118">Si noti che le interfacce sono l'unico modo per dichiarare i metodi virtuali, non esiste una parola chiave virtuale come in C++ e le classi connot dichiarano metodi virtuali.</span><span class="sxs-lookup"><span data-stu-id="7cd61-118">Note that interfaces are the only way to declare virtual methods, there is no virtual keyword as in C++, and classes connot declare virtual methods.</span></span>

<span data-ttu-id="7cd61-119">Nell'esempio di codice dello shader seguente vengono dichiarate due interfacce.</span><span class="sxs-lookup"><span data-stu-id="7cd61-119">The following example shader code declares two interfaces.</span></span>


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



## <a name="declaring-classes"></a><span data-ttu-id="7cd61-120">Dichiarazione di classi</span><span class="sxs-lookup"><span data-stu-id="7cd61-120">Declaring Classes</span></span>

<span data-ttu-id="7cd61-121">Una classe si comporta in modo analogo alle classi in C++.</span><span class="sxs-lookup"><span data-stu-id="7cd61-121">A class behaves in a similar manner to classes in C++.</span></span> <span data-ttu-id="7cd61-122">Una classe viene dichiarata con la parola chiave Class e può contenere variabili membro e metodi.</span><span class="sxs-lookup"><span data-stu-id="7cd61-122">A class is declared with the class keyword and can contain member variables and methods.</span></span> <span data-ttu-id="7cd61-123">Una classe può ereditare da zero o una classe e da zero o più interfacce.</span><span class="sxs-lookup"><span data-stu-id="7cd61-123">A class can inherit from zero or one class and zero or more interfaces.</span></span> <span data-ttu-id="7cd61-124">Le classi devono implementare o ereditare implementazioni per tutte le interfacce nella catena di ereditarietà oppure non è possibile creare un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="7cd61-124">Classes must implement or inherit implementations for all interfaces in its inheritance chain or the class cannot be instantiated.</span></span>

<span data-ttu-id="7cd61-125">Nell'esempio di codice dello shader seguente viene illustrato come derivare una classe da un'interfaccia e da un'altra classe.</span><span class="sxs-lookup"><span data-stu-id="7cd61-125">The following example shader code illustrates deriving a class from an interface and from another class.</span></span>


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



## <a name="interface-instance-declarations-in-a-shader"></a><span data-ttu-id="7cd61-126">Dichiarazioni di istanze di interfaccia in uno shader</span><span class="sxs-lookup"><span data-stu-id="7cd61-126">Interface Instance Declarations in a Shader</span></span>

<span data-ttu-id="7cd61-127">Un'istanza dell'interfaccia funge da segnaposto per le istanze di classe che forniscono un'implementazione dei metodi dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7cd61-127">An interface instance acts as a place holder for class instances that provide an implementation of the interface's methods.</span></span> <span data-ttu-id="7cd61-128">L'uso di un'istanza di un'interfaccia consente al codice dello shader di chiamare un metodo senza sapere quale implementazione di tale metodo verrà richiamato.</span><span class="sxs-lookup"><span data-stu-id="7cd61-128">Using an instance of an interface allows shader code to call a method without knowing which implementation of that method will be invoked.</span></span> <span data-ttu-id="7cd61-129">Il codice dello shader dichiara una o più istanze per ogni interfaccia definita.</span><span class="sxs-lookup"><span data-stu-id="7cd61-129">Shader code declares one or more instances for each interface it defines.</span></span> <span data-ttu-id="7cd61-130">Queste istanze vengono usate nel codice dello shader in modo analogo ai puntatori della classe base C++.</span><span class="sxs-lookup"><span data-stu-id="7cd61-130">These instances are used in shader code in a similar manner to C++ base class pointers.</span></span>

<span data-ttu-id="7cd61-131">Nell'esempio di codice dello shader seguente viene illustrato come dichiarare diverse istanze di interfaccia e utilizzarle nel codice dello shader.</span><span class="sxs-lookup"><span data-stu-id="7cd61-131">The following example shader code illustrates declaring several interface instances and using them in shader code.</span></span>


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



## <a name="class-instance-declarations-in-a-shader"></a><span data-ttu-id="7cd61-132">Dichiarazioni di istanze di classe in uno shader</span><span class="sxs-lookup"><span data-stu-id="7cd61-132">Class Instance Declarations in a Shader</span></span>

<span data-ttu-id="7cd61-133">Ogni classe che verrà usata al posto di un'istanza di interfaccia deve essere dichiarata come variabile in un buffer costante o creata dall'applicazione in fase di esecuzione usando il metodo [**ID3D11ClassLinkage:: CreateClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) .</span><span class="sxs-lookup"><span data-stu-id="7cd61-133">Each class that will be used in place of an interface instance must either be declared as a variable in a constant buffer or created by the application at runtime using the [**ID3D11ClassLinkage::CreateClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) method.</span></span> <span data-ttu-id="7cd61-134">Alle istanze di interfaccia verranno indirizzate le istanze di classe nel codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7cd61-134">Interface instances will be pointed at class instances in the application code.</span></span> <span data-ttu-id="7cd61-135">È possibile fare riferimento alle istanze della classe nel codice dello shader come qualsiasi altra variabile, ma una classe derivata da un'interfaccia viene in genere usata solo con un'istanza di interfaccia e non vi verrà fatto riferimento direttamente dal codice dello shader.</span><span class="sxs-lookup"><span data-stu-id="7cd61-135">Class instances can be referenced in shader code like any other variable, but a class that is derived from an interface will typically only be used with an interface instance and will not be referenced by shader code directly.</span></span>

<span data-ttu-id="7cd61-136">Nell'esempio di codice dello shader riportato di seguito viene illustrata la dichiarazione di più istanze di classe.</span><span class="sxs-lookup"><span data-stu-id="7cd61-136">The following example shader code illustrates declaring several class instances.</span></span>


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



## <a name="initializing-interface-instances-in-an-application"></a><span data-ttu-id="7cd61-137">Inizializzazione di istanze di interfaccia in un'applicazione</span><span class="sxs-lookup"><span data-stu-id="7cd61-137">Initializing Interface Instances in an Application</span></span>

<span data-ttu-id="7cd61-138">Le istanze di interfaccia vengono inizializzate nel codice dell'applicazione passando una matrice di collegamento dinamico che contiene le assegnazioni di interfaccia a uno dei metodi [**sul ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="7cd61-138">Interface instances are initialized in application code by passing a dynamic linkage array containing interface assignments to one of the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) SetShader methods.</span></span>

<span data-ttu-id="7cd61-139">Per creare una matrice di collegamento dinamico, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="7cd61-139">To create a dynamic linkage array use the following steps</span></span>

1.  <span data-ttu-id="7cd61-140">Creare un oggetto collegamento di classe usando [**CreateClassLinkage**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage).</span><span class="sxs-lookup"><span data-stu-id="7cd61-140">Create a class linkage object using [**CreateClassLinkage**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage).</span></span>
    ```
    ID3D11ClassLinkage* g_pPSClassLinkage = NULL;            
    pd3dDevice->CreateClassLinkage( &g_pPSClassLinkage );
              
    ```

    

2.  <span data-ttu-id="7cd61-141">Creare lo shader che utilizzerà il collegamento alla classe dinamica, passando l'oggetto del collegamento alla classe come parametro alla funzione create dello shader.</span><span class="sxs-lookup"><span data-stu-id="7cd61-141">Create the shader that will be using dynamic class linking, passing the class linkage object as a parameter to the shader's create function.</span></span>
    ```
    pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
        pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader ) );            
              
    ```

    

3.  <span data-ttu-id="7cd61-142">Creare un oggetto [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) usando la funzione [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) .</span><span class="sxs-lookup"><span data-stu-id="7cd61-142">Create a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) object using the [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) function.</span></span>
    ```
    ID3D11ShaderReflection* pReflector = NULL; 
    D3DReflect( pPixelShaderBuffer->GetBufferPointer(),                  
        pPixelShaderBuffer->GetBufferSize(), 
        IID_ID3D11ShaderReflection, (void**) &pReflector) );            
              
    ```

    

4.  <span data-ttu-id="7cd61-143">Usare l'oggetto Reflection shader per ottenere il numero di istanze di interfaccia nello shader usando il metodo [**ID3D11ShaderReflection:: GetNumInterfaceSlots**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) .</span><span class="sxs-lookup"><span data-stu-id="7cd61-143">Use the shader reflection object to get the number of interface instances in the shader using the [**ID3D11ShaderReflection::GetNumInterfaceSlots**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) method.</span></span>
    ```
    g_iNumPSInterfaces = pReflector->GetNumInterfaceSlots();             
              
    ```

    

5.  <span data-ttu-id="7cd61-144">Creare una matrice sufficientemente grande da mantenere il numero di istanze di interfaccia nello shader.</span><span class="sxs-lookup"><span data-stu-id="7cd61-144">Create an array large enough to hold the number of interface instances in the shader.</span></span>
    ```
    ID3D11ClassInstance** g_dynamicLinkageArray = NULL;            
    g_dynamicLinkageArray = 
        (ID3D11ClassInstance**) malloc( sizeof(ID3D11ClassInstance*) * g_iNumPSInterfaces );            
              
    ```

    

6.  <span data-ttu-id="7cd61-145">Determinare l'indice nella matrice corrispondente a ogni istanza dell'interfaccia utilizzando [**ID3D11ShaderReflection:: GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) e [**ID3D11ShaderReflectionVariable:: GetInterfaceSlot**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot).</span><span class="sxs-lookup"><span data-stu-id="7cd61-145">Determine the index in the array that corresponds to each interface instance using [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) and [**ID3D11ShaderReflectionVariable::GetInterfaceSlot**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot).</span></span>
    ```
    ID3D11ShaderReflectionVariable* pAmbientLightingVar = 
        pReflector->GetVariableByName("g_abstractAmbientLighting");
        g_iAmbientLightingOffset = pAmbientLightingVar->GetInterfaceSlot(0);            
              
    ```

    

7.  <span data-ttu-id="7cd61-146">Ottenere un'istanza della classe per ogni oggetto classe derivato da un'interfaccia nello shader utilizzando [**ID3D11ClassLinkage:: GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance).</span><span class="sxs-lookup"><span data-stu-id="7cd61-146">Get a class instance for each class object derived from an interface in the shader using [**ID3D11ClassLinkage::GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance).</span></span>
    ```
    g_pPSClassLinkage->GetClassInstance( "g_hemiAmbientLight", 0, 
        &g_pHemiAmbientLightClass );            
              
    ```

    

8.  <span data-ttu-id="7cd61-147">Impostare le istanze di interfaccia sulle istanze della classe impostando la voce corrispondente nella matrice del collegamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="7cd61-147">Set interface instances to class instances by setting the corresponding entry in the dynamic linkage array.</span></span>
    ```
    g_dynamicLinkageArray[g_iAmbientLightingOffset] = g_pHemiAmbientLightClass;            
              
    ```

    

9.  <span data-ttu-id="7cd61-148">Passare la matrice di collegamento dinamico come parametro a una chiamata di seshader.</span><span class="sxs-lookup"><span data-stu-id="7cd61-148">Pass the dynamic linkage array as a parameter to a SetShader call.</span></span>
    ```
    pd3dImmediateContext->PSSetShader( g_pPixelShader, g_dynamicLinkageArray, g_iNumPSInterfaces );            
              
    ```

    

## <a name="related-topics"></a><span data-ttu-id="7cd61-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7cd61-149">Related topics</span></span>

[<span data-ttu-id="7cd61-150">Collegamento dinamico</span><span class="sxs-lookup"><span data-stu-id="7cd61-150">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)