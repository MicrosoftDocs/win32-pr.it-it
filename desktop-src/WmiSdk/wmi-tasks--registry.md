---
description: Le attività WMI per il registro di sistema creano e modificano chiavi e valori del registro di sistema. Per altri esempi, vedere il sito TechNet ScriptCenter all'indirizzo https://www.microsoft.com/technet .
ms.assetid: 0785189e-9638-4776-8414-1414d7b02524
ms.tgt_platform: multiple
title: 'Attività WMI: Registro di sistema'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df6ae73d41c9cbfd6cd303b72e1b9207f3191c85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316556"
---
# <a name="wmi-tasks-registry"></a><span data-ttu-id="aff0e-104">Attività WMI: Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="aff0e-104">WMI Tasks: Registry</span></span>

<span data-ttu-id="aff0e-105">Le attività WMI per il registro di sistema creano e modificano chiavi e valori del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="aff0e-105">WMI tasks for the registry create and modify registry keys and values.</span></span> <span data-ttu-id="aff0e-106">Per altri esempi, vedere il sito TechNet ScriptCenter all'indirizzo [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="aff0e-106">For other examples, see the TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx).</span></span>

<span data-ttu-id="aff0e-107">Gli esempi di script illustrati in questo argomento ottengono dati solo dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="aff0e-107">The script examples shown in this topic obtain data only from the local computer.</span></span> <span data-ttu-id="aff0e-108">Per ulteriori informazioni sull'utilizzo dello script per ottenere dati da computer remoti, vedere la pagina [relativa alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="aff0e-108">For more information about how to use the script to obtain data from remote computers, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>


<span data-ttu-id="aff0e-109">Nella procedura riportata di seguito viene descritto come eseguire uno script.</span><span class="sxs-lookup"><span data-stu-id="aff0e-109">The following procedure describes how to run a script.</span></span>

<span data-ttu-id="aff0e-110">**Per eseguire uno script**</span><span class="sxs-lookup"><span data-stu-id="aff0e-110">**To run a script**</span></span>

1.  <span data-ttu-id="aff0e-111">Copiare il codice e salvarlo in un file con estensione vbs, ad esempio *filename.vbs*.</span><span class="sxs-lookup"><span data-stu-id="aff0e-111">Copy the code and save it in a file with a .vbs extension, such as *filename.vbs*.</span></span> <span data-ttu-id="aff0e-112">Assicurarsi che l'editor di testo non aggiunga un'estensione txt al file.</span><span class="sxs-lookup"><span data-stu-id="aff0e-112">Ensure that your text editor does not add a .txt extension to the file.</span></span>
2.  <span data-ttu-id="aff0e-113">Aprire una finestra del prompt dei comandi e passare alla directory in cui è stato salvato il file.</span><span class="sxs-lookup"><span data-stu-id="aff0e-113">Open a command prompt window and navigate to the directory where you saved the file.</span></span>
3.  <span data-ttu-id="aff0e-114">Digitare **cscript filename.vbs** al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="aff0e-114">Type **cscript filename.vbs** at the command prompt.</span></span>
4.  <span data-ttu-id="aff0e-115">Se non è possibile accedere a un registro eventi, verificare che sia in esecuzione da un prompt dei comandi con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="aff0e-115">If you cannot access an event log, check to see if you are running from an Elevated command prompt.</span></span> <span data-ttu-id="aff0e-116">Alcuni log eventi, ad esempio il registro eventi di sicurezza, possono essere protetti da controlli di accesso utente (UAC).</span><span class="sxs-lookup"><span data-stu-id="aff0e-116">Some Event Log, such as the Security Event Log, may be protected by User Access Controls (UAC).</span></span>

