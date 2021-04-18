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
# <a name="loading-character-and-animation-data"></a>Caricamento dei dati di tipo carattere e animazione

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Dopo avere un puntatore all'interfaccia [**IAgentEx**](iagentex.md) , è possibile usare il metodo [**Load**](load-method.md) per caricare un carattere e recuperare la relativa interfaccia [**IAgentCharacterEx**](iagentcharacterex.md) . Sono disponibili tre diverse possibilità per il percorso di caricamento di un carattere. Il primo è compatibile con Microsoft Agent 1,5, dove il percorso specificato è il percorso completo e il nome file di un file di caratteri. La seconda possibilità è specificare solo il nome del file. in questo caso, Agent Cerca nella directory chars. L'ultima possibilità è fornire un parametro VARIANT vuoto che causa il caricamento del carattere predefinito.


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



È possibile utilizzare questa interfaccia per accedere ai metodi del carattere:


```
   // Show the character.  The first parameter tells Microsoft
   // Agent to show the character by playing an animation.

   hRes = pCharacterEx->Show(FALSE, &lRequestID);

   // Make the character speak

   bszSpeak = SysAllocString(L"Hello World!");

   hRes = pCharacterEx->Speak(bszSpeak, NULL, &lRequestID);

   SysFreeString(bszSpeak);
```



Quando i servizi di Microsoft Agent non sono più necessari, ad esempio quando l'applicazione client viene arrestata, rilascia le interfacce. Si noti che il rilascio dell'interfaccia dei caratteri non Scarica il carattere. Per eseguire questa operazione, chiamare il metodo [**unload**](unload-method.md) prima di rilasciare l'interfaccia [**IAgentEx**](iagentex.md) :


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



 

 




