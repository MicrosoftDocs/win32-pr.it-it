---
description: Le funzioni di esportazione del parser forniscono tutte le funzionalità dei parser nella DLL del parser. Ogni DLL del parser deve implementare ParserAutoInstallInfo e DllMain. Le funzioni di esportazione rimanenti devono essere implementate per ogni parser incluso nella DLL del parser.
ms.assetid: be73623c-7ae7-4ca9-be6c-52f513cd38a4
title: Implementazione delle funzioni di esportazione del parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e32b3b1aa807a604f058ed8965ef11728f6c12fecb34e27a337682361f8dd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778841"
---
# <a name="implementing-parser-export-functions"></a>Implementazione delle funzioni di esportazione del parser

Le funzioni di esportazione del parser forniscono tutte le funzionalità dei parser nella DLL del parser. Ogni DLL del parser deve [**implementare ParserAutoInstallInfo**](parserautoinstallinfo.md) e [**DllMain.**](dllmain-parser.md) Le funzioni di esportazione rimanenti devono essere implementate per ogni parser incluso nella DLL del parser.

Negli argomenti seguenti viene illustrato come implementare le funzioni di esportazione.



| Termine                                                                                                                                                                                                                                                   | Descrizione                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Implementing_ParserAutoInstallInfo"></span><span id="implementing_parserautoinstallinfo"></span><span id="IMPLEMENTING_PARSERAUTOINSTALLINFO"></span>[Implementazione di ParserAutoInstallInfo](implementing-parserautoinstallinfo.md)<br/> | Fornisce una descrizione e un esempio di codice per l'implementazione della funzione [**ParserAutoInstallInfo,**](parserautoinstallinfo.md) che identifica i parser che si trovano in una DLL del parser.<br/>                                                                                            |
| <span id="Implementing_DllMain_Parser"></span><span id="implementing_dllmain_parser"></span><span id="IMPLEMENTING_DLLMAIN_PARSER"></span>[Implementazione del parser DllMain](implementing-dllmain-parser.md)<br/>                                    | Fornisce una descrizione e un esempio di codice per l'implementazione della funzione [**parser DllMain,**](dllmain-parser.md) che identifica l'esistenza di un parser e quindi rilascia le risorse utilizzate Network Monitor per il parser.<br/>                                              |
| <span id="Implementing_Register"></span><span id="implementing_register"></span><span id="IMPLEMENTING_REGISTER"></span>[Implementazione del registro](implementing-register.md)<br/>                                                                  | Fornisce una descrizione e un esempio di codice per l'implementazione [**della funzione Register,**](register-parser.md) che registra tutte le proprietà di un protocollo.<br/>                                                                                                                     |
| <span id="Implementing_RecognizeFrame"></span><span id="implementing_recognizeframe"></span><span id="IMPLEMENTING_RECOGNIZEFRAME"></span>[Implementazione di RecognizeFrame](implementing-recognizeframe.md)<br/>                                    | Fornisce una descrizione e un esempio di codice per l'implementazione [**della funzione RecognizeFrame,**](recognizeframe.md) che identifica un'istanza di un protocollo in un frame.<br/>                                                                                                         |
| <span id="Implementing_AttachProperties"></span><span id="implementing_attachproperties"></span><span id="IMPLEMENTING_ATTACHPROPERTIES"></span>[Implementazione di AttachProperties](implementing-attachproperties.md)<br/>                          | Fornisce una descrizione e un esempio di codice per l'implementazione della funzione [**AttachProperties,**](attachproperties.md) che separa i dati riconosciuti dal parser e quindi allega le descrizioni delle proprietà a ogni proprietà del protocollo presente nei dati riconosciuti.<br/> |
| <span id="Implementing_FormatProperties"></span><span id="implementing_formatproperties"></span><span id="IMPLEMENTING_FORMATPROPERTIES"></span>[Implementazione di FormatProperties](implementing-formatproperties.md)<br/>                          | Fornisce una descrizione e un esempio di codice per l'implementazione della funzione [**FormatProperties,**](formatproperties.md) che formatta i dati visualizzati nel riquadro dei dettagli dell'interfaccia Network Monitor interfaccia utente.<br/>                                                                    |
| <span id="Implementing_Deregister"></span><span id="implementing_deregister"></span><span id="IMPLEMENTING_DEREGISTER"></span>[Implementazione dell'annullamento della registrazione](implementing-deregister.md)<br/>                                                        | Fornisce una descrizione e un esempio di codice per l'implementazione [**della funzione Deregister,**](deregister.md) che rilascia le risorse usate per registrare le proprietà del protocollo.<br/>                                                                                                     |



 

 

 




