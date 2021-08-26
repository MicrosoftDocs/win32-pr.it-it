---
title: " Direttive ifdef e ifndef"
description: Direttive per il preprocessore che determinano se è definita una macro o una costante del preprocessore specifica.
ms.assetid: c1cc2e1d-2599-45ec-9629-56c4b42e0d0e
keywords:
- Direttive ifdef e ifndef HLSL
topic_type:
- apiref
api_name:
- ifdef and ifndef Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 584cde8856c48aeafed5665016a71146f8c2ffb341b837faa6bf35d627152c39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068321"
---
# <a name="ifdef-and-ifndef-directives"></a>\#Direttive ifdef \# e ifndef

Direttive per il preprocessore che determinano se è definita una macro o una costante del preprocessore specifica.



| \#Identificatore *ifdef* ...  |
|---------------------------|
| \#endif                   |
| \#Identificatore *ifndef* ... |
| \#endif                   |



 

## <a name="parameters"></a>Parametri



| Elemento                                                                              | Descrizione                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*Identificatore*<br/> | Identificatore della costante o della macro da controllare. <br/> |



 

## <a name="remarks"></a>Commenti

È possibile usare le \# direttive ifdef \# e ifndef ovunque sia possibile usare [ \# se](dx-graphics-hlsl-appendix-pre-if.md) . \#L'istruzione ifdef equivale alla direttiva ). Queste direttive verificano solo la presenza o l'assenza di identificatori definiti tramite la direttiva [ \# define,](dx-graphics-hlsl-appendix-pre-define.md) non per gli identificatori dichiarati nel codice sorgente C o C++.

Queste direttive sono fornite solo per compatibilità con le versioni precedenti del linguaggio. È preferibile usare [l'operatore](dx-graphics-hlsl-appendix-pre-if.md) definito con \# la direttiva if.

La \# direttiva ifndef verifica l'opposto della condizione controllata da \# ifdef. Se l'identificatore non è definito, la condizione è true (diverso da zero). in caso contrario, la condizione è false (zero).

## <a name="examples"></a>Esempio

L'identifier può essere passato dalla riga di comando utilizzando l'opzione /D. È possibile specificare fino a 30 macro utilizzando /D. Ciò è utile per controllare l'esistenza di una definizione poiché una definizione può essere passata dalla riga di comando. Nell'esempio seguente viene utilizzato questo comportamento per determinare se eseguire un'applicazione in modalità test.


```
// PROG.CPP
#ifndef test
  #define final
#endif
int main()
{
}
```



Quando viene compilato con il comando seguente, prog.cpp verrà compilato in modalità test. In caso contrario, verrà compilato in modalità finale.


```
CL.EXE /Dtest prog.cpp
```



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Direttive per il preprocessore (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#se, )](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





