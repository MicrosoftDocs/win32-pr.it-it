---
description: Per poter essere utilizzata dalla piattaforma Tablet PC, è necessario registrare la DLL del riconoscitore. Il riconoscitore deve apportare le modifiche seguenti al Registro di sistema al momento dell'installazione.
ms.assetid: 1f1d826b-3968-424b-8da8-b69590058ff1
title: Registrazione della DLL del riconoscitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae80eb49f1795e315cf77bf5aede83cc1677e168f4aea4d6715a216e74434caf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350071"
---
# <a name="registering-your-recognizer-dll"></a>Registrazione della DLL del riconoscitore

Per poter essere utilizzata dalla piattaforma Tablet PC, è necessario registrare la DLL del riconoscitore. Il riconoscitore deve apportare le modifiche seguenti al Registro di sistema al momento dell'installazione.

Aggiungere una nuova chiave per ogni CLSID del sistema di riconoscimento nella chiave HKEY \_ LOCAL \_ MACHINE/SOFTWARE/Microsoft/TPG/Recognizers/ del Registro di sistema. Aggiungere un CLSID per ogni linguaggio. Nella tabella seguente vengono descritti i valori che devono essere aggiunti sotto ognuna delle chiavi contenenti i CLSID.

> [!Note]  
> Per i nomi di questi valori viene fatto distinzione tra maiuscole e minuscole.

 



| Nome del valore                             | Tipo di valore             | Descrizione del valore                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Flag di funzionalità di riconoscimento<br/> | REG \_ DWORD<br/>  | DWORD usato per determinare le funzionalità del riconoscitore.<br/>                                                                                                                                                                                                                                                                                                                             |
| DLL di riconoscimento<br/>              | REG \_ SZ<br/>     | Percorso completo della DLL del riconoscitore installato.<br/>                                                                                                                                                                                                                                                                                                                                              |
| Lingue riconosciute<br/>        | REG \_ BINARY<br/> | Matrice binaria che descrive la lingua o le lingue con cui è progettato un sistema di riconoscimento.<br/> In rectypes.h la definizione MAX LANGUAGES specifica il numero massimo di lingue supportate da un sistema di riconoscimento e ogni lingua accetta una parola da archiviare nell'elemento \_ "Recognized Languages". Le dimensioni della voce del Registro di sistema REG \_ BINARY devono essere max LANGUAGES \_ \* sizeof(WORD).<br/> |



 

 

 




