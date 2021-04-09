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
# <a name="iagentspeechinputpropertiesgethotkey"></a><span data-ttu-id="77ba5-103">IAgentSpeechInputProperties:: GetHotKey</span><span class="sxs-lookup"><span data-stu-id="77ba5-103">IAgentSpeechInputProperties::GetHotKey</span></span>

<span data-ttu-id="77ba5-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="77ba5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHotKey(
BSTR * pbszHotCharKey  // address of variable for listening key 
);                        
```

<span data-ttu-id="77ba5-105">Recupera l'assegnazione di tastiera corrente per la chiave di ascolto dell'input vocale.</span><span class="sxs-lookup"><span data-stu-id="77ba5-105">Retrieves the current keyboard assignment for the speech input Listening key.</span></span>

-   <span data-ttu-id="77ba5-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="77ba5-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="77ba5-107"><span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*pbszHotCharKey*</span><span class="sxs-lookup"><span data-stu-id="77ba5-107"><span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*pbszHotCharKey*</span></span>
</dt> <dd>

<span data-ttu-id="77ba5-108">Indirizzo di un BSTR che riceve l'impostazione del tasto di scelta rapida corrente usata per aprire il canale audio per l'input vocale.</span><span class="sxs-lookup"><span data-stu-id="77ba5-108">Address of a BSTR that receives the current hotkey setting used to open the audio channel for speech input.</span></span>

</dd> </dl>

<span data-ttu-id="77ba5-109">Se [**GetEnabled**](iagentspeechinputproperties--getenabled.md) restituisce **false**, l'esecuzione di una query su questa impostazione genera un errore.</span><span class="sxs-lookup"><span data-stu-id="77ba5-109">If [**GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**, querying this setting raises an error.</span></span>

## <a name="see-also"></a><span data-ttu-id="77ba5-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="77ba5-110">See Also</span></span>

[<span data-ttu-id="77ba5-111">**IAgentSpeechInputProperties:: GetEnabled**</span><span class="sxs-lookup"><span data-stu-id="77ba5-111">**IAgentSpeechInputProperties::GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)


 

 




