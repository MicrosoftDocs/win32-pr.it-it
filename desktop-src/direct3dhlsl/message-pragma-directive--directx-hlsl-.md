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
ms.openlocfilehash: fce4b8f2fec887397794914604a0755049615699af77c5572536b5758bda2d88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986361"
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

 

 





