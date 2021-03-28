---
title: Tipo struct
description: Tipo struct
ms.assetid: 896030b0-07cd-41bd-8c94-e173eabc81dd
keywords:
- Tipo struct HLSL
topic_type:
- apiref
api_name:
- Struct Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416c14c18fa1d0b76f4d13b609b895b0c64c2594
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104992904"
---
# <a name="struct-type"></a>Tipo struct

Utilizzare la sintassi seguente per dichiarare una struttura utilizzando HLSL.



|                                                                                           |
|-------------------------------------------------------------------------------------------|
| *nome* struct { \[ *InterpolationModifier* \] *Type* \[ *R* x *C* \] *memberName*;     ... }; |



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*
</dt> <dd>

Stringa ASCII che identifica in modo univoco il nome della struttura.

</dd> <dt>

<span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]
</dt> <dd>

Modificatore facoltativo che specifica un tipo di interpolazione. Per informazioni dettagliate, vedere la [sezione Osservazioni](#remarks) .

</dd> <dt>

<span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Tipo* \[ di *R* x *C*\]
</dt> <dd>

Tipo di membro con una matrice di colonne (*C*) di riga facoltativa (*R*). Una struttura contiene almeno un elemento. Se contiene più di un elemento, gli elementi sono tutti dello stesso tipo. Il numero di righe e colonne è costituito da interi senza segno compreso tra 1 e 4 inclusi.

</dd> <dt>

<span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*MemberName*
</dt> <dd>

Stringa ASCII che identifica in modo univoco il nome del membro.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile specificare un modificatore di interpolazione per qualsiasi membro della struttura o per un argomento di una funzione pixel shader. Se un modificatore viene visualizzato in entrambe le posizioni, il modificatore esterno (il modificatore di argomento pixel shader) sovraregola il modificatore interno (il modificatore di struttura).

Quando si compila uno shader o un effetto, il compilatore shader comprime i membri della struttura in base alle [regole di compressione HLSL](dx-graphics-hlsl-packing-rules.md).

### <a name="interpolation-modifiers-introduced-in-shader-model-4"></a>Modificatori di interpolazione introdotti in Shader Model 4

Gli output di vertex shader usati per gli input pixel shader vengono interpolati linearmente per ottenere i valori per pixel durante la rasterizzazione. Per impostare il metodo di interpolazione, usare uno dei valori seguenti, supportati in [Shader Model 4](dx-graphics-hlsl-sm4.md) o versione successiva. Il modificatore viene ignorato in qualsiasi output del vertex shader che non viene usato come input pixel shader.



| Modificatore di interpolazione | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **lineare**             | Interpolazione tra input shader; **Linear** è il valore predefinito se non è specificato alcun modificatore di interpolazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **centro**           | Interpolare tra i campioni che si trovano in un punto qualsiasi all'interno dell'area coperta del pixel (potrebbe essere necessario estrapolare i punti finali da un pixel Center). Il campionamento centrale può migliorare l'anti-aliasing se un pixel è parzialmente analizzato (anche se il pixel Center non è coperto). Il modificatore di **baricentro** deve essere combinato con il modificatore **Linear** o **noperspective** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **interpolazione**    | Non eseguire l'interpolazione.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **noperspective**      | Non eseguire la correzione della prospettiva durante l'interpolazione. Il modificatore **noperspective** può essere combinato con il modificatore di **baricentro** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **esempio**             | **Disponibile nel modello di shader 4,1 e versioni successive** Interpolare in un percorso di esempio anziché in un pixel Center. In questo modo il pixel shader viene eseguito per campione anziché per pixel. Un altro modo per eseguire l'esecuzione per campione è avere un input con la [semantica SV \_ SampleIndex](dx-graphics-hlsl-semantics.md), che indica l'esempio corrente. Solo gli input con l' **esempio** specificato (o inserendo SV \_ SampleIndex) variano tra le chiamate dello shader nel pixel, mentre altri input che non specificano i modificatori (ad esempio, se si combinano i modificatori su input diversi) ancora interpolano in corrispondenza del pixel Center. Per ogni esempio incluso nel pixel si verificano sia la chiamata del pixel shader che il test di profondità/stencil. Questa operazione è talvolta nota come *supercampionamento*. Al contrario, in assenza della chiamata di frequenza di esempio, nota come *multicampionamento*, il pixel shader viene richiamato una volta per ogni pixel indipendentemente dal numero di campioni analizzati, mentre il test di profondità/stencil si verifica alla frequenza di campionamento. Entrambe le modalità forniscono l'anti-aliasing Edge equivalente. Tuttavia, il supercampionamento offre una migliore qualità di ombreggiatura richiamando il pixel shader più spesso.<br/> |



 

<dl> 1. Quando si usa un tipo int/uint, l'unica opzione valida è **Interpolation**.  
</dl>

È possibile applicare i modificatori di interpolazione a membri della struttura o [argomenti di funzione](dx-graphics-hlsl-function-parameters.md)o a entrambi.

## <a name="examples"></a>Esempio

Di seguito sono riportate alcune dichiarazioni di struttura di esempio.


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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di dati (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





