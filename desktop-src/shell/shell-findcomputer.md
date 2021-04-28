---
<span data-ttu-id="7d2b0-101">description: metodo Shell.FindComputer - 'Visualizza la finestra di dialogo Risultati ricerca: Computer.</span><span class="sxs-lookup"><span data-stu-id="7d2b0-101">description: Shell.FindComputer method - 'Displays the Search Results: Computers dialog box.</span></span> <span data-ttu-id="7d2b0-102">La finestra di dialogo mostra il risultato della ricerca di un computer specificato."</span><span class="sxs-lookup"><span data-stu-id="7d2b0-102">The dialog box shows the result of the search for a specified computer.'</span></span>
<span data-ttu-id="7d2b0-103">ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360 title: Shell.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type:</span><span class="sxs-lookup"><span data-stu-id="7d2b0-103">ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360 title: Shell.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type:</span></span> 
- <span data-ttu-id="7d2b0-104">APIRef</span><span class="sxs-lookup"><span data-stu-id="7d2b0-104">APIRef</span></span>
- <span data-ttu-id="7d2b0-105">kbSyntax api_name:</span><span class="sxs-lookup"><span data-stu-id="7d2b0-105">kbSyntax api_name:</span></span> 
- <span data-ttu-id="7d2b0-106">Shell.FindComputer api_type:</span><span class="sxs-lookup"><span data-stu-id="7d2b0-106">Shell.FindComputer api_type:</span></span> 
- <span data-ttu-id="7d2b0-107">Com api_location:</span><span class="sxs-lookup"><span data-stu-id="7d2b0-107">COM api_location:</span></span> 
- <span data-ttu-id="7d2b0-108">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="7d2b0-108">Shell32.dll</span></span>
---

# <a name="shellfindcomputer-method"></a><span data-ttu-id="7d2b0-109">Metodo Shell.FindComputer</span><span class="sxs-lookup"><span data-stu-id="7d2b0-109">Shell.FindComputer method</span></span>

<span data-ttu-id="7d2b0-110">Visualizza la **finestra di dialogo Risultati ricerca:** Computer.</span><span class="sxs-lookup"><span data-stu-id="7d2b0-110">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="7d2b0-111">Nella finestra di dialogo viene visualizzato il risultato della ricerca di un computer specificato.</span><span class="sxs-lookup"><span data-stu-id="7d2b0-111">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d2b0-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d2b0-112">Syntax</span></span>


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="7d2b0-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d2b0-113">Parameters</span></span>

<span data-ttu-id="7d2b0-114">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7d2b0-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7d2b0-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d2b0-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="7d2b0-116">JScript</span><span class="sxs-lookup"><span data-stu-id="7d2b0-116">JScript</span></span>

<span data-ttu-id="7d2b0-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7d2b0-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="7d2b0-118">VB</span><span class="sxs-lookup"><span data-stu-id="7d2b0-118">VB</span></span>

<span data-ttu-id="7d2b0-119">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7d2b0-119">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="7d2b0-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="7d2b0-120">Examples</span></span>

<span data-ttu-id="7d2b0-121">L'esempio seguente mostra **FindComputer** in uso.</span><span class="sxs-lookup"><span data-stu-id="7d2b0-121">The following example shows **FindComputer** in use.</span></span> <span data-ttu-id="7d2b0-122">Il risultato di questo codice è lo stesso che si fa premendo il pulsante **Start,** facendo clic su **Cerca**, facendo clic sull'opzione **Stampanti,** computer o persone, quindi facendo clic su Un **computer nella rete**.</span><span class="sxs-lookup"><span data-stu-id="7d2b0-122">The result of this code is the same as pressing the **Start** button, clicking **Search**, clicking the **Printers, computers, or people** option, then clicking **A computer on the network**.</span></span> <span data-ttu-id="7d2b0-123">Viene illustrato l'utilizzo corretto per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7d2b0-123">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7d2b0-124">Jscript:</span><span class="sxs-lookup"><span data-stu-id="7d2b0-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
    }
</script>
```



<span data-ttu-id="7d2b0-125">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="7d2b0-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="7d2b0-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="7d2b0-126">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="7d2b0-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d2b0-127">Requirements</span></span>



| <span data-ttu-id="7d2b0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d2b0-128">Requirement</span></span> | <span data-ttu-id="7d2b0-129">Valore</span><span class="sxs-lookup"><span data-stu-id="7d2b0-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d2b0-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d2b0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7d2b0-131">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7d2b0-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7d2b0-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d2b0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7d2b0-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7d2b0-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7d2b0-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d2b0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d2b0-135"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="7d2b0-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7d2b0-136">Idl</span><span class="sxs-lookup"><span data-stu-id="7d2b0-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7d2b0-137"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="7d2b0-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7d2b0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7d2b0-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d2b0-139"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="7d2b0-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




