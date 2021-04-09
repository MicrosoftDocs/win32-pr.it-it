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
# <a name="using-signtool-to-sign-a-file"></a><span data-ttu-id="ab5a6-103">Uso di SignTool per firmare un file</span><span class="sxs-lookup"><span data-stu-id="ab5a6-103">Using SignTool to Sign a File</span></span>

<span data-ttu-id="ab5a6-104">Il comando seguente firma il file denominato MyControl.exe usando un [*certificato*](../secgloss/c-gly.md) archiviato in un file pfx (Personal Information Exchange):</span><span class="sxs-lookup"><span data-stu-id="ab5a6-104">The following command signs the file named MyControl.exe using a [*certificate*](../secgloss/c-gly.md) stored in a Personal Information Exchange (PFX) file:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx MyControl.exe</pre>

<span data-ttu-id="ab5a6-105">Il comando seguente consente di firmare il file usando un certificato archiviato in un file PFX protetto da password:</span><span class="sxs-lookup"><span data-stu-id="ab5a6-105">The following command signs the file using a certificate stored in a password-protected PFX file:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx /p <b>MyPassword</b> MyControl.exe</pre>

> [!Note]  
> <span data-ttu-id="ab5a6-106">Assicurarsi di proteggere correttamente la password.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-106">Ensure that you properly protect the password.</span></span>

 

<span data-ttu-id="ab5a6-107">Il comando seguente firma e timbra il timestamp del file:</span><span class="sxs-lookup"><span data-stu-id="ab5a6-107">The following command signs and time stamps the file:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx /t http://timestamp.digicert.com MyControl.exe</pre>

> [!Note]  
> <span data-ttu-id="ab5a6-108">Per informazioni sul timestamp di un file dopo che è già stato firmato, vedere [aggiunta di timestamp ai file firmati in precedenza](adding-time-stamps-to-previously-signed-files.md).</span><span class="sxs-lookup"><span data-stu-id="ab5a6-108">For information about time stamping a file after it has already been signed, see [Adding Time Stamps to Previously Signed Files](adding-time-stamps-to-previously-signed-files.md).</span></span>

 

<span data-ttu-id="ab5a6-109">Il comando seguente consente di firmare il file usando un certificato presente nell'archivio My con un nome soggetto dell'editore dell'azienda:</span><span class="sxs-lookup"><span data-stu-id="ab5a6-109">The following command signs the file using a certificate located in the My store with a subject name of My Company Publisher:</span></span>

<pre>SignTool sign /n "<b>My Company Publisher</b>" MyControl.exe</pre>

<span data-ttu-id="ab5a6-110">Il comando seguente firma un controllo ActiveX e fornisce le informazioni visualizzate da Internet Explorer quando viene richiesto all'utente di installare il controllo:</span><span class="sxs-lookup"><span data-stu-id="ab5a6-110">The following command signs an ActiveX control and provides information that is displayed by Internet Explorer when the user is prompted to install the control:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx /d "<b>My Product Name</b>" /du <b>"https://www.example.com/myproductinfo.html"</b> MyControl.exe</pre>

<span data-ttu-id="ab5a6-111">Il comando seguente consente di firmare il file usando un certificato le cui informazioni sulla [*chiave privata*](../secgloss/p-gly.md) sono protette da un modulo di crittografia hardware.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-111">The following command signs the file using a certificate whose [*private key*](../secgloss/p-gly.md) information is protected by a hardware cryptography module.</span></span> <span data-ttu-id="ab5a6-112">Ad esempio, si supponga che il certificato denominato "My High-Value certificate" disponga di una chiave privata installata in un modulo di crittografia hardware e che il certificato sia installato correttamente.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-112">For example purposes, assume that the certificate called "My High-Value Certificate," has a private key installed in a hardware cryptography module, and the certificate is properly installed.</span></span>

<pre>SignTool sign /n "<b>My High-Value Certificate</b>" MyControl.exe</pre>

<span data-ttu-id="ab5a6-113">Il comando seguente consente di firmare il file usando un certificato le cui informazioni sulla [*chiave privata*](../secgloss/p-gly.md) sono protette da un modulo di crittografia hardware.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-113">The following command signs the file using a certificate whose [*private key*](../secgloss/p-gly.md) information is protected by a hardware cryptography module.</span></span> <span data-ttu-id="ab5a6-114">Viene specificato un archivio del computer per l' [*autorità di certificazione*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="ab5a6-114">A computer store is specified for the [*certification authority*](../secgloss/c-gly.md) (CA) store.</span></span>

<pre>SignTool sign /n "<b>My High Value Certificate</b>" /sm /s CA MyControl.exe</pre>

<span data-ttu-id="ab5a6-115">Il comando seguente consente di firmare il file usando un certificato archiviato in un file.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-115">The following command signs the file using a certificate stored in a file.</span></span> <span data-ttu-id="ab5a6-116">Le informazioni sulla chiave privata sono protette da un modulo di crittografia hardware e il [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) e il [*contenitore di chiavi*](../secgloss/k-gly.md) vengono specificati in base al nome.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-116">The private key information is protected by a hardware cryptography module, and the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP)and [*key container*](../secgloss/k-gly.md) are specified by name.</span></span> <span data-ttu-id="ab5a6-117">Questo comando è utile se il certificato non è installato correttamente.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-117">This command is useful if the certificate is not properly installed.</span></span>

<pre>SignTool sign /f <b>HighValue</b>.cer /csp "<b>Hardware Cryptography Module</b>" /k <b>HighValueContainer</b> MyControl.exe</pre>

<span data-ttu-id="ab5a6-118">[SignTool](signtool.md) restituisce il testo della riga di comando che indica il risultato dell'operazione di firma.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-118">[SignTool](signtool.md) returns command line text that states the result of the signing operation.</span></span> <span data-ttu-id="ab5a6-119">Inoltre, SignTool restituisce un codice di uscita pari a zero per l'esecuzione completata, uno per l'esecuzione non riuscita e due per l'esecuzione completata con avvisi.</span><span class="sxs-lookup"><span data-stu-id="ab5a6-119">Additionally, SignTool returns an exit code of zero for successful execution, one for failed execution, and two for execution that completed with warnings.</span></span>

<span data-ttu-id="ab5a6-120">Per informazioni sulla verifica della firma di un file, vedere [uso di SignTool per verificare una firma del file](using-signtool-to-verify-a-file-signature.md).</span><span class="sxs-lookup"><span data-stu-id="ab5a6-120">For information about verifying a file's signature, see [Using SignTool to Verify a File Signature](using-signtool-to-verify-a-file-signature.md).</span></span> <span data-ttu-id="ab5a6-121">Per informazioni sull'aggiunta di un timestamp se il file è già stato firmato, vedere [aggiunta di timestamp ai file firmati in precedenza](adding-time-stamps-to-previously-signed-files.md).</span><span class="sxs-lookup"><span data-stu-id="ab5a6-121">For information about adding a time stamp if the file has already been signed, see [Adding Time Stamps to Previously Signed Files](adding-time-stamps-to-previously-signed-files.md).</span></span> <span data-ttu-id="ab5a6-122">Per ulteriori informazioni su [SignTool](signtool.md), vedere [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="ab5a6-122">For additional information about [SignTool](signtool.md), see [SignTool](signtool.md).</span></span>

 

 
