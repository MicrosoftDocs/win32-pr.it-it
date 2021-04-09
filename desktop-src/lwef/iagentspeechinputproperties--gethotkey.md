---
title: IAgentSpeechInputProperties GetHotKey
description: IAgentSpeechInputProperties GetHotKey
ms.assetid: b93e5b46-b8f8-4ca4-8417-7626b97d8928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e672b26f97cfbe92bc71d0ceab165e100c3ecf92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104043979"
---
# <a name="iagentspeechinputpropertiesgethotkey"></a>IAgentSpeechInputProperties:: GetHotKey

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetHotKey(
BSTR * pbszHotCharKey  // address of variable for listening key 
);                        
```

Recupera l'assegnazione di tastiera corrente per la chiave di ascolto dell'input vocale.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*pbszHotCharKey*
</dt> <dd>

Indirizzo di un BSTR che riceve l'impostazione del tasto di scelta rapida corrente usata per aprire il canale audio per l'input vocale.

</dd> </dl>

Se [**GetEnabled**](iagentspeechinputproperties--getenabled.md) restituisce **false**, l'esecuzione di una query su questa impostazione genera un errore.

## <a name="see-also"></a>Vedere anche

[**IAgentSpeechInputProperties:: GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




