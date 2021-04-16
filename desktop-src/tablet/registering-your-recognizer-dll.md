---
description: Per usarlo, è necessario registrare la DLL del riconoscitore per la piattaforma Tablet PC. Il riconoscimento deve apportare le seguenti modifiche al registro di sistema al momento dell'installazione.
ms.assetid: 1f1d826b-3968-424b-8da8-b69590058ff1
title: Registrazione della DLL del riconoscitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51114f11868e6d45dc4d319dab60e5b4f094ddbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530276"
---
# <a name="registering-your-recognizer-dll"></a>Registrazione della DLL del riconoscitore

Per usarlo, è necessario registrare la DLL del riconoscitore per la piattaforma Tablet PC. Il riconoscimento deve apportare le seguenti modifiche al registro di sistema al momento dell'installazione.

Aggiungere una nuova chiave per ognuno dei CLSID del riconoscimento sotto la \_ chiave del registro di sistema HKEY LOCAL \_ computer/software/Microsoft/TPG/Recognizers/Registry. Aggiungere un solo CLSID per lingua. Nella tabella seguente vengono descritti i valori che devono essere aggiunti sotto ogni chiave contenente i CLSID.

> [!Note]  
> I nomi di questi valori fanno distinzione tra maiuscole e minuscole.

 



| Nome del valore                             | Tipo di valore             | Descrizione del valore                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Flag funzionalità di riconoscimento<br/> | REG \_ DWORD<br/>  | DWORD utilizzato per determinare le funzionalità del riconoscimento.<br/>                                                                                                                                                                                                                                                                                                                             |
| DLL di riconoscimento<br/>              | REG \_ SZ<br/>     | Percorso completo della DLL del riconoscitore installato.<br/>                                                                                                                                                                                                                                                                                                                                              |
| Lingue riconosciute<br/>        | REG \_ binario<br/> | Matrice binaria che descrive la lingua o le lingue con cui un riconoscimento è progettato per funzionare.<br/> In rictypes. h, il \_ numero massimo di lingue definito specifica il numero massimo di lingue supportate da un riconoscimento e ogni lingua accetta una parola da archiviare nell'elemento "lingue riconosciute". La dimensione della voce del \_ Registro di sistema reg Binary deve essere il numero massimo di \_ lingue \* sizeof (Word).<br/> |



 

 

 




