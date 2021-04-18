---
description: È possibile utilizzare la libreria dei tipi di scripting WMI per chiamare i metodi dell'API di scripting WMI da Microsoft Visual Studio e nei file WSF di Windows script host.
ms.assetid: 6ef4e210-0733-4f2a-89c1-1a7aca5a19d9
ms.tgt_platform: multiple
title: Utilizzo della libreria dei tipi di scripting WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8ba419d9a9b676d798b97e3b1a57f4e038d97814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315185"
---
# <a name="using-the-wmi-scripting-type-library"></a><span data-ttu-id="2a329-103">Utilizzo della libreria dei tipi di scripting WMI</span><span class="sxs-lookup"><span data-stu-id="2a329-103">Using the WMI Scripting Type Library</span></span>

<span data-ttu-id="2a329-104">È possibile utilizzare la libreria dei tipi di scripting WMI per chiamare i metodi dell'API di scripting WMI da Microsoft Visual Studio e nei file WSF di Windows script host.</span><span class="sxs-lookup"><span data-stu-id="2a329-104">You can use the WMI scripting type library to call WMI Scripting API methods from Microsoft Visual Studio and in Windows Script Host WSF files.</span></span>

## <a name="using-the-wmi-scripting-type-library-with-microsoft-visual-studio"></a><span data-ttu-id="2a329-105">Uso della libreria dei tipi di scripting WMI con Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2a329-105">Using the WMI Scripting Type Library with Microsoft Visual Studio</span></span>

