---
title: Interfacce e classi negli effetti
description: Esistono diversi modi per usare le classi e le interfacce in Effects 11.
ms.assetid: 526d477b-fc1f-4bd0-a620-ce9b78147f68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b067b8e03b2d43ea44ccab6164424cbc84c7237
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399229"
---
# <a name="interfaces-and-classes-in-effects"></a>Interfacce e classi negli effetti

Esistono diversi modi per usare le classi e le interfacce in Effects 11. Per la sintassi dell'interfaccia e della classe, vedere [interfacce e classi](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).

Le sezioni seguenti illustrano in dettaglio come specificare le istanze di classe per uno shader che usa le interfacce. Negli esempi si useranno le seguenti interfacce e classi:


```
interface IColor
{
  float4 GetColor();
};

class CRed : IColor
{
  float4 GetColor() { return float4(1,0,0,1); }
};
class CGreen : IColor
{
  float4 GetColor() { return float4(0,1,0,1); }
};

CRed pRed;
CGreen pGreen;
IColor pIColor;
IColor pIColor2 = pRed;
```



Si noti che le istanze dell'interfaccia possono essere inizializzate in istanze di classe. Sono supportate anche matrici di classi e istanze di interfaccia che possono essere inizializzate come nell'esempio seguente:


```
CRed pRedArray[2];
IColor pIColor3 = pRedArray[1];
IColor pIColorArray[2] = {pRed, pGreen};
IColor pIColorArray2[2] = pRedArray;
```



## <a name="uniform-interface-parameters"></a>Parametri dell'interfaccia uniforme

Analogamente ad altri tipi di dati uniformi, è necessario specificare parametri di interfaccia uniformi nella chiamata CompileShader. I parametri di interfaccia possono essere assegnati a istanze di interfaccia globali o a istanze di classe globali. Quando viene assegnato a un'istanza dell'interfaccia globale, lo shader avrà una dipendenza dall'istanza dell'interfaccia, il che significa che deve essere impostato su un'istanza della classe. Quando vengono assegnate a istanze di classe globali, il compilatore specializza lo shader (come con altri tipi di dati uniformi) per usare tale classe. Questa operazione è importante per due scenari:

1.  Gli shader con una \_ destinazione 4 x possono usare i parametri di interfaccia se questi parametri sono uniformi e assegnati alle istanze di classe globali (pertanto non viene usato alcun collegamento dinamico).
2.  Gli utenti possono decidere di avere molti shader compilati e specializzati senza collegamento dinamico o con pochi shader compilati con collegamento dinamico.


```
float4 PSUniform( uniform IColor color ) : SV_Target
{
  return color;
}

technique11
{
  pass
  {
    SetPixelShader( CompileShader( ps_4_0, PSUniform(pRed) ) );
  }
  pass
  {
    SetPixelShader( CompileShader( ps_5_0, PSUniform(pIColor2) ) );
  }
}
```



Se pIColor2 rimane invariato tramite l'API, le due passate precedenti sono funzionalmente equivalenti, ma il primo usa uno \_ \_ shader statico PS 4 0 mentre il secondo usa uno \_ shader PS 5 \_ 0 con collegamento dinamico. Se pIColor2 viene modificato tramite l'API Effects (vedere l'impostazione delle istanze della classe di seguito), il comportamento del pixel shader nel secondo passaggio potrebbe cambiare.

## <a name="non-uniform-interface-parameters"></a>Parametri di interfaccia non uniformi

I parametri di interfaccia non uniformi creano dipendenze dell'interfaccia per gli shader. Quando si applica uno shader con parametri di interfaccia, questi parametri devono essere assegnati in con la chiamata BindInterfaces. Le istanze di interfaccia globali e le istanze della classe globale possono essere specificate nella chiamata BindInterfaces.


```
float4 PSAbstract( IColor color ) : SV_Target
{
  return color;
}

PixelShader pPSAbstract = CompileShader( ps_5_0, PSAbstract(pRed) );

technique11
{
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pRed ) );
  }
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pIColor2 ) );
  }
}
```



Se pIColor2 rimane invariato tramite l'API, le due passate precedenti sono funzionalmente equivalenti e usano il collegamento dinamico. Se pIColor2 viene modificato tramite l'API Effects (vedere l'impostazione delle istanze della classe di seguito), il comportamento del pixel shader nel secondo passaggio potrebbe cambiare.

## <a name="setting-class-instances"></a>Impostazione delle istanze della classe

Quando si imposta uno shader con collegamento dello shader dinamico sul dispositivo Direct3D 11, è necessario specificare anche le istanze della classe. È un errore impostare tale shader con un'istanza della classe **null** . Pertanto, tutte le istanze di interfaccia a cui fa riferimento uno shader devono disporre di un'istanza della classe associata.

Nell'esempio seguente viene illustrato come ottenere una variabile di istanza di classe da un effetto e come impostarla su una variabile di interfaccia:


```
ID3DX11EffectPass* pPass = pEffect->GetTechniqueByIndex(0)->GetPassByIndex(1);

ID3DX11EffectInterfaceVariable* pIface = pEffect->GetVariableByName( "pIColor2" )->AsInterface();
ID3DX11EffectClassInstanceVariable* pCI = pEffect->GetVariableByName( "pGreen" )->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );

// Apply the same pass with a different class instance
pCI = pEffect->GetVariableByName( "pRedArray" )->GetElement(1)->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 