> [!Note]  
> <span data-ttu-id="aff0e-117">Per impostazione predefinita, cscript Visualizza l'output di uno script nella finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="aff0e-117">By default, cscript displays the output of a script in the command prompt window.</span></span> <span data-ttu-id="aff0e-118">Poiché gli script WMI possono produrre grandi quantità di output, potrebbe essere necessario reindirizzare l'output a un file.</span><span class="sxs-lookup"><span data-stu-id="aff0e-118">Because WMI scripts can produce large amounts of output, you might want to redirect the output to a file.</span></span> <span data-ttu-id="aff0e-119">Digitare **cscript filename.vbs > outfile.txt** al prompt dei comandi per reindirizzare l'output dello script *filename.vbs* a *outfile.txt*.</span><span class="sxs-lookup"><span data-stu-id="aff0e-119">Type **cscript filename.vbs > outfile.txt** at the command prompt to redirect the output of the *filename.vbs* script to *outfile.txt*.</span></span>

 

<span data-ttu-id="aff0e-120">Nella tabella seguente sono elencati esempi di script che è possibile utilizzare per ottenere vari tipi di dati dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="aff0e-120">The following table lists script examples that can be used to obtain various types of data from the local computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff0e-121">Ricerca per categorie</span><span class="sxs-lookup"><span data-stu-id="aff0e-121">How do I...</span></span></th>
<th><span data-ttu-id="aff0e-122">Classi o metodi WMI</span><span class="sxs-lookup"><span data-stu-id="aff0e-122">WMI classes or methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aff0e-123">... leggere i valori delle chiavi del registro di sistema tramite WMI?</span><span class="sxs-lookup"><span data-stu-id="aff0e-123">...read registry key values using WMI?</span></span></td>
<td><span data-ttu-id="aff0e-124">Usare la classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>WMI StdRegProv</strong></a> , che si trova nello spazio dei nomi root\default.</span><span class="sxs-lookup"><span data-stu-id="aff0e-124">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace.</span></span> <span data-ttu-id="aff0e-125">Non è possibile ottenere alcuna istanza di questa classe perché il <a href="/previous-versions/windows/desktop/regprov/system-registry-provider">provider del registro di sistema</a> è solo un metodo e un provider di eventi.</span><span class="sxs-lookup"><span data-stu-id="aff0e-125">You cannot get any instances of this class because the <a href="/previous-versions/windows/desktop/regprov/system-registry-provider">System Registry Provider</a> is a method and event provider only.</span></span> <span data-ttu-id="aff0e-126">Tuttavia, è possibile ottenere i dati del registro di sistema tramite metodi quali <a href="/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov"><strong>EnumKey</strong></a> o <a href="/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov"><strong>EnumValue</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aff0e-126">However, you can get registry data through methods such as <a href="/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov"><strong>EnumKey</strong></a> or <a href="/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov"><strong>EnumValue</strong></a>.</span></span> <span data-ttu-id="aff0e-127">Il <a href="/windows/desktop/CIMWin32Prov/win32-registry"><strong>Win32_Registry</strong></a>, situato nello spazio dei nomi root\cimv2, ottiene i dati sul Registro di sistema nel suo complesso, ad esempio le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="aff0e-127">The <a href="/windows/desktop/CIMWin32Prov/win32-registry"><strong>Win32_Registry</strong></a>, located in root\cimv2 namespace, gets data about the registry as a whole, such as how large it is.</span></span><br/> <span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff0e-128">VB</span><span class="sxs-lookup"><span data-stu-id="aff0e-128">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_CURRENT_USER = &H80000001
strComputer = &quot;.&quot;
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
strKeyPath = &quot;Console&quot;
strValueName = &quot;HistoryBufferSize&quot;
oReg.GetDWORDValue HKEY_CURRENT_USER,strKeyPath,strValueName,dwValue
WScript.Echo &quot;Current History Buffer Size: &quot; & dwValue</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff0e-129">PowerShell</span><span class="sxs-lookup"><span data-stu-id="aff0e-129">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_CURRENT_USER =2147483649
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key = &quot;Console&quot;
$Value = &quot;HistoryBufferSize&quot;
$results = $reg.GetDWORDValue($HKEY_CURRENT_USER, $Key, $value)
&quot;Current History Buffer Size: {0}&quot; -f $results.uValue</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff0e-130">... creare una nuova chiave del registro di sistema?</span><span class="sxs-lookup"><span data-stu-id="aff0e-130">...create a new registry key?</span></span></td>
<td><p><span data-ttu-id="aff0e-131">Usare la classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>WMI StdRegProv</strong></a> , che si trova nello spazio dei nomi root\default e il metodo <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="aff0e-131">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace, and the <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> method.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff0e-132">VB</span><span class="sxs-lookup"><span data-stu-id="aff0e-132">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strComputer = &quot;.&quot;
Set objReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)

