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
# <a name="iagentspeechinputpropertiesgetlisteningtip"></a><span data-ttu-id="bf75e-103">IAgentSpeechInputProperties::GetListeningTip</span><span class="sxs-lookup"><span data-stu-id="bf75e-103">IAgentSpeechInputProperties::GetListeningTip</span></span>

<span data-ttu-id="bf75e-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bf75e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetListeningTip(
long * pbListeningTip  // address of variable for listening tip flag
);                       
```

<span data-ttu-id="bf75e-105">Recupera un valore che indica se il suggerimento di ascolto è abilitato per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="bf75e-105">Retrieves a value indicating whether the Listening Tip is enabled for display.</span></span>

-   <span data-ttu-id="bf75e-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="bf75e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="bf75e-107"><span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*</span><span class="sxs-lookup"><span data-stu-id="bf75e-107"><span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*</span></span>
</dt> <dd>

<span data-ttu-id="bf75e-108">Indirizzo di una variabile che riceve **true** se il suggerimento di ascolto è abilitato per la visualizzazione oppure **false** se il suggerimento di ascolto è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bf75e-108">Address of a variable that receives **True** if the Listening Tip is enabled for display, or **False** if the Listening Tip is disabled.</span></span>

</dd> </dl>

<span data-ttu-id="bf75e-109">Se [**GetEnabled**](iagentspeechinputproperties--getenabled.md) restituisce **false**, l'esecuzione di una query su qualsiasi altra proprietà di input vocale restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="bf75e-109">If [**GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**, querying any other speech input properties returns an error.</span></span>

## <a name="see-also"></a><span data-ttu-id="bf75e-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="bf75e-110">See Also</span></span>

[<span data-ttu-id="bf75e-111">**IAgentSpeechInputProperties:: GetEnabled**</span><span class="sxs-lookup"><span data-stu-id="bf75e-111">**IAgentSpeechInputProperties::GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)


 

 




