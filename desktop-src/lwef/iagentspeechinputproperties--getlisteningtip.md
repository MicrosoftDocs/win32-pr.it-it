---
title: IAgentSpeechInputProperties GetListeningTip
description: IAgentSpeechInputProperties GetListeningTip
ms.assetid: b0488a54-03f8-43ce-935c-dd49c6ed5dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91218fb7935edb68458d540a8f35fe5402b317ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297599"
---
# <a name="iagentspeechinputpropertiesgetlisteningtip"></a>IAgentSpeechInputProperties::GetListeningTip

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetListeningTip(
long * pbListeningTip  // address of variable for listening tip flag
);                       
```

Recupera un valore che indica se il suggerimento di ascolto è abilitato per la visualizzazione.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*
</dt> <dd>

Indirizzo di una variabile che riceve **true** se il suggerimento di ascolto è abilitato per la visualizzazione oppure **false** se il suggerimento di ascolto è disabilitato.

</dd> </dl>

Se [**GetEnabled**](iagentspeechinputproperties--getenabled.md) restituisce **false**, l'esecuzione di una query su qualsiasi altra proprietà di input vocale restituisce un errore.

## <a name="see-also"></a>Vedere anche

[**IAgentSpeechInputProperties:: GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




