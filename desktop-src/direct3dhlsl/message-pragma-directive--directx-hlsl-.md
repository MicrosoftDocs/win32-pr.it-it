---
title: Message pragma (direttiva)
description: Direttiva pragma che produce messaggi della fase di compilazione.
ms.assetid: dc3ece10-9730-4ab1-acc8-f95abc92de7d
keywords:
- Message pragma directive HLSL
topic_type:
- apiref
api_name:
- message pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f342f4a139320e4beb821f32662da72785ab751c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718925"
---
# <a name="message-pragma-directive"></a>Message pragma (direttiva)

Direttiva pragma che produce messaggi della fase di compilazione.



| \#pragma message "*token-String*" |
|-----------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                    | Descrizione                  |
|-----------------------------------------------------------------------------------------|------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*stringa di token*<br/> | Messaggio del compilatore.<br/> |



 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrata l'elaborazione dei messaggi durante la pre-elaborazione.


```
#pragma message "Debugging flag set."
```



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Direttive per il preprocessore (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#pragma (direttiva) (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





