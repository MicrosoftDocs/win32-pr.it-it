---
description: "Metodo IShellDispatch2.ShellExecute: esegue un'operazione specificata su un file specificato."
ms.assetid: a55e804c-ed7c-4b22-b86f-8e5653976654
title: Metodo IShellDispatch2.ShellExecute (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5c058275948d5d96805ae24a76389321d7c69b8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117019"
---
# <a name="ishelldispatch2shellexecute-method"></a><span data-ttu-id="6cd0f-103">Metodo IShellDispatch2.ShellExecute</span><span class="sxs-lookup"><span data-stu-id="6cd0f-103">IShellDispatch2.ShellExecute method</span></span>

<span data-ttu-id="6cd0f-104">Esegue un'operazione specificata su un file specificato.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-104">Performs a specified operation on a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cd0f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6cd0f-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
)
```


```VB

IShellDispatch2.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="6cd0f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6cd0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cd0f-107">*sFile* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6cd0f-107">*sFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd0f-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="6cd0f-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="6cd0f-109">Valore **String** contenente il nome del file in cui **ShellExecute** eseguirà l'azione specificata da *vOperation.*</span><span class="sxs-lookup"><span data-stu-id="6cd0f-109">A **String** that contains the name of the file on which **ShellExecute** will perform the action specified by *vOperation*.</span></span>

</dd> <dt>

<span data-ttu-id="6cd0f-110">*vArguments* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6cd0f-110">*vArguments* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd0f-111">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="6cd0f-111">Type: **Variant**</span></span>

<span data-ttu-id="6cd0f-112">Stringa che contiene i valori dei parametri per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-112">A string that contains parameter values for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6cd0f-113">*vDirectory* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6cd0f-113">*vDirectory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd0f-114">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="6cd0f-114">Type: **Variant**</span></span>

<span data-ttu-id="6cd0f-115">Percorso completo della directory che contiene il file specificato da *sFile*.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-115">The fully qualified path of the directory that contains the file specified by *sFile*.</span></span> <span data-ttu-id="6cd0f-116">Se questo parametro non viene specificato, viene utilizzata la directory di lavoro corrente.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-116">If this parameter is not specified, the current working directory is used.</span></span>

</dd> <dt>

<span data-ttu-id="6cd0f-117">*vOperation* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6cd0f-117">*vOperation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd0f-118">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="6cd0f-118">Type: **Variant**</span></span>

<span data-ttu-id="6cd0f-119">L'operazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-119">The operation to be performed.</span></span> <span data-ttu-id="6cd0f-120">Questo valore è impostato su una delle stringhe verbo supportate dal file.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-120">This value is set to one of the verb strings that is supported by the file.</span></span> <span data-ttu-id="6cd0f-121">Per una descrizione dei verbi, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-121">For a discussion of verbs, see the Remarks section.</span></span> <span data-ttu-id="6cd0f-122">Se questo parametro non viene specificato, viene eseguita l'operazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-122">If this parameter is not specified, the default operation is performed.</span></span>

</dd> <dt>

<span data-ttu-id="6cd0f-123">*vShow* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="6cd0f-123">*vShow* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd0f-124">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="6cd0f-124">Type: **Variant**</span></span>

<span data-ttu-id="6cd0f-125">Raccomandazione su come visualizzare inizialmente la finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-125">A recommendation as to how the application window should be displayed initially.</span></span> <span data-ttu-id="6cd0f-126">L'applicazione può ignorare questa raccomandazione.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-126">The application can ignore this recommendation.</span></span> <span data-ttu-id="6cd0f-127">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-127">This parameter can be one of the following values.</span></span> <span data-ttu-id="6cd0f-128">Se questo parametro non viene specificato, l'applicazione usa il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-128">If this parameter is not specified, the application uses its default value.</span></span>



