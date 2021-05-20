---
title: Direttiva pragma message
description: Direttiva pragma che genera messaggi in fase di compilazione.
ms.assetid: dc3ece10-9730-4ab1-acc8-f95abc92de7d
keywords:
- Direttiva pragma message HLSL
topic_type:
- apiref
api_name:
- message pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 813483efb161a06db5ef7e40da99c391f53565bc
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153484"
---
# <a name="message-pragma-directive"></a>Direttiva pragma message

Direttiva pragma che genera messaggi in fase di compilazione.



| \#pragma message("*token-string*") |
|-----------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                    | Descrizione                  |
|-----------------------------------------------------------------------------------------|------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*<br/> | Messaggio del compilatore.<br/> |



 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata l'elaborazione dei messaggi durante la pre-elaborazione.


```
#pragma message "Debugging flag set."
```



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Direttive per il preprocessore (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Direttiva pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





