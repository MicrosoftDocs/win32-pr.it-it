---
title: Tipo struct
description: Tipo struct
ms.assetid: 896030b0-07cd-41bd-8c94-e173eabc81dd
keywords:
- Tipo di struct HLSL
topic_type:
- apiref
api_name:
- Struct Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89435e9c8757d2e732bc6237b02a508d3af4b4db
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119096"
---
# <a name="struct-type"></a>Tipo struct

Usare la sintassi seguente per dichiarare una struttura usando HLSL.

struct *Name*{ \[ *InterpolationModifier* \] *Type* \[ *R* x *C* \] *MemberName*;     ... };



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*
</dt> <dd>

Stringa ASCII che identifica in modo univoco il nome della struttura.

</dd> <dt>

<span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolazioneModifier*\]
</dt> <dd>

Modificatore facoltativo che specifica un tipo di interpolazione. Per [informazioni dettagliate, vedere](#remarks) Note.

</dd> <dt>

<span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Tipo* \[ *R* x *C*\]
</dt> <dd>

Tipo di membro con una riga facoltativa (*R*) x colonna (*C*) dimensione della matrice. Una struttura contiene almeno un elemento. se contiene più di un elemento, gli elementi sono tutti dello stesso tipo. Il numero di righe e colonne è unsigned integer compreso tra 1 e 4 inclusi.

</dd> <dt>

<span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*Membername*
</dt> <dd>

Stringa ASCII che identifica in modo univoco il nome del membro.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un modificatore di interpolazione può essere specificato in qualsiasi membro della struttura o in un argomento di una pixel shader funzione. Se un modificatore viene visualizzato in entrambe le posizioni, il modificatore outside (modificatore di argomento pixel shader) prevale sul modificatore inside (modificatore structure).

Quando si compila uno shader o un effetto, il compilatore shader esegue il pacchetto dei membri della struttura in base alle [regole di pacchetto HLSL.](dx-graphics-hlsl-packing-rules.md)

### <a name="interpolation-modifiers-introduced-in-shader-model-4"></a>Modificatori di interpolazione introdotti nel modello shader 4

Gli output di vertex shader usati per pixel shader input vengono interpolati in modo lineare per ottenere valori per pixel durante la rasterizzazione. Per impostare il metodo di interpolazione, usare uno dei valori seguenti, supportati nel modello [shader 4](dx-graphics-hlsl-sm4.md) o versione successiva. Il modificatore viene ignorato in qualsiasi output di vertex shader che non viene usato come input pixel shader di input.



| Modificatore di interpolazione | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Lineare**             | Eseguire l'interpolazione tra gli input dello shader; **linear** è il valore predefinito se non viene specificato alcun modificatore di interpolazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Baricentro**           | Interpolazione tra campioni che si trova in un punto qualsiasi all'interno dell'area coperta del pixel (potrebbe essere necessario estrapolare i punti finali da un centro pixel). Il campionamento centroide può migliorare l'antialiasing se un pixel è parzialmente coperto (anche se il centro pixel non è coperto). Il **modificatore centroid** deve essere combinato con il **modificatore lineare** **o noperspective.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **nointerpolazione**    | Non eseguire l'interpolazione di .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **noperspective**      | Non eseguire la correzione della prospettiva durante l'interpolazione. Il **modificatore noperspective** può essere combinato con il **modificatore centroid.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Esempio**             | **Disponibile nel modello shader 4.1 e versioni successive** Interpolare in corrispondenza della posizione del campione anziché al centro dei pixel. In questo modo il pixel shader viene eseguito per campione anziché per pixel. Un altro modo per causare l'esecuzione per campione è avere un input con [ \_ SV SampleIndex semantico,](dx-graphics-hlsl-semantics.md)che indica l'esempio corrente. Solo gli input  con il campione specificato (o l'input di SV SampleIndex) differiscono tra le chiamate dello shader nel pixel, mentre altri input che non specificano modificatori (ad esempio, se si combinano modificatori in input diversi) continuano a interpolare al centro \_ pixel. Sia pixel shader chiamate che test di profondità/stencil vengono eseguiti per ogni campione coperto nel pixel. Questa operazione è talvolta nota come *supersampling*. Al contrario, in assenza di una chiamata di frequenza di campionamento, nota come multicampionamento, il pixel shader viene richiamato una volta per pixel indipendentemente dal numero di campioni coperti, mentre i test di profondità/stencil si verificano alla *frequenza* del campione. Entrambe le modalità forniscono un antialiasing perimetrale equivalente. Tuttavia, il supercampionamento offre una migliore qualità di ombreggiatura richiamando l'pixel shader più frequentemente.<br/> |



 

<dl> 1. Quando si usa un tipo int/uint, l'unica opzione valida è **nointerpolation**.  
</dl>

I modificatori di interpolazione possono essere applicati ai membri della struttura o agli [argomenti di funzione](dx-graphics-hlsl-function-parameters.md)o a entrambi.

## <a name="examples"></a>Esempio

Di seguito sono riportati alcuni esempi di dichiarazioni di struttura.


```
struct struct1
{
  int    a;
}
```



Questa dichiarazione include una matrice.


```
struct struct2
{
  int    a;
  float  b;
  int4x4 iMatrix;
}
```



Questa dichiarazione include un modificatore di interpolazione.


```
struct In
{
  centroid float2 Texcoord;
};
```



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Tipi di dati (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





