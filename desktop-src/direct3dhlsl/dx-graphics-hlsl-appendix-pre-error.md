---
title: " Error (direttiva)"
description: Direttiva per il preprocessore che produce messaggi di errore in fase di compilazione.
ms.assetid: e32bcd6f-f2c1-43f7-a0bb-2c384b056492
keywords:
- Direttiva di errore HLSL
topic_type:
- apiref
api_name:
- error Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 362150e494398abbc708416e6bfca6aa83756c52
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397670"
---
# <a name="error-directive"></a>\#Error (direttiva)

Direttiva per il preprocessore che produce messaggi di errore in fase di compilazione.



| \#*stringa di token di* errore |
|------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                    | Descrizione                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*stringa di token*<br/> | Messaggio di errore. Questo parametro è costituito da una serie di token, ad esempio parole chiave, costanti o istruzioni complete. La stringa del token è soggetta all'espansione della macro. <br/> |



 

## <a name="remarks"></a>Commenti

\#le direttive Error sono particolarmente utili per rilevare le incoerenze del programmatore e la violazione dei vincoli durante la pre-elaborazione. Quando \# viene rilevata una direttiva di errore, la compilazione viene terminata.

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

 

 





