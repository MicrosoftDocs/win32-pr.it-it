---
description: Viene illustrato come usare SignTool per firmare un file.
ms.assetid: fa8ee4d3-8927-4f7d-a09e-dbcf75a164d3
title: Uso di SignTool per firmare un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a71d8e85e8e22f65ccbe8b5f15453b0a0cac34fc27697bad648b1c815f255b10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971471"
---
# <a name="using-signtool-to-sign-a-file"></a>Uso di SignTool per firmare un file

Il comando seguente firma il file denominato MyControl.exe un [*certificato*](../secgloss/c-gly.md) archiviato in un file PFX (Personal Information Exchange):

<pre>SignTool sign /f <b>MyCert</b>.pfx MyControl.exe</pre>

Il comando seguente firma il file usando un certificato archiviato in un file PFX protetto da password:

<pre>SignTool sign /f <b>MyCert</b>.pfx /p <b>MyPassword</b> MyControl.exe</pre>

> [!Note]  
> Assicurarsi di proteggere correttamente la password.

 

Il comando seguente firma e contrassegna l'ora del file:

<pre>SignTool sign /f <b>MyCert</b>.pfx /t http://timestamp.digicert.com MyControl.exe</pre>

> [!Note]  
> Per informazioni sul timestamp di un file dopo che è già stato firmato, vedere Aggiunta di timestamp [a file firmati in precedenza](adding-time-stamps-to-previously-signed-files.md).

 

Il comando seguente firma il file usando un certificato che si trova nell'archivio my con il nome soggetto My Company Publisher:

<pre>SignTool sign /n "<b>My Company Publisher</b>" MyControl.exe</pre>

Il comando seguente firma un ActiveX e fornisce le informazioni visualizzate dal Internet Explorer quando all'utente viene richiesto di installare il controllo:

<pre>SignTool sign /f <b>MyCert</b>.pfx /d "<b>My Product Name</b>" /du <b>"https://www.example.com/myproductinfo.html"</b> MyControl.exe</pre>

Il comando seguente firma il file usando un certificato le cui informazioni sulla [*chiave*](../secgloss/p-gly.md) privata sono protette da un modulo di crittografia hardware. A scopo di esempio, si supponga che nel certificato denominato "Certificato High-Value" sia installata una chiave privata in un modulo di crittografia hardware e che il certificato sia installato correttamente.

<pre>SignTool sign /n "<b>My High-Value Certificate</b>" MyControl.exe</pre>

Il comando seguente firma il file usando un certificato le cui informazioni sulla [*chiave*](../secgloss/p-gly.md) privata sono protette da un modulo di crittografia hardware. Per l'archivio autorità [*di certificazione*](../secgloss/c-gly.md) (CA) è specificato un archivio computer.

<pre>SignTool sign /n "<b>My High Value Certificate</b>" /sm /s CA MyControl.exe</pre>

Il comando seguente firma il file usando un certificato archiviato in un file. Le informazioni sulla chiave privata sono protette da un modulo di crittografia hardware e il [*provider*](../secgloss/c-gly.md) del servizio di crittografia (CSP) e il contenitore di chiavi [*vengono*](../secgloss/k-gly.md) specificati in base al nome. Questo comando è utile se il certificato non è installato correttamente.

<pre>SignTool sign /f <b>HighValue</b>.cer /csp "<b>Hardware Cryptography Module</b>" /k <b>HighValueContainer</b> MyControl.exe</pre>

[SignTool restituisce](signtool.md) il testo della riga di comando che indica il risultato dell'operazione di firma. SignTool restituisce inoltre un codice di uscita pari a zero per l'esecuzione corretta, uno per l'esecuzione non riuscita e due per l'esecuzione completata con avvisi.

Per informazioni sulla verifica della firma di un file, vedere [Uso di SignTool per verificare una firma file](using-signtool-to-verify-a-file-signature.md). Per informazioni sull'aggiunta di un timestamp se il file è già stato firmato, vedere Aggiunta di timestamp [a file firmati in precedenza](adding-time-stamps-to-previously-signed-files.md). Per altre informazioni su [SignTool,](signtool.md)vedere [SignTool](signtool.md).

 

 
