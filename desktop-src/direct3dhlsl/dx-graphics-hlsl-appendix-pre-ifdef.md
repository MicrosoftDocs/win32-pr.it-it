---
title: " Direttive ifdef e ifndef"
description: Direttive per il preprocessore che determinano se una specifica costante o macro del preprocessore è definita.
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
ms.openlocfilehash: 338308b58f1cdc68ec78984e65ffbf056a36b10b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045742"
---
# <a name="ifdef-and-ifndef-directives"></a>\#\#direttive ifdef e ifndef

Direttive per il preprocessore che determinano se una specifica costante o macro del preprocessore è definita.



| \#*identificatore* ifdef...  |
|---------------------------|
| \#endif                   |
| \#*identificatore* ifndef... |
| \#endif                   |



 

## <a name="parameters"></a>Parametri



| Elemento                                                                              | Descrizione                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*identificatore*<br/> | Identificatore della costante o della macro da verificare. <br/> |



 

## <a name="remarks"></a>Commenti

È possibile utilizzare le \# \# direttive ifdef e ifndef in qualsiasi punto [ \# ](dx-graphics-hlsl-appendix-pre-if.md) in cui è possibile utilizzare. L' \# istruzione ifdef è equivalente alla direttiva. Queste direttive controllano solo la presenza o l'assenza di identificatori definiti usando la direttiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) , non per gli identificatori dichiarati nel codice sorgente C o C++.

Queste direttive sono fornite solo per compatibilità con le versioni precedenti del linguaggio. È preferibile usare l'operatore [definito](dx-graphics-hlsl-appendix-pre-if.md) con la \# direttiva if.

La \# direttiva ifndef controlla l'opposto della condizione controllata da \# ifdef. Se l'identificatore non è definito, la condizione è true (diverso da zero); in caso contrario, la condizione è false (zero).

## <a name="examples"></a>Esempio

L'identifier può essere passato dalla riga di comando utilizzando l'opzione /D. È possibile specificare fino a 30 macro utilizzando /D. Ciò è utile per controllare l'esistenza di una definizione poiché una definizione può essere passata dalla riga di comando. Nell'esempio seguente viene usato questo comportamento per determinare se eseguire un'applicazione in modalità test.


```
// PROG.CPP
#ifndef test
  #define final
#endif
int main()
{
}
```



Quando viene compilato usando il comando seguente, PROG. cpp verrà compilato in modalità test. in caso contrario, verrà compilato in modalità finale.


```
CL.EXE /Dtest prog.cpp
```



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Direttive per il preprocessore (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Se,)](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





