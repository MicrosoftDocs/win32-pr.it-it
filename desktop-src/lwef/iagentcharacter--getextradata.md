---
title: GetExtraData IAgentCharacter
description: GetExtraData IAgentCharacter
ms.assetid: 83f69bae-0ae3-45c5-ba0d-71610993da60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea854479ab85630abc3d110c9c193716ddedd004
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116937"
---
# <a name="iagentcharactergetextradata"></a><span data-ttu-id="2457c-103">IAgentCharacter:: GetExtraData</span><span class="sxs-lookup"><span data-stu-id="2457c-103">IAgentCharacter::GetExtraData</span></span>

<span data-ttu-id="2457c-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2457c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetExtraData(
   BSTR * pbszExtraData   // address of buffer for additional character data
); 
```

<span data-ttu-id="2457c-105">Recupera dati aggiuntivi archiviati come parte del carattere.</span><span class="sxs-lookup"><span data-stu-id="2457c-105">Retrieves additional data stored as part of the character.</span></span>

-   <span data-ttu-id="2457c-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="2457c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2457c-107"><span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszExtraData*</span><span class="sxs-lookup"><span data-stu-id="2457c-107"><span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszExtraData*</span></span>
</dt> <dd>

<span data-ttu-id="2457c-108">Indirizzo di un BSTR che riceve il valore dei dati aggiuntivi per il carattere.</span><span class="sxs-lookup"><span data-stu-id="2457c-108">The address of a BSTR that receives the value of the additional data for the character.</span></span> <span data-ttu-id="2457c-109">I dati aggiuntivi di un carattere vengono definiti quando vengono compilati con l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="2457c-109">A character's additional data is defined when it is compiled with the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="2457c-110">Uno sviluppatore di caratteri può fornire questa stringa modificando. File ACD per un carattere.</span><span class="sxs-lookup"><span data-stu-id="2457c-110">A character developer can supply this string by editing the .ACD file for a character.</span></span> <span data-ttu-id="2457c-111">L'impostazione è facoltativa e non può essere specificata per tutti i caratteri, né i dati possono essere definiti o modificati in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2457c-111">The setting is optional and may not be supplied for all characters, nor can the data be defined or changed at run time.</span></span> <span data-ttu-id="2457c-112">Inoltre, il significato dei dati forniti viene definito dallo sviluppatore di caratteri.</span><span class="sxs-lookup"><span data-stu-id="2457c-112">In addition, the meaning of the data supplied is defined by the character developer.</span></span>

</dd> </dl>

 

 




