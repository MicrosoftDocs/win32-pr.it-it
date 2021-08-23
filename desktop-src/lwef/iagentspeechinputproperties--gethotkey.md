---
title: IAgentSpeechInputProperties GetHotKey
description: IAgentSpeechInputProperties GetHotKey
ms.assetid: b93e5b46-b8f8-4ca4-8417-7626b97d8928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a66e4f3fe070a944ecd9800a6712e8ae4db8d333913e5cfe85c027565cf1cf77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609381"
---
# <a name="iagentspeechinputpropertiesgethotkey"></a>IAgentSpeechInputProperties::GetHotKey

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetHotKey(
BSTR * pbszHotCharKey  // address of variable for listening key 
);                        
```

Recupera l'assegnazione di tastiera corrente per il tasto di ascolto dell'input vocale.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*pbszHotCharKey*
</dt> <dd>

Indirizzo di un BSTR che riceve l'impostazione del tasto di scelta rapida corrente usata per aprire il canale audio per l'input vocale.

</dd> </dl>

Se [**GetEnabled restituisce**](iagentspeechinputproperties--getenabled.md) **False**, l'esecuzione di query su questa impostazione genera un errore.

## <a name="see-also"></a>Vedere anche

[**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




