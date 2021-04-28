---
<span data-ttu-id="83dfa-101">description: metodo IShellDispatch.FindComputer - 'Visualizza la finestra di dialogo Risultati ricerca: Computer.</span><span class="sxs-lookup"><span data-stu-id="83dfa-101">description: IShellDispatch.FindComputer method - 'Displays the Search Results: Computers dialog box.</span></span> <span data-ttu-id="83dfa-102">Nella finestra di dialogo viene visualizzato il risultato della ricerca di un computer specificato."</span><span class="sxs-lookup"><span data-stu-id="83dfa-102">The dialog box shows the result of the search for a specified computer.'</span></span>
<span data-ttu-id="83dfa-103">ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 title: IShellDispatch.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type:</span><span class="sxs-lookup"><span data-stu-id="83dfa-103">ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 title: IShellDispatch.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type:</span></span> 
- <span data-ttu-id="83dfa-104">APIRef</span><span class="sxs-lookup"><span data-stu-id="83dfa-104">APIRef</span></span>
- <span data-ttu-id="83dfa-105">kbSyntax api_name:</span><span class="sxs-lookup"><span data-stu-id="83dfa-105">kbSyntax api_name:</span></span> 
- <span data-ttu-id="83dfa-106">IShellDispatch.FindComputer api_type:</span><span class="sxs-lookup"><span data-stu-id="83dfa-106">IShellDispatch.FindComputer api_type:</span></span> 
- <span data-ttu-id="83dfa-107">Com api_location:</span><span class="sxs-lookup"><span data-stu-id="83dfa-107">COM api_location:</span></span> 
- <span data-ttu-id="83dfa-108">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="83dfa-108">Shell32.dll</span></span>
---

# <a name="ishelldispatchfindcomputer-method"></a><span data-ttu-id="83dfa-109">Metodo IShellDispatch.FindComputer</span><span class="sxs-lookup"><span data-stu-id="83dfa-109">IShellDispatch.FindComputer method</span></span>

<span data-ttu-id="83dfa-110">Visualizza la **finestra di dialogo Risultati ricerca:** Computer .</span><span class="sxs-lookup"><span data-stu-id="83dfa-110">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="83dfa-111">Nella finestra di dialogo viene visualizzato il risultato della ricerca di un computer specificato.</span><span class="sxs-lookup"><span data-stu-id="83dfa-111">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="83dfa-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83dfa-112">Syntax</span></span>


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="83dfa-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="83dfa-113">Parameters</span></span>

<span data-ttu-id="83dfa-114">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="83dfa-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="83dfa-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83dfa-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="83dfa-116">JScript</span><span class="sxs-lookup"><span data-stu-id="83dfa-116">JScript</span></span>

<span data-ttu-id="83dfa-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="83dfa-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="83dfa-118">VB</span><span class="sxs-lookup"><span data-stu-id="83dfa-118">VB</span></span>

<span data-ttu-id="83dfa-119">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="83dfa-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83dfa-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="83dfa-120">Remarks</span></span>

<span data-ttu-id="83dfa-121">Questo metodo viene implementato e accessibile tramite il [**metodo Shell.FindComputer.**](shell-findcomputer.md)</span><span class="sxs-lookup"><span data-stu-id="83dfa-121">This method is implemented and accessed through the [**Shell.FindComputer**](shell-findcomputer.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="83dfa-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="83dfa-122">Examples</span></span>

<span data-ttu-id="83dfa-123">Gli esempi seguenti illustrano l'uso **di FindComputer** in JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="83dfa-123">The following examples show the use of **FindComputer** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="83dfa-124">Jscript:</span><span class="sxs-lookup"><span data-stu-id="83dfa-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



<span data-ttu-id="83dfa-125">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="83dfa-125">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="83dfa-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="83dfa-126">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="83dfa-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83dfa-127">Requirements</span></span>



| <span data-ttu-id="83dfa-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="83dfa-128">Requirement</span></span> | <span data-ttu-id="83dfa-129">Valore</span><span class="sxs-lookup"><span data-stu-id="83dfa-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83dfa-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83dfa-130">Minimum supported client</span></span><br/> | <span data-ttu-id="83dfa-131">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="83dfa-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="83dfa-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83dfa-132">Minimum supported server</span></span><br/> | <span data-ttu-id="83dfa-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="83dfa-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="83dfa-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83dfa-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="83dfa-135"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="83dfa-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="83dfa-136">Idl</span><span class="sxs-lookup"><span data-stu-id="83dfa-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="83dfa-137"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="83dfa-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="83dfa-138">DLL</span><span class="sxs-lookup"><span data-stu-id="83dfa-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83dfa-139"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="83dfa-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




