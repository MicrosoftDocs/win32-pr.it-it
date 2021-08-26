---
title: Caricamento di dati di animazione e caratteri
description: Caricamento di dati di animazione e caratteri
ms.assetid: cd674513-fd68-49bb-a43f-12b07adddf3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0e387a6122ab08513763878678d99941ef65d8ed11822eed8639fccd6e3815d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961431"
---
# <a name="loading-character-and-animation-data"></a>Caricamento di dati di animazione e caratteri

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Dopo aver creato un puntatore [**all'interfaccia IAgentEx,**](iagentex.md) è possibile usare il metodo [**Load**](load-method.md) per caricare un carattere e recuperarne [**l'interfaccia IAgentCharacterEx.**](iagentcharacterex.md) Esistono tre diverse possibilità per il percorso di caricamento di un carattere. Il primo è compatibile con Microsoft Agent 1.5, dove il percorso specificato è il percorso completo e il nome file di un file di caratteri. La seconda possibilità è specificare solo il nome del file. In tal caso, Agent cerca nella directory Chars. L'ultima possibilità è fornire un parametro Variant vuoto che causa il caricamento del carattere predefinito.


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



È possibile usare questa interfaccia per accedere ai metodi del carattere:


```
   // Show the character.  The first parameter tells Microsoft
   // Agent to show the character by playing an animation.

   hRes = pCharacterEx->Show(FALSE, &lRequestID);

   // Make the character speak

   bszSpeak = SysAllocString(L"Hello World!");

   hRes = pCharacterEx->Speak(bszSpeak, NULL, &lRequestID);

   SysFreeString(bszSpeak);
```



Quando i servizi di Microsoft Agent non sono più necessari, ad esempio quando l'applicazione client viene arrestata, rilasciare le relative interfacce. Si noti che il rilascio dell'interfaccia dei caratteri non scarica il carattere. Chiamare il [**metodo Unload**](unload-method.md) per eseguire questa operazione prima di rilasciare [**l'interfaccia IAgentEx:**](iagentex.md)


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



 

 