strKeyPath = &quot;SOFTWARE\NewKey&quot;
objReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
WScript.Echo &quot;Created registry key HKEY_LOCAL_MACHINE\SOFTWARE\NewKey&quot;</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff0e-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="aff0e-133">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key     = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.CreateKey($HKEY_LOCAL_MACHINE, $Key)
If ($results.Returnvalue -eq 0) {&quot;Key created&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff0e-134">... creare un nuovo valore del registro di sistema in una chiave?</span><span class="sxs-lookup"><span data-stu-id="aff0e-134">...create a new registry value under a key?</span></span></td>
<td><p><span data-ttu-id="aff0e-135">Usare la classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>WMI StdRegProv</strong></a> , che si trova nello spazio dei nomi root\default e il metodo <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="aff0e-135">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in the root\default namespace, and the <a href="/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov"><strong>CreateKey</strong></a> method.</span></span> <span data-ttu-id="aff0e-136">Usare quindi uno dei metodi set, a seconda del tipo di dati del registro di sistema in cui si trova il valore, ad esempio <a href="/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov"><strong>SetDWORDValue</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="aff0e-136">Then use one of the Set methods, depending on what registry datatype the value is, such as the <a href="/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov"><strong>SetDWORDValue</strong></a>.</span></span> <span data-ttu-id="aff0e-137">I metodi set creano un valore se non esiste già.</span><span class="sxs-lookup"><span data-stu-id="aff0e-137">The Set methods create a value if it does not already exist.</span></span> <span data-ttu-id="aff0e-138">Per ulteriori informazioni, vedere <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">mapping di un tipo di dati del registro di sistema a un tipo di dati WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="aff0e-138">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff0e-139">VB</span><span class="sxs-lookup"><span data-stu-id="aff0e-139">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
Set objReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
strValueName = &quot;Example_Expanded_String_Value&quot;
strValue = &quot;%PATHEXT%&quot;
objReg.SetExpandedStringValue HKEY_LOCAL_MACHINE,strKeyPath,strValueName,strValue
WScript.Echo &quot;Example expanded_String_Value at &quot; & &quot;HKEY_LOCAL_MACHINE\SOFTWARE\NewKey&quot;</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff0e-140">PowerShell</span><span class="sxs-lookup"><span data-stu-id="aff0e-140">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$ValueName = &quot;Example_Expanded_String_Value&quot;
$Value     = &quot;%PATHEXT%&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.SetExpandedStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName, $Value)
If ($results.Returnvalue -eq 0) {&quot;Value created&quot;}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff0e-141">... evitare di ottenere un errore di classe non valido quando si tenta di scrivere uno script per leggere il registro di sistema?</span><span class="sxs-lookup"><span data-stu-id="aff0e-141">...avoid getting an Invalid Class error when trying to write a script to read the registry?</span></span></td>
<td><p><span data-ttu-id="aff0e-142">Usare lo spazio dei nomi root\default quando si accede alla classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>WMI StdRegProv</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="aff0e-142">Use the root\default namespace when accessing the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class.</span></span> <span data-ttu-id="aff0e-143"><strong>WMI StdRegProv</strong> non fa parte dello spazio dei nomi CIMV2, motivo per cui &quot; viene generato un errore di classe non valido &quot; se si tenta di connettersi a &quot; root\cimv2: WMI StdRegProv &quot; .</span><span class="sxs-lookup"><span data-stu-id="aff0e-143"><strong>StdRegProv</strong> is not part of the cimv2 namespace, which is why an &quot;Invalid Class&quot; error is generated if you try to connect to &quot;root\cimv2:StdRegProv&quot;.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff0e-144">VB</span><span class="sxs-lookup"><span data-stu-id="aff0e-144">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>Const HKEY_CURRENT_USER = &H80000001
strComputer = &quot;.&quot;
Set oReg=GetObject( &quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;) 
strKeyPath = &quot;Console&quot;
strValueName = &quot;HistoryBufferSize&quot;
oReg.GetDWORDValue HKEY_CURRENT_USER, strKeyPath, strValueName, dwValue
Wscript.Echo &quot;Current History Buffer Size: &quot; & dwValue</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff0e-145">... verificare la sicurezza in una chiave del registro di sistema specifica.</span><span class="sxs-lookup"><span data-stu-id="aff0e-145">...check security on a specific registry key?</span></span></td>
<td><p><span data-ttu-id="aff0e-146">Usare la classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>WMI StdRegProv</strong></a> , che si trova nello spazio dei nomi root\default e il metodo <a href="/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov"><strong>CheckAccess</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="aff0e-146">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov"><strong>CheckAccess</strong></a> method.</span></span> <span data-ttu-id="aff0e-147">È possibile controllare solo i diritti di accesso per l'utente corrente che esegue lo script o l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="aff0e-147">You can only check the access rights for the current user that is running the script or application.</span></span> <span data-ttu-id="aff0e-148">Non è possibile controllare i diritti di accesso per un altro utente specificato.</span><span class="sxs-lookup"><span data-stu-id="aff0e-148">You cannot check the access rights for another specified user.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff0e-149">... leggere e scrivere i valori di registro binari?</span><span class="sxs-lookup"><span data-stu-id="aff0e-149">...read and write binary registry values?</span></span></td>
<td><p><span data-ttu-id="aff0e-150">Usare la classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>WMI StdRegProv</strong></a> , che si trova nello &quot; &quot; spazio dei nomi Root\Default e i metodi <a href="/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov"><strong>getBinaryValue</strong></a> e <a href="/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov"><strong>SetBinaryValue</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="aff0e-150">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in &quot;Root\Default&quot; namespace and the <a href="/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov"><strong>GetBinaryValue</strong></a> and <a href="/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov"><strong>SetBinaryValue</strong></a> methods.</span></span> <span data-ttu-id="aff0e-151">I valori del registro di sistema visualizzati nell'utilità RegEdt32 come una serie di valori esadecimali byte sono nel formato dati <strong>REG_BINARY</strong> .</span><span class="sxs-lookup"><span data-stu-id="aff0e-151">Registry values that appear in the RegEdt32 utility as a series of byte hexadecimal values are in the <strong>REG_BINARY</strong> data format.</span></span> <span data-ttu-id="aff0e-152">Per ulteriori informazioni, vedere <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">mapping di un tipo di dati del registro di sistema a un tipo di dati WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="aff0e-152">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span> <span data-ttu-id="aff0e-153">Nell'esempio di codice VBScript riportato di seguito viene creata una nuova chiave con un valore binario.</span><span class="sxs-lookup"><span data-stu-id="aff0e-153">The following VBScript code example creates a new key with a binary value.</span></span> <span data-ttu-id="aff0e-154">Il valore binario viene fornito nella matrice di byte <em>iValues</em> specificata in esadecimale.</span><span class="sxs-lookup"><span data-stu-id="aff0e-154">The binary value is supplied in the <em>iValues</em> byte array specified in Hex.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff0e-155">VB</span><span class="sxs-lookup"><span data-stu-id="aff0e-155">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
iValues = Array(&H01,&Ha2,&H10)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
strKeyPath = &quot;SOFTWARE\NewKey&quot;
BinaryValueName = &quot;Example Binary Value&quot;

