---
title: " Direttiva error"
description: Direttiva del preprocessore che genera messaggi di errore in fase di compilazione.
ms.assetid: e32bcd6f-f2c1-43f7-a0bb-2c384b056492
keywords:
- Direttiva error HLSL
topic_type:
- apiref
api_name:
- error Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5fa1af02a693b5168a2d96e653726fd0a468587bf2b8c1825afbf8e73057f61f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068331"
---
# <a name="error-directive"></a>\#Direttiva error

Direttiva del preprocessore che genera messaggi di errore in fase di compilazione.



| \#*token-string di errore* |
|------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                    | Descrizione                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*<br/> | Messaggio di errore. Questo parametro è costituito da una serie di token, ad esempio parole chiave, costanti o istruzioni complete. La stringa del token è soggetta all'espansione della macro. <br/> |



 

## <a name="remarks"></a>Commenti

\#Le direttive error sono particolarmente utili per rilevare le incoerenze del programmatore e la violazione dei vincoli durante la pre-elaborazione. Quando viene \# rilevata una direttiva error, la compilazione termina.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata l'elaborazione degli errori durante la pre-elaborazione.


```
#if !defined(__cplusplus)
  #error C++ compiler required.
#endif
```



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Direttive per il preprocessore (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





