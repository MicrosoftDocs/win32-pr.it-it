---
description: Recupera un oggetto InternetExplorer che rappresenta la finestra della shell.
ms.assetid: 32390f35-f83a-45d9-a240-282da7cb2b13
title: Metodo ShellWindows. Item (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ccdb73deb1d97d9c6e1ad8c335db3c58d796a299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231921"
---
# <a name="shellwindowsitem-method"></a><span data-ttu-id="561f4-103">Metodo ShellWindows. Item</span><span class="sxs-lookup"><span data-stu-id="561f4-103">ShellWindows.Item method</span></span>

<span data-ttu-id="561f4-104">Recupera un oggetto [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) che rappresenta la finestra della shell.</span><span class="sxs-lookup"><span data-stu-id="561f4-104">Retrieves an [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span>

## <a name="syntax"></a><span data-ttu-id="561f4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="561f4-105">Syntax</span></span>


```JScript
retVal = ShellWindows.Item(
  [ iIndex ]
)
```



## <a name="parameters"></a><span data-ttu-id="561f4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="561f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="561f4-107">*iIndex* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="561f4-107">*iIndex* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="561f4-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="561f4-108">Type: **Variant**</span></span>

<span data-ttu-id="561f4-109">Indice in base zero dell'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="561f4-109">The zero-based index of the item to retrieve.</span></span> <span data-ttu-id="561f4-110">Questo valore deve essere minore del valore della proprietà [**count**](shellwindows-count.md) .</span><span class="sxs-lookup"><span data-stu-id="561f4-110">This value must be less than the value of the [**Count**](shellwindows-count.md) property.</span></span> <span data-ttu-id="561f4-111">Se questo valore viene omesso, viene utilizzato il valore predefinito 0.</span><span class="sxs-lookup"><span data-stu-id="561f4-111">If this value is omitted, a default value of 0 is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="561f4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="561f4-112">Return value</span></span>

<span data-ttu-id="561f4-113">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="561f4-113">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="561f4-114">Riferimento all'oggetto [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) che rappresenta la finestra della shell.</span><span class="sxs-lookup"><span data-stu-id="561f4-114">An object reference to the [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span>

## <a name="examples"></a><span data-ttu-id="561f4-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="561f4-115">Examples</span></span>

<span data-ttu-id="561f4-116">Nell'esempio seguente viene usato [**Item**](folderitemverbs-item.md) per recuperare l'oggetto [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) che rappresenta il primo elemento della finestra della shell.</span><span class="sxs-lookup"><span data-stu-id="561f4-116">The following example uses [**Item**](folderitemverbs-item.md) to retrieve the [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the first Shell window item.</span></span> <span data-ttu-id="561f4-117">L'utilizzo corretto viene visualizzato per JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="561f4-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="561f4-118">JScript</span><span class="sxs-lookup"><span data-stu-id="561f4-118">JScript:</span></span>


```JavaScript
<script language="JScript">
    function fnShellWindowsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();
        if (objShellWindows != null)
        {
            var objIE;
            objIE = objShellWindows.Item();

            if (objIE != null)
            {
                alert(objIE.path());
            }
        }
    }
</script>
```



<span data-ttu-id="561f4-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="561f4-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsItemVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows()

        if (not objShellWindows is nothing) then
            dim objIE
            set objIE = objShellWindows.Item

            if (not objIE is nothing) then
                Wscript.Echo objIE.path
            end if

            set objIE = nothing
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="561f4-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="561f4-120">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsItemVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows()

    If (Not objShellWindows Is Nothing) Then
        Dim objIE As InternetExplorer
        Set objIE = objShellWindows.Item

        If (Not objIE Is Nothing) Then
            Debug.Print objIE.Path
        End If

        Set objIE = Nothing
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="561f4-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="561f4-121">Requirements</span></span>



| <span data-ttu-id="561f4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="561f4-122">Requirement</span></span> | <span data-ttu-id="561f4-123">Valore</span><span class="sxs-lookup"><span data-stu-id="561f4-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="561f4-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="561f4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="561f4-125">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="561f4-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="561f4-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="561f4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="561f4-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="561f4-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="561f4-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="561f4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="561f4-129"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="561f4-129"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="561f4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="561f4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="561f4-131"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="561f4-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