oReg.SetBinaryValue HKEY_LOCAL_MACHINE,strKeyPath,BinaryValueName,iValues</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="aff0e-156">Nello script seguente viene letto il valore binario.</span><span class="sxs-lookup"><span data-stu-id="aff0e-156">The following script reads the binary value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff0e-157">VB</span><span class="sxs-lookup"><span data-stu-id="aff0e-157">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002 
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strValueName = &quot;Example Binary Value&quot;
strComputer = &quot;.&quot;
dim iValues(3)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.GetBinaryValue HKEY_LOCAL_MACHINE,strKeyPath,strValueName,iValues
For i = lBound(iValues) to uBound(iValues)
Wscript.Echo iValues(i)
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff0e-158">PowerShell</span><span class="sxs-lookup"><span data-stu-id="aff0e-158">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$ValueName = &quot;Example Binary Value&quot;
$Values     = @(0x54, 0x46, 0x4C)
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.GetBinaryValue($HKEY_LOCAL_MACHINE, $Key, $ValueName)
Foreach ($byte in $results.uvalue) {&quot;{0}&quot; -f $byte.tostring(&quot;x&quot;)}</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aff0e-159">... leggere e scrivere valori del registro di sistema che contengono più stringhe?</span><span class="sxs-lookup"><span data-stu-id="aff0e-159">...read and write registry values that contain multiple strings?</span></span></td>
<td><p><span data-ttu-id="aff0e-160">Usare la classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>WMI StdRegProv</strong></a> , che si trova nello spazio dei nomi root\default e i metodi <a href="/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov"><strong>GetMultiStringValue</strong></a> e <a href="/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov"><strong>SetMultiStringValue</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="aff0e-160">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov"><strong>GetMultiStringValue</strong></a> and <a href="/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov"><strong>SetMultiStringValue</strong></a> methods.</span></span> <span data-ttu-id="aff0e-161">Le chiavi del registro di sistema visualizzate nell'utilità RegEdt32 come una serie di stringhe separate da spazi sono nel formato dati <strong>REG_MULTI_SZ</strong> .</span><span class="sxs-lookup"><span data-stu-id="aff0e-161">Registry keys that appear in the RegEdt32 utility as a series of strings separated by spaces are in the <strong>REG_MULTI_SZ</strong> data format.</span></span> <span data-ttu-id="aff0e-162">Per ulteriori informazioni, vedere <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">mapping di un tipo di dati del registro di sistema a un tipo di dati WMI</a>.</span><span class="sxs-lookup"><span data-stu-id="aff0e-162">For more information, see <a href="mapping-a-registry-data-type-to-a-wmi-data-type.md">Mapping a Registry Data Type to a WMI Data Type</a>.</span></span> <span data-ttu-id="aff0e-163">Nell'esempio di codice VBScript seguente vengono create una nuova chiave e un nuovo valore multistringa.</span><span class="sxs-lookup"><span data-stu-id="aff0e-163">The following VBScript code example creates a new key and a new multistring value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff0e-164">VB</span><span class="sxs-lookup"><span data-stu-id="aff0e-164">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
MultValueName = &quot;Example Multistring Value&quot;
strComputer = &quot;.&quot;
iValues = Array(&quot;string1&quot;, &quot;string2&quot;)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
oReg.CreateKey HKEY_LOCAL_MACHINE,strKeyPath
oReg.SetMultiStringValue HKEY_LOCAL_MACHINE,strKeyPath,MultValueName,iValues</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff0e-165">PowerShell</span><span class="sxs-lookup"><span data-stu-id="aff0e-165">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$ValueName = &quot;Example MultiString Value&quot;
$Values     = @(&quot;Thomas&quot;, &quot;Susan&quot;, &quot;Rebecca&quot;)
$Key       = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.SetMultiStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName, $Values)
If ($results.Returnvalue -eq 0) {&quot;Value Set&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><span data-ttu-id="aff0e-166">Nello script seguente viene letto il valore multistringa.</span><span class="sxs-lookup"><span data-stu-id="aff0e-166">The following script reads the multistring value.</span></span></p>
<div class="code">
<span data-codelanguage="VisualBasic"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff0e-167">VB</span><span class="sxs-lookup"><span data-stu-id="aff0e-167">VB</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>const HKEY_LOCAL_MACHINE = &H80000002
strKeyPath = &quot;SOFTWARE\NewKey&quot;
strComputer = &quot;.&quot;
iValues = Array(&quot;string1&quot;, &quot;string2&quot;)
Set oReg=GetObject(&quot;winmgmts:{impersonationLevel=impersonate}!\\&quot; & strComputer & &quot;\root\default:StdRegProv&quot;)
MultValueName = &quot;Example Multistring Value&quot;
oReg.GetMultiStringValue HKEY_LOCAL_MACHINE,strKeyPath,MultValueName,iValues
For Each strValue In iValues
WScript.echo strValue
Next</code></pre></td>
</tr>
</tbody>
</table>
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff0e-168">PowerShell</span><span class="sxs-lookup"><span data-stu-id="aff0e-168">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code># Define Constants
$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key       = &quot;SOFTWARE\NewKey&quot;
$ValueName = &quot;Example MultiString Value&quot;
$results   = $reg.GetMultiStringValue($HKEY_LOCAL_MACHINE, $Key, $ValueName)
$results.svalue</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aff0e-169">... rimuovere una chiave del registro di sistema?</span><span class="sxs-lookup"><span data-stu-id="aff0e-169">...remove a registry key?</span></span></td>
<td><p><span data-ttu-id="aff0e-170">Usare la classe <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>WMI StdRegProv</strong></a> , che si trova nello spazio dei nomi root\default e nei metodi <a href="/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov"><strong>DeleteKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="aff0e-170">Use the <a href="/previous-versions/windows/desktop/regprov/stdregprov"><strong>StdRegProv</strong></a> class, located in root\default namespace and the <a href="/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov"><strong>DeleteKey</strong></a> methods.</span></span></p>
<div class="code">
<span data-codelanguage="PowerShell"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aff0e-171">PowerShell</span><span class="sxs-lookup"><span data-stu-id="aff0e-171">PowerShell</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>$HKEY_Local_Machine =2147483650 
$computer =&#39;.&#39;
$reg = [WMIClass]&quot;ROOT\DEFAULT:StdRegProv&quot;
$Key     = &quot;SOFTWARE\NewKey&quot;
$results   = $reg.DeleteKey($HKEY_LOCAL_MACHINE, $Key)
If ($results.Returnvalue -eq 0) {&quot;Key Removed&quot;} </code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="aff0e-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aff0e-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aff0e-173">Attività WMI per script e applicazioni</span><span class="sxs-lookup"><span data-stu-id="aff0e-173">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="aff0e-174">Esempi di applicazioni WMI C++</span><span class="sxs-lookup"><span data-stu-id="aff0e-174">WMI C++ Application Examples</span></span>](wmi-c---application-examples.md)
</dt> <dt>

[<span data-ttu-id="aff0e-175">TechNet ScriptCenter</span><span class="sxs-lookup"><span data-stu-id="aff0e-175">TechNet ScriptCenter</span></span>](https://www.microsoft.com/technet/scriptcenter)
</dt> <dt>

[<span data-ttu-id="aff0e-176">Modifica del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="aff0e-176">Modifying the System Registry</span></span>](modifying-the-system-registry.md)
</dt> <dt>

[<span data-ttu-id="aff0e-177">**WMI StdRegProv**</span><span class="sxs-lookup"><span data-stu-id="aff0e-177">**StdRegProv**</span></span>](/previous-versions/windows/desktop/regprov/stdregprov)
</dt> </dl>