| <span data-ttu-id="6cd0f-129">Valore</span><span class="sxs-lookup"><span data-stu-id="6cd0f-129">Value</span></span>                                                                                                                               | <span data-ttu-id="6cd0f-130">Significato</span><span class="sxs-lookup"><span data-stu-id="6cd0f-130">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6cd0f-131"><dt></dt><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6cd0f-131"><dt></dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="6cd0f-132">Aprire l'applicazione con una finestra nascosta.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-132">Open the application with a hidden window.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="6cd0f-133"><dt></dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6cd0f-133"><dt></dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="6cd0f-134">Aprire l'applicazione con una finestra normale.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-134">Open the application with a normal window.</span></span> <span data-ttu-id="6cd0f-135">Se la finestra è ridotta a icona o ingrandita, il sistema la ripristina alle dimensioni e alla posizione originali.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-135">If the window is minimized or maximized, the system restores it to its original size and position.</span></span><br/> |
| <dl> <span data-ttu-id="6cd0f-136"><dt></dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6cd0f-136"><dt></dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="6cd0f-137">Aprire l'applicazione con una finestra ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-137">Open the application with a minimized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="6cd0f-138"><dt></dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6cd0f-138"><dt></dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="6cd0f-139">Aprire l'applicazione con una finestra ingrandita.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-139">Open the application with a maximized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="6cd0f-140"><dt></dt><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6cd0f-140"><dt></dt> <dt>4</dt></span></span> </dl>  | <span data-ttu-id="6cd0f-141">Aprire l'applicazione con la relativa finestra con le dimensioni e la posizione più recenti.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-141">Open the application with its window at its most recent size and position.</span></span> <span data-ttu-id="6cd0f-142">La finestra attiva rimane attiva.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-142">The active window remains active.</span></span><br/>                                  |
| <dl> <span data-ttu-id="6cd0f-143"><dt></dt><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="6cd0f-143"><dt></dt> <dt>5</dt></span></span> </dl>  | <span data-ttu-id="6cd0f-144">Aprire l'applicazione con la relativa finestra con le dimensioni e la posizione correnti.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-144">Open the application with its window at its current size and position.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="6cd0f-145"><dt></dt><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="6cd0f-145"><dt></dt> <dt>7</dt></span></span> </dl>  | <span data-ttu-id="6cd0f-146">Aprire l'applicazione con una finestra ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-146">Open the application with a minimized window.</span></span> <span data-ttu-id="6cd0f-147">La finestra attiva rimane attiva.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-147">The active window remains active.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="6cd0f-148"><dt></dt><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="6cd0f-148"><dt></dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="6cd0f-149">Aprire l'applicazione con la relativa finestra nello stato predefinito specificato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-149">Open the application with its window in the default state specified by the application.</span></span><br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6cd0f-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="6cd0f-150">Remarks</span></span>

<span data-ttu-id="6cd0f-151">Questo metodo viene implementato e accessibile tramite il [**metodo Shell.ShellExecute.**](./shell-shellexecute.md)</span><span class="sxs-lookup"><span data-stu-id="6cd0f-151">This method is implemented and accessed through the [**Shell.ShellExecute**](./shell-shellexecute.md) method.</span></span>

<span data-ttu-id="6cd0f-152">Questo metodo equivale all'avvio di uno dei comandi associati al menu di scelta rapida di un file.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-152">This method is equivalent to launching one of the commands associated with a file's shortcut menu.</span></span> <span data-ttu-id="6cd0f-153">Ogni comando è rappresentato da una stringa verbo.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-153">Each command is represented by a verb string.</span></span> <span data-ttu-id="6cd0f-154">Il set di verbi supportati varia da file a file.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-154">The set of supported verbs varies from file to file.</span></span> <span data-ttu-id="6cd0f-155">Il verbo più comunemente supportato è "open", che in genere è anche il verbo predefinito.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-155">The most commonly supported verb is "open", which is also usually the default verb.</span></span> <span data-ttu-id="6cd0f-156">Altri verbi potrebbero essere supportati solo da determinati tipi di file.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-156">Other verbs might be supported by only certain types of files.</span></span> <span data-ttu-id="6cd0f-157">Per altre informazioni sui verbi della shell, vedere [Avvio di applicazioni o](launch.md) Estensione dei menu di scelta [rapida.](context.md)</span><span class="sxs-lookup"><span data-stu-id="6cd0f-157">For further discussion of Shell verbs, see [Launching Applications](launch.md) or [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="6cd0f-158">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-158">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="6cd0f-159">Esempio</span><span class="sxs-lookup"><span data-stu-id="6cd0f-159">Examples</span></span>

<span data-ttu-id="6cd0f-160">Gli esempi seguenti illustrano l'uso di **ShellExecute per** aprire il Blocco note.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-160">The following examples show the use of **ShellExecute** to open Notepad.</span></span> <span data-ttu-id="6cd0f-161">L'utilizzo viene visualizzato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="6cd0f-161">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="6cd0f-162">Jscript:</span><span class="sxs-lookup"><span data-stu-id="6cd0f-162">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExecuteJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShellExecute("notepad.exe", "", "", "open", 1);
    }
</script>
```



<span data-ttu-id="6cd0f-163">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="6cd0f-163">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExecuteVB()
        dim objShell

        set objShell = CreateObject("shell.application")

        objShell.ShellExecute "notepad.exe", "", "", "open", 1

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="6cd0f-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6cd0f-164">Requirements</span></span>



| <span data-ttu-id="6cd0f-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cd0f-165">Requirement</span></span> | <span data-ttu-id="6cd0f-166">Valore</span><span class="sxs-lookup"><span data-stu-id="6cd0f-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cd0f-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6cd0f-167">Minimum supported client</span></span><br/> | <span data-ttu-id="6cd0f-168">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6cd0f-168">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6cd0f-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6cd0f-169">Minimum supported server</span></span><br/> | <span data-ttu-id="6cd0f-170">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6cd0f-170">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6cd0f-171">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6cd0f-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cd0f-172"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="6cd0f-172"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="6cd0f-173">Idl</span><span class="sxs-lookup"><span data-stu-id="6cd0f-173">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6cd0f-174"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="6cd0f-174"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="6cd0f-175">DLL</span><span class="sxs-lookup"><span data-stu-id="6cd0f-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cd0f-176"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="6cd0f-176"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