> [!Note]  
> <span data-ttu-id="2a329-106">Le funzionalità di Visual InterDev 6,0 sono state integrate in [Microsoft Visual Studio .NET](https://msdn.microsoft.com/vstudio/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="2a329-106">Visual InterDev 6.0 features have been integrated into [Microsoft Visual Studio .NET](https://msdn.microsoft.com/vstudio/default.aspx).</span></span>

 

<span data-ttu-id="2a329-107">Nella procedura seguente viene descritto come abilitare il Integrated Development Environment (IDE) per tenere presente la libreria dei tipi WbemScripting.</span><span class="sxs-lookup"><span data-stu-id="2a329-107">The following procedure describes how to enable the integrated development environment (IDE) to be aware of the WbemScripting type library.</span></span>

<span data-ttu-id="2a329-108">**Per aggiungere la libreria dei tipi di scripting WMI ai riferimenti del progetto**</span><span class="sxs-lookup"><span data-stu-id="2a329-108">**To add the WMI Scripting type library to the project references**</span></span>

1.  <span data-ttu-id="2a329-109">Scegliere **Aggiungi riferimenti** dal menu **progetto** .</span><span class="sxs-lookup"><span data-stu-id="2a329-109">Select **Add References** from the **Project** menu.</span></span>
2.  <span data-ttu-id="2a329-110">Nella scheda COM della casella **Aggiungi riferimento** selezionare libreria Microsoft WMI Scripting v 1.2.</span><span class="sxs-lookup"><span data-stu-id="2a329-110">In the COM tab of the **Add Reference** box, select Microsoft WMI Scripting V1.2 Library.</span></span>
3.  <span data-ttu-id="2a329-111">Se non viene visualizzata alcuna opzione appropriata nell'elenco riferimenti, aggiungerla usando **Sfoglia** nella casella **riferimenti** .</span><span class="sxs-lookup"><span data-stu-id="2a329-111">If no suitable option appears in the References list, add it by using **Browse** in the **References** box.</span></span> <span data-ttu-id="2a329-112">Il **Browse** apre una casella **Aggiungi riferimento** che consente di individuare la libreria dei tipi WbemScripting.</span><span class="sxs-lookup"><span data-stu-id="2a329-112">The **Browse** opens an **Add Reference** box that enables you to locate the WbemScripting type library.</span></span>

    <span data-ttu-id="2a329-113">La libreria dei tipi WbemScripting si trova nel file wbemdisp. tlb nella directory% windir% \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="2a329-113">The WbemScripting type library resides in the file Wbemdisp.tlb in the %windir%\\System32\\Wbem directory.</span></span>

4.  <span data-ttu-id="2a329-114">Selezionare il file e fare clic su **Apri**.</span><span class="sxs-lookup"><span data-stu-id="2a329-114">Select the file and click **Open**.</span></span> <span data-ttu-id="2a329-115">La libreria Microsoft WMI Scripting V 1.2 viene visualizzata nell'elenco riferimenti.</span><span class="sxs-lookup"><span data-stu-id="2a329-115">Microsoft WMI Scripting V1.2 Library appears on the references list.</span></span> <span data-ttu-id="2a329-116">Assicurarsi di selezionare la casella accanto a questo elemento nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="2a329-116">Ensure that you select the box next to this item in the list.</span></span>

## <a name="using-the-wmi-scripting-type-library-with-windows-script-host-20"></a><span data-ttu-id="2a329-117">Uso della libreria dei tipi di scripting WMI con Windows Script Host 2,0</span><span class="sxs-lookup"><span data-stu-id="2a329-117">Using the WMI Scripting Type Library with Windows Script Host 2.0</span></span>

<span data-ttu-id="2a329-118">È possibile includere il riferimento a **WbemScripting. SWbemLocator** in un file WSF di Windows script host, diversamente da uno script scritto in Visual Basic, Scripting Edition o altri linguaggi di scripting.</span><span class="sxs-lookup"><span data-stu-id="2a329-118">You can include the reference to the **WbemScripting.SWbemLocator** in a Windows Script Host WSF file, unlike a script written in Visual Basic, Scripting Edition or other scripting languages.</span></span> <span data-ttu-id="2a329-119">In questo modo è possibile utilizzare nomi costanti anziché valori.</span><span class="sxs-lookup"><span data-stu-id="2a329-119">This enables you to use constant names instead of values.</span></span> <span data-ttu-id="2a329-120">Ad esempio, usare **WbemAuthenticationLevelPktPrivacy** invece del valore 6 quando si imposta l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="2a329-120">For example, use **WbemAuthenticationLevelPktPrivacy** rather than the value 6 when setting authentication.</span></span>

<span data-ttu-id="2a329-121">Gli script possono connettersi con l'API di scripting per la libreria dei tipi WMI usando i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2a329-121">Scripts can connect with the Scripting API for WMI type library using the following methods:</span></span>

-   <span data-ttu-id="2a329-122">Specifica del GUID WbemScripting nei metodi VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) e [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="2a329-122">Specifying the WbemScripting GUID in the VBScript methods [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) and [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).</span></span>

    <span data-ttu-id="2a329-123">Questo avviso Avvisa Windows script host per la connessione al set di oggetti WMI.</span><span class="sxs-lookup"><span data-stu-id="2a329-123">This alerts Windows Script Host to connect to the WMI object set.</span></span>

    <span data-ttu-id="2a329-124">Nell'esempio di codice VBScript seguente viene creato un nuovo oggetto [**SWbemDateTime**](swbemdatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="2a329-124">The following VBScript code example creates a new [**SWbemDateTime**](swbemdatetime.md) object.</span></span>

    ```VB
    Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
    ```

    

-   <span data-ttu-id="2a329-125">Uso della [stringa del moniker](constructing-a-moniker-string.md) "winmgmts:" quando si ottiene un oggetto nuovo o esistente.</span><span class="sxs-lookup"><span data-stu-id="2a329-125">Using the [Moniker string](constructing-a-moniker-string.md) "winmgmts:" when obtaining a new or existing object.</span></span>

    <span data-ttu-id="2a329-126">Nell'esempio di codice VBScript seguente viene usato il moniker "winmgmts:" per ottenere l'istanza del [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) con una proprietà **handle** pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="2a329-126">The following VBScript code example uses the "winmgmts:" moniker to get the instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) with a **Handle** property of 0 (zero).</span></span> <span data-ttu-id="2a329-127">**Handle** è la proprietà chiave per questa classe.</span><span class="sxs-lookup"><span data-stu-id="2a329-127">**Handle** is the key property for this class.</span></span>

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process.Handle=0")
    ```

    

-   <span data-ttu-id="2a329-128">Riferimento alla libreria dei tipi WMI utilizzando il <reference> tag del formato di file XML WSH 2,0.</span><span class="sxs-lookup"><span data-stu-id="2a329-128">Referencing the WMI type library using the <reference> tag of the WSH 2.0 XML file format.</span></span> <span data-ttu-id="2a329-129">Se si usa il <reference> tag, il tag deve avere un attributo **UUID** il cui valore è il **GUID** della libreria dei tipi WMI oppure (scelta consigliata) un attributo di oggetto il cui valore è il **ProgID** di uno degli oggetti di script WMI che è possibile creare.</span><span class="sxs-lookup"><span data-stu-id="2a329-129">If you use the <reference> tag, the tag must have either a **uuid** attribute whose value is the **GUID** of the WMI type library, or (recommended) an object attribute whose value is the **PROGID** of any of the WMI scripting objects you can create.</span></span>

    <span data-ttu-id="2a329-130">Nell'esempio di codice VBScript seguente viene usato il PROGID di "WbemScripting".</span><span class="sxs-lookup"><span data-stu-id="2a329-130">The following VBScript code example uses the PROGID of "WbemScripting" .</span></span> <span data-ttu-id="2a329-131">Per eseguire lo script, salvare il testo in un file con estensione wsf.</span><span class="sxs-lookup"><span data-stu-id="2a329-131">To run the script, save the text in a file with a .wsf extension.</span></span>

    ```VB
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
    <reference object="WbemScripting.SWbemLocator"/>
    <script language="VBScript">
        set service = GetObject("winmgmts:")
        ' Following line uses a symbolic 
        ' constant from the WMI type library
        service.Security_.impersonationLevel = _
            wbemImpersonationLevelDelegate
    </script>
    </job>
    ```

    

-   <span data-ttu-id="2a329-132">Utilizzando un <**oggetto**> tag per creare un oggetto di scripting WMI.</span><span class="sxs-lookup"><span data-stu-id="2a329-132">Using an <**object**> tag to create a WMI scripting object.</span></span> <span data-ttu-id="2a329-133">È possibile specificare l'attributo **ID** con il valore di un nome che fa riferimento all'oggetto di scripting WMI che si desidera creare e l'attributo **ProgID** uguale a PROID dell'oggetto di scripting WMI.</span><span class="sxs-lookup"><span data-stu-id="2a329-133">You can specify the **id** attribute with the value of a name that references the WMI scripting object you want to create, and the **progid** attribute equal to the PROID of the WMI scripting object.</span></span>

    <span data-ttu-id="2a329-134">Nello script WSH seguente vengono visualizzati il nome host e il numero di processori nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="2a329-134">The following WSH script displays the hostname and the number of processors on the local computer.</span></span> <span data-ttu-id="2a329-135">Per eseguire lo script, salvare il testo in un file con estensione wsf.</span><span class="sxs-lookup"><span data-stu-id="2a329-135">To run the script, save the text in a file with a .wsf extension.</span></span>

    ```XML
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
     <object id="objSWbemLocator" progid="WbemScripting.SWbemLocator"/>
     <script language="VBScript">

      strComputer = "."
      Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
      Set colSettings = objSWbemServices.ExecQuery("Select * From Win32_ComputerSystem")
      For Each objComputer in colSettings
       Wscript.Echo "System Name: " & objComputer.Name
       Wscript.Echo "Number of Processors: " & objComputer.NumberOfProcessors
      Next

     </script>
    </job>
    ```

    

## <a name="related-topics"></a><span data-ttu-id="2a329-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2a329-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a329-137">Creazione di script in WMI</span><span class="sxs-lookup"><span data-stu-id="2a329-137">Scripting in WMI</span></span>](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> <dt>

[<span data-ttu-id="2a329-138">API di scripting per WMI</span><span class="sxs-lookup"><span data-stu-id="2a329-138">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 
