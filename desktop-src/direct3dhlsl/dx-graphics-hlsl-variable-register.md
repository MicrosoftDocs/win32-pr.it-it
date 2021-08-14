---
title: register
description: register
ms.assetid: 45149f8c-8b76-4247-98d7-d141d7268da3
keywords:
- registrare HLSL
topic_type:
- apiref
api_name:
- register
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0102716529471b3e867e17b0e9b635274cdfc28ec603f239d66c76ffb0fdaa19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983211"
---
# <a name="register"></a>register

Parola chiave facoltativa per l'assegnazione di una variabile shader a un registro specifico, che usa la sintassi seguente:



| : register ( *\[ profilo shader, \_ \]* *\# \[ sottocomponente Type \]* ) |
|----------------------------------------------------------------|



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="register"></span><span id="REGISTER"></span>Registro
</dt> <dd>

Parola chiave obbligatoria.

</dd> <dt>

<span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[Profilo \_ shader\]*
</dt> <dd>

Profilo [shader facoltativo,](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)che può essere una destinazione shader o semplicemente **ps** **o vs**.

</dd> <dt>

<span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*\# \[ Sottocomponente type\]*
</dt> <dd>

Registrare la dichiarazione di tipo, numero e sottocomponente.

-   Il tipo è uno dei seguenti:

    

    | Tipo | Descrizione del registro       |
    |------|----------------------------|
    | b    | Buffer costante            |
    | t    | Buffer trame e trame |
    | c    | Offset del buffer              |
    | s    | Campionatore                    |
    | u    | Unordered Access View      |

    

     

-   *\#* è il numero di registro, ovvero un numero intero.
-   Il *sottocomponente* è un numero intero facoltativo.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile aggiungere una o più assegnazioni di registro alla stessa dichiarazione di variabile, separate da spazi.

Per le variabili Direct3D 10 nell'ambito globale, la parola chiave **register** agisce come la parola chiave [packoffset (DirectX HLSL).](dx-graphics-hlsl-variable-packoffset.md)

## <a name="examples"></a>Esempio

Di seguito sono riportati alcuni esempi:


```
sampler myVar : register( ps_5_0, s ); 
```




```
sampler myVar : register( vs, s[8] );
```




```
sampler myVar : register( ps, s[2] ) 
              : register( ps_5_0, s[0] ) 
              : register( vs, s[8] );
```



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi delle variabili](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[Variabili (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 