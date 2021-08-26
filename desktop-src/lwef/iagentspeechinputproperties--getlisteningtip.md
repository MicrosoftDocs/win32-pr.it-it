---
title: IAgentSpeechInputProperties GetListeningTip
description: IAgentSpeechInputProperties GetListeningTip
ms.assetid: b0488a54-03f8-43ce-935c-dd49c6ed5dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0199e75ad56cee2c299ce53be3aa94376104af5ead40004e8dbbd8fd4dcfec9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014181"
---
# <a name="iagentspeechinputpropertiesgetlisteningtip"></a>IAgentSpeechInputProperties::GetListeningTip

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetListeningTip(
long * pbListeningTip  // address of variable for listening tip flag
);                       
```

Recupera un valore che indica se il suggerimento in ascolto è abilitato per la visualizzazione.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*
</dt> <dd>

Indirizzo di una variabile che riceve **True se** il suggerimento in ascolto è abilitato per la visualizzazione oppure **False se** il suggerimento in ascolto è disabilitato.

</dd> </dl>

Se [**GetEnabled restituisce**](iagentspeechinputproperties--getenabled.md) **False,** l'esecuzione di query su qualsiasi altra proprietà di input vocale restituisce un errore.

## <a name="see-also"></a>Vedere anche

[**IAgentSpeechInputProperties::GetEnabled**](iagentspeechinputproperties--getenabled.md)


 

 




