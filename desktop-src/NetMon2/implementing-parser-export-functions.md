---
description: Le funzioni di esportazione del parser forniscono tutte le funzionalità dei parser nella DLL del parser. Ogni DLL del parser deve implementare ParserAutoInstallInfo e DllMain. Le funzioni di esportazione rimanenti devono essere implementate per ogni parser incluso nella DLL del parser.
ms.assetid: be73623c-7ae7-4ca9-be6c-52f513cd38a4
title: Implementazione di funzioni di esportazione del parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b8eafb7e12c36a9413a320652e3d372ffbf51e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525110"
---
# <a name="implementing-parser-export-functions"></a>Implementazione di funzioni di esportazione del parser

Le funzioni di esportazione del parser forniscono tutte le funzionalità dei parser nella DLL del parser. Ogni DLL del parser deve implementare [**ParserAutoInstallInfo**](parserautoinstallinfo.md) e [**DllMain**](dllmain-parser.md). Le funzioni di esportazione rimanenti devono essere implementate per ogni parser incluso nella DLL del parser.

Negli argomenti seguenti viene illustrato come implementare le funzioni di esportazione.



| Termine                                                                                                                                                                                                                                                   | Descrizione                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Implementing_ParserAutoInstallInfo"></span><span id="implementing_parserautoinstallinfo"></span><span id="IMPLEMENTING_PARSERAUTOINSTALLINFO"></span>[Implementazione di ParserAutoInstallInfo](implementing-parserautoinstallinfo.md)<br/> | Fornisce una descrizione e un esempio di codice per l'implementazione della funzione [**ParserAutoInstallInfo**](parserautoinstallinfo.md) , che identifica i parser presenti in una dll del parser.<br/>                                                                                            |
| <span id="Implementing_DllMain_Parser"></span><span id="implementing_dllmain_parser"></span><span id="IMPLEMENTING_DLLMAIN_PARSER"></span>[Implementazione del parser DllMain](implementing-dllmain-parser.md)<br/>                                    | Fornisce una descrizione e un esempio di codice per l'implementazione della funzione del [**parser DllMain**](dllmain-parser.md) , che identifica l'esistenza di un parser, quindi rilascia le risorse utilizzate Network Monitor per il parser.<br/>                                              |
| <span id="Implementing_Register"></span><span id="implementing_register"></span><span id="IMPLEMENTING_REGISTER"></span>[Implementazione del registro](implementing-register.md)<br/>                                                                  | Fornisce una descrizione e un esempio di codice per l'implementazione della funzione [**Register**](register-parser.md) , che registra tutte le proprietà di un protocollo.<br/>                                                                                                                     |
| <span id="Implementing_RecognizeFrame"></span><span id="implementing_recognizeframe"></span><span id="IMPLEMENTING_RECOGNIZEFRAME"></span>[Implementazione di RecognizeFrame](implementing-recognizeframe.md)<br/>                                    | Fornisce una descrizione e un esempio di codice per l'implementazione della funzione [**RecognizeFrame**](recognizeframe.md) , che identifica un'istanza di un protocollo in un frame.<br/>                                                                                                         |
| <span id="Implementing_AttachProperties"></span><span id="implementing_attachproperties"></span><span id="IMPLEMENTING_ATTACHPROPERTIES"></span>[Implementazione di AttachProperties](implementing-attachproperties.md)<br/>                          | Fornisce una descrizione e un esempio di codice per l'implementazione della funzione [**AttachProperties**](attachproperties.md) , che separa i dati riconosciuti dal parser, quindi connette le descrizioni delle proprietà a ogni proprietà del protocollo presente nei dati riconosciuti.<br/> |
| <span id="Implementing_FormatProperties"></span><span id="implementing_formatproperties"></span><span id="IMPLEMENTING_FORMATPROPERTIES"></span>[Implementazione di FormatProperties](implementing-formatproperties.md)<br/>                          | Fornisce una descrizione e un esempio di codice per l'implementazione della funzione [**FormatProperties**](formatproperties.md) , che formatta i dati visualizzati nel riquadro dei dettagli dell'interfaccia utente di Network Monitor.<br/>                                                                    |
| <span id="Implementing_Deregister"></span><span id="implementing_deregister"></span><span id="IMPLEMENTING_DEREGISTER"></span>[Implementazione della deregistrazione](implementing-deregister.md)<br/>                                                        | Fornisce una descrizione e un esempio di codice per l'implementazione della funzione [**deregister**](deregister.md) , che rilascia le risorse usate per registrare le proprietà del protocollo.<br/>                                                                                                     |



 

 

 




