---
description: Esegue un'operazione specificata su un file specificato.
ms.assetid: 62E59A1C-51BD-4864-AF09-35FFD49FAB9D
title: Metodo Shell.ShellExecute (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 83ab9741199bff675245f15dc2ad1ffb20592a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979887"
---
# <a name="shellshellexecute-method"></a><span data-ttu-id="517ac-103">Shell. ShellExecute, metodo</span><span class="sxs-lookup"><span data-stu-id="517ac-103">Shell.ShellExecute method</span></span>

<span data-ttu-id="517ac-104">Esegue un'operazione specificata su un file specificato.</span><span class="sxs-lookup"><span data-stu-id="517ac-104">Performs a specified operation on a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="517ac-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="517ac-105">Syntax</span></span>

<span data-ttu-id="517ac-106">JScript</span><span class="sxs-lookup"><span data-stu-id="517ac-106">JScript:</span></span>

```js
iRetVal = Shell.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
);
```

<span data-ttu-id="517ac-107">VBScript</span><span class="sxs-lookup"><span data-stu-id="517ac-107">VBScript:</span></span>

```vb
iRetVal = Shell.ShellExecute( _
  sFile, _
  [ ByVal vArguments ], _
  [ ByVal vDirectory ], _
  [ ByVal vOperation ], _
  [ ByVal vShow ] _
)
```

<span data-ttu-id="517ac-108">VB:</span><span class="sxs-lookup"><span data-stu-id="517ac-108">VB:</span></span>

```vb
Shell.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```

## <a name="parameters"></a><span data-ttu-id="517ac-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="517ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="517ac-110">*sfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="517ac-110">*sFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="517ac-111">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="517ac-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="517ac-112">**Stringa** che contiene il nome del file in cui **ShellExecute** eseguirà l'azione specificata da *vOperation*.</span><span class="sxs-lookup"><span data-stu-id="517ac-112">A **String** that contains the name of the file on which **ShellExecute** will perform the action specified by *vOperation*.</span></span>

</dd> <dt>

<span data-ttu-id="517ac-113">*vArguments* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="517ac-113">*vArguments* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="517ac-114">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="517ac-114">Type: **Variant**</span></span>

<span data-ttu-id="517ac-115">Stringa che contiene i valori dei parametri per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="517ac-115">A string that contains parameter values for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="517ac-116">*vDirectory* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="517ac-116">*vDirectory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="517ac-117">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="517ac-117">Type: **Variant**</span></span>

<span data-ttu-id="517ac-118">Percorso completo della directory che contiene il file specificato da *sfile*.</span><span class="sxs-lookup"><span data-stu-id="517ac-118">The fully qualified path of the directory that contains the file specified by *sFile*.</span></span> <span data-ttu-id="517ac-119">Se questo parametro non viene specificato, viene utilizzata la directory di lavoro corrente.</span><span class="sxs-lookup"><span data-stu-id="517ac-119">If this parameter is not specified, the current working directory is used.</span></span>

</dd> <dt>

<span data-ttu-id="517ac-120">*vOperation* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="517ac-120">*vOperation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="517ac-121">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="517ac-121">Type: **Variant**</span></span>

<span data-ttu-id="517ac-122">L'operazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="517ac-122">The operation to be performed.</span></span> <span data-ttu-id="517ac-123">Questo valore è impostato su una delle stringhe dei verbi supportate dal file.</span><span class="sxs-lookup"><span data-stu-id="517ac-123">This value is set to one of the verb strings that is supported by the file.</span></span> <span data-ttu-id="517ac-124">Per informazioni sui verbi, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="517ac-124">For a discussion of verbs, see the Remarks section.</span></span> <span data-ttu-id="517ac-125">Se questo parametro non viene specificato, viene eseguita l'operazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="517ac-125">If this parameter is not specified, the default operation is performed.</span></span>

</dd> <dt>

<span data-ttu-id="517ac-126">*vShow* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="517ac-126">*vShow* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="517ac-127">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="517ac-127">Type: **Variant**</span></span>

<span data-ttu-id="517ac-128">Indicazione relativa alla modalità di visualizzazione iniziale della finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="517ac-128">A recommendation as to how the application window should be displayed initially.</span></span> <span data-ttu-id="517ac-129">Questa raccomandazione può essere ignorata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="517ac-129">The application can ignore this recommendation.</span></span> <span data-ttu-id="517ac-130">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="517ac-130">This parameter can be one of the following values.</span></span> <span data-ttu-id="517ac-131">Se questo parametro non viene specificato, l'applicazione utilizzerà il relativo valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="517ac-131">If this parameter is not specified, the application uses its default value.</span></span>



| <span data-ttu-id="517ac-132">Valore</span><span class="sxs-lookup"><span data-stu-id="517ac-132">Value</span></span>                                                                                                                               | <span data-ttu-id="517ac-133">Significato</span><span class="sxs-lookup"><span data-stu-id="517ac-133">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="517ac-134"><dt></dt><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="517ac-134"><dt></dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="517ac-135">Aprire l'applicazione con una finestra nascosta.</span><span class="sxs-lookup"><span data-stu-id="517ac-135">Open the application with a hidden window.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="517ac-136"><dt></dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="517ac-136"><dt></dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="517ac-137">Aprire l'applicazione con una finestra normale.</span><span class="sxs-lookup"><span data-stu-id="517ac-137">Open the application with a normal window.</span></span> <span data-ttu-id="517ac-138">Se la finestra è ridotta a icona o ingrandita, il sistema ripristina le dimensioni e la posizione originali.</span><span class="sxs-lookup"><span data-stu-id="517ac-138">If the window is minimized or maximized, the system restores it to its original size and position.</span></span><br/> |
| <dl> <span data-ttu-id="517ac-139"><dt></dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="517ac-139"><dt></dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="517ac-140">Aprire l'applicazione con una finestra ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="517ac-140">Open the application with a minimized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="517ac-141"><dt></dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="517ac-141"><dt></dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="517ac-142">Aprire l'applicazione con una finestra ingrandita.</span><span class="sxs-lookup"><span data-stu-id="517ac-142">Open the application with a maximized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="517ac-143"><dt></dt><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="517ac-143"><dt></dt> <dt>4</dt></span></span> </dl>  | <span data-ttu-id="517ac-144">Aprire l'applicazione con la relativa finestra con le dimensioni e la posizione più recenti.</span><span class="sxs-lookup"><span data-stu-id="517ac-144">Open the application with its window at its most recent size and position.</span></span> <span data-ttu-id="517ac-145">La finestra attiva rimane attiva.</span><span class="sxs-lookup"><span data-stu-id="517ac-145">The active window remains active.</span></span><br/>                                  |
| <dl> <span data-ttu-id="517ac-146"><dt></dt><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="517ac-146"><dt></dt> <dt>5</dt></span></span> </dl>  | <span data-ttu-id="517ac-147">Aprire l'applicazione con la relativa finestra in corrispondenza delle dimensioni e della posizione correnti.</span><span class="sxs-lookup"><span data-stu-id="517ac-147">Open the application with its window at its current size and position.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="517ac-148"><dt></dt><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="517ac-148"><dt></dt> <dt>7</dt></span></span> </dl>  | <span data-ttu-id="517ac-149">Aprire l'applicazione con una finestra ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="517ac-149">Open the application with a minimized window.</span></span> <span data-ttu-id="517ac-150">La finestra attiva rimane attiva.</span><span class="sxs-lookup"><span data-stu-id="517ac-150">The active window remains active.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="517ac-151"><dt></dt><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="517ac-151"><dt></dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="517ac-152">Aprire l'applicazione con la relativa finestra nello stato predefinito specificato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="517ac-152">Open the application with its window in the default state specified by the application.</span></span><br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="517ac-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="517ac-153">Remarks</span></span>

<span data-ttu-id="517ac-154">Questo metodo equivale a avviare uno dei comandi associati al menu di scelta rapida di un file.</span><span class="sxs-lookup"><span data-stu-id="517ac-154">This method is equivalent to launching one of the commands associated with a file's shortcut menu.</span></span> <span data-ttu-id="517ac-155">Ogni comando è rappresentato da una stringa verbo.</span><span class="sxs-lookup"><span data-stu-id="517ac-155">Each command is represented by a verb string.</span></span> <span data-ttu-id="517ac-156">Il set di verbi supportati varia da file a file.</span><span class="sxs-lookup"><span data-stu-id="517ac-156">The set of supported verbs varies from file to file.</span></span> <span data-ttu-id="517ac-157">Il verbo più comunemente supportato è "Open", che è in genere anche il verbo predefinito.</span><span class="sxs-lookup"><span data-stu-id="517ac-157">The most commonly supported verb is "open", which is also usually the default verb.</span></span> <span data-ttu-id="517ac-158">Altri verbi possono essere supportati solo da determinati tipi di file.</span><span class="sxs-lookup"><span data-stu-id="517ac-158">Other verbs might be supported by only certain types of files.</span></span> <span data-ttu-id="517ac-159">Per ulteriori informazioni sui verbi della shell, vedere [avvio di applicazioni](launch.md) o [estensione dei menu di scelta rapida](context.md).</span><span class="sxs-lookup"><span data-stu-id="517ac-159">For further discussion of Shell verbs, see [Launching Applications](launch.md) or [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="517ac-160">Questo metodo non è attualmente disponibile in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="517ac-160">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="517ac-161">Esempio</span><span class="sxs-lookup"><span data-stu-id="517ac-161">Examples</span></span>

<span data-ttu-id="517ac-162">Negli esempi seguenti viene illustrato l'utilizzo di **ShellExecute** per aprire il blocco note.</span><span class="sxs-lookup"><span data-stu-id="517ac-162">The following examples show the use of **ShellExecute** to open Notepad.</span></span> <span data-ttu-id="517ac-163">L'utilizzo viene visualizzato per JScript e VBScript.</span><span class="sxs-lookup"><span data-stu-id="517ac-163">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="517ac-164">JScript</span><span class="sxs-lookup"><span data-stu-id="517ac-164">JScript:</span></span>


```JScript
function ShellExecuteJS()
{
    var objShell = new ActiveXObject("Shell.Application");
    objShell.ShellExecute("notepad.exe", "", "", "open", 1);
}
```

<span data-ttu-id="517ac-165">VBScript</span><span class="sxs-lookup"><span data-stu-id="517ac-165">VBScript:</span></span>

```vb
Function ShellExecuteVB()
    Dim objShell
    Set objShell = CreateObject("Shell.Application")
    Call objShell.ShellExecute("notepad.exe", "", "", "open", 1)
End Function
```



## <a name="requirements"></a><span data-ttu-id="517ac-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="517ac-166">Requirements</span></span>



| <span data-ttu-id="517ac-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="517ac-167">Requirement</span></span> | <span data-ttu-id="517ac-168">Valore</span><span class="sxs-lookup"><span data-stu-id="517ac-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="517ac-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="517ac-169">Minimum supported client</span></span><br/> | <span data-ttu-id="517ac-170">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="517ac-170">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="517ac-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="517ac-171">Minimum supported server</span></span><br/> | <span data-ttu-id="517ac-172">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="517ac-172">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="517ac-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="517ac-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="517ac-174"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="517ac-174"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="517ac-175">IDL</span><span class="sxs-lookup"><span data-stu-id="517ac-175">IDL</span></span><br/>                      | <dl> <span data-ttu-id="517ac-176"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="517ac-176"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="517ac-177">DLL</span><span class="sxs-lookup"><span data-stu-id="517ac-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="517ac-178"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="517ac-178"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
