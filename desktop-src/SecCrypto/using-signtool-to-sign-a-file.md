---
description: Viene illustrato come utilizzare SignTool per firmare un file.
ms.assetid: fa8ee4d3-8927-4f7d-a09e-dbcf75a164d3
title: Uso di SignTool per firmare un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089026cde629278e5c6ac033164c2a9d26528917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130235"
---
# <a name="using-signtool-to-sign-a-file"></a>Uso di SignTool per firmare un file

Il comando seguente firma il file denominato MyControl.exe usando un [*certificato*](../secgloss/c-gly.md) archiviato in un file pfx (Personal Information Exchange):

<pre>SignTool sign /f <b>MyCert</b>.pfx MyControl.exe</pre>

Il comando seguente consente di firmare il file usando un certificato archiviato in un file PFX protetto da password:

<pre>SignTool sign /f <b>MyCert</b>.pfx /p <b>MyPassword</b> MyControl.exe</pre>

> [!Note]  
> Assicurarsi di proteggere correttamente la password.

 

Il comando seguente firma e timbra il timestamp del file:

<pre>SignTool sign /f <b>MyCert</b>.pfx /t http://timestamp.digicert.com MyControl.exe</pre>

> [!Note]  
> Per informazioni sul timestamp di un file dopo che è già stato firmato, vedere [aggiunta di timestamp ai file firmati in precedenza](adding-time-stamps-to-previously-signed-files.md).

 

Il comando seguente consente di firmare il file usando un certificato presente nell'archivio My con un nome soggetto dell'editore dell'azienda:

<pre>SignTool sign /n "<b>My Company Publisher</b>" MyControl.exe</pre>

Il comando seguente firma un controllo ActiveX e fornisce le informazioni visualizzate da Internet Explorer quando viene richiesto all'utente di installare il controllo:

<pre>SignTool sign /f <b>MyCert</b>.pfx /d "<b>My Product Name</b>" /du <b>"https://www.example.com/myproductinfo.html"</b> MyControl.exe</pre>

Il comando seguente consente di firmare il file usando un certificato le cui informazioni sulla [*chiave privata*](../secgloss/p-gly.md) sono protette da un modulo di crittografia hardware. Ad esempio, si supponga che il certificato denominato "My High-Value certificate" disponga di una chiave privata installata in un modulo di crittografia hardware e che il certificato sia installato correttamente.

<pre>SignTool sign /n "<b>My High-Value Certificate</b>" MyControl.exe</pre>

Il comando seguente consente di firmare il file usando un certificato le cui informazioni sulla [*chiave privata*](../secgloss/p-gly.md) sono protette da un modulo di crittografia hardware. Viene specificato un archivio del computer per l' [*autorità di certificazione*](../secgloss/c-gly.md) (CA).

<pre>SignTool sign /n "<b>My High Value Certificate</b>" /sm /s CA MyControl.exe</pre>

Il comando seguente consente di firmare il file usando un certificato archiviato in un file. Le informazioni sulla chiave privata sono protette da un modulo di crittografia hardware e il [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) e il [*contenitore di chiavi*](../secgloss/k-gly.md) vengono specificati in base al nome. Questo comando è utile se il certificato non è installato correttamente.

<pre>SignTool sign /f <b>HighValue</b>.cer /csp "<b>Hardware Cryptography Module</b>" /k <b>HighValueContainer</b> MyControl.exe</pre>

[SignTool](signtool.md) restituisce il testo della riga di comando che indica il risultato dell'operazione di firma. Inoltre, SignTool restituisce un codice di uscita pari a zero per l'esecuzione completata, uno per l'esecuzione non riuscita e due per l'esecuzione completata con avvisi.

Per informazioni sulla verifica della firma di un file, vedere [uso di SignTool per verificare una firma del file](using-signtool-to-verify-a-file-signature.md). Per informazioni sull'aggiunta di un timestamp se il file è già stato firmato, vedere [aggiunta di timestamp ai file firmati in precedenza](adding-time-stamps-to-previously-signed-files.md). Per ulteriori informazioni su [SignTool](signtool.md), vedere [SignTool](signtool.md).

 

 
