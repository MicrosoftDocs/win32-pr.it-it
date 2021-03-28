---
title: register
description: register
ms.assetid: 45149f8c-8b76-4247-98d7-d141d7268da3
keywords:
- Registra HLSL
topic_type:
- apiref
api_name:
- register
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b378cd97bc9779951d62873d393009c98d32823
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399055"
---
# <a name="register"></a>register

Parola chiave facoltativa per l'assegnazione di una variabile shader a un particolare registro, che usa la sintassi seguente:



| : Register ( *\[ \_ profilo \] shader*, *tipo \# \[ sottocomponente \]* ) |
|----------------------------------------------------------------|



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="register"></span><span id="REGISTER"></span>Registro
</dt> <dd>

Parola chiave required.

</dd> <dt>

<span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[profilo shader \_\]*
</dt> <dd>

[Profilo shader](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)facoltativo, che può essere una destinazione shader o semplicemente **PS** o **vs**.

</dd> <dt>

<span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*Sottocomponente di tipo \# \[\]*
</dt> <dd>

Tipo di registrazione, numero e dichiarazione di sottocomponente.

-   Il tipo è uno dei seguenti:

    

    | Tipo | Descrizione registro       |
    |------|----------------------------|
    | b    | Buffer costante            |
    | u    | Trama e buffer di trama |
    | c    | Offset del buffer              |
    | s    | Campionatore                    |
    | u    | Unordered Access View      |

    

     

-   *\#* numero del registro, ovvero un numero intero.
-   Il *sottocomponente* è un numero intero facoltativo.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile aggiungere una o più assegnazioni di registro alla stessa dichiarazione di variabile, separate da spazi.

Per le variabili Direct3D 10 nell'ambito globale, la parola chiave **Register** funziona come la parola chiave [PACKOFFSET (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .

## <a name="examples"></a>Esempio

Ecco alcuni esempi:


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

 

 