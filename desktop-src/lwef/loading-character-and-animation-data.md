---
title: Caricamento dei dati di tipo carattere e animazione
description: Caricamento dei dati di tipo carattere e animazione
ms.assetid: cd674513-fd68-49bb-a43f-12b07adddf3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed77524c4e3cbbcae725b87c3671914f2261fa1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298641"
---
# <a name="loading-character-and-animation-data"></a><span data-ttu-id="c074e-103">Caricamento dei dati di tipo carattere e animazione</span><span class="sxs-lookup"><span data-stu-id="c074e-103">Loading Character and Animation Data</span></span>

<span data-ttu-id="c074e-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c074e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="c074e-105">Dopo avere un puntatore all'interfaccia [**IAgentEx**](iagentex.md) , è possibile usare il metodo [**Load**](load-method.md) per caricare un carattere e recuperare la relativa interfaccia [**IAgentCharacterEx**](iagentcharacterex.md) .</span><span class="sxs-lookup"><span data-stu-id="c074e-105">After you have a pointer to the [**IAgentEx**](iagentex.md) interface, you can use the [**Load**](load-method.md) method to load a character and retrieve its [**IAgentCharacterEx**](iagentcharacterex.md) interface.</span></span> <span data-ttu-id="c074e-106">Sono disponibili tre diverse possibilità per il percorso di caricamento di un carattere.</span><span class="sxs-lookup"><span data-stu-id="c074e-106">There are three different possibilities for the Load path of a character.</span></span> <span data-ttu-id="c074e-107">Il primo è compatibile con Microsoft Agent 1,5, dove il percorso specificato è il percorso completo e il nome file di un file di caratteri.</span><span class="sxs-lookup"><span data-stu-id="c074e-107">The first is compatible with Microsoft Agent 1.5 where the specified path is the full path and filename of a character file.</span></span> <span data-ttu-id="c074e-108">La seconda possibilità è specificare solo il nome del file. in questo caso, Agent Cerca nella directory chars.</span><span class="sxs-lookup"><span data-stu-id="c074e-108">The second possibility is to specify the filename only, in which case, Agent looks in its Chars directory.</span></span> <span data-ttu-id="c074e-109">L'ultima possibilità è fornire un parametro VARIANT vuoto che causa il caricamento del carattere predefinito.</span><span class="sxs-lookup"><span data-stu-id="c074e-109">The last possibility is to supply an empty Variant parameter that causes the default character to be loaded.</span></span>


```
   // Create a variant to store the filename of the character to load

   const LPWSTR kpwszCharacter = L"merlin.acs";

   VariantInit(&vPath);

   vPath.vt = VT_BSTR;
   vPath.bstrVal = SysAllocString(kpwszCharacter);

   // Load the character

   hRes = pAgentEx->Load(vPath, &lCharID, &lRequestID);

   // Get its IAgentCharacterEx interface

   hRes = pAgentEx->GetCharacterEx(lCharID, &pCharacterEx);
```



<span data-ttu-id="c074e-110">È possibile utilizzare questa interfaccia per accedere ai metodi del carattere:</span><span class="sxs-lookup"><span data-stu-id="c074e-110">You can use this interface to access the character's methods:</span></span>


```
   // Show the character.  The first parameter tells Microsoft
   // Agent to show the character by playing an animation.

   hRes = pCharacterEx->Show(FALSE, &lRequestID);

   // Make the character speak

   bszSpeak = SysAllocString(L"Hello World!");

   hRes = pCharacterEx->Speak(bszSpeak, NULL, &lRequestID);

   SysFreeString(bszSpeak);
```



<span data-ttu-id="c074e-111">Quando i servizi di Microsoft Agent non sono più necessari, ad esempio quando l'applicazione client viene arrestata, rilascia le interfacce.</span><span class="sxs-lookup"><span data-stu-id="c074e-111">When you no longer need Microsoft Agent services, such as when your client application shuts down, release its interfaces.</span></span> <span data-ttu-id="c074e-112">Si noti che il rilascio dell'interfaccia dei caratteri non Scarica il carattere.</span><span class="sxs-lookup"><span data-stu-id="c074e-112">Note that releasing the character interface does not unload the character.</span></span> <span data-ttu-id="c074e-113">Per eseguire questa operazione, chiamare il metodo [**unload**](unload-method.md) prima di rilasciare l'interfaccia [**IAgentEx**](iagentex.md) :</span><span class="sxs-lookup"><span data-stu-id="c074e-113">Call the [**Unload**](unload-method.md) method to do this before releasing the [**IAgentEx**](iagentex.md) interface:</span></span>


```
// Clean up

if (pCharacterEx) {

   // Release the character interface

   pCharacterEx->Release();

   // Unload the character.  NOTE:  releasing the character
   // interface does NOT make the character go away.  You must
   // call Unload.

   pAgentEx->Unload(lCharID);
}
   
// Release the Agent

pAgentEx->Release();

VariantClear(&vPath);
```



 

 




