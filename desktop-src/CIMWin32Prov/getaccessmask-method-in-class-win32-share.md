---
description: "Metodo GetAccessMask della classe Win32_Share: restituisce una bitmap uint32 con i diritti di accesso alla condivisione mantenuta dall'utente o dal gruppo per conto del quale viene restituita l'istanza."
ms.assetid: 234f44a4-ffff-431d-a973-98f2bd313c7d
ms.tgt_platform: multiple
title: Metodo GetAccessMask della Win32_Share classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.GetAccessMask
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fcd6396f6421060a67108e7c428c99bcd7ca9651
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097019"
---
# <a name="getaccessmask-method-of-the-win32_share-class"></a><span data-ttu-id="adba1-103">Metodo GetAccessMask della classe Win32 \_ Share</span><span class="sxs-lookup"><span data-stu-id="adba1-103">GetAccessMask method of the Win32\_Share class</span></span>

<span data-ttu-id="adba1-104">Il **metodo GetAccessMask** restituisce una bitmap uint32 con i diritti di accesso alla condivisione mantenuta dall'utente o dal gruppo per conto del quale viene restituita l'istanza.</span><span class="sxs-lookup"><span data-stu-id="adba1-104">The **GetAccessMask** method returns a uint32 bitmap with the access rights to the share held by the user or group on whose behalf the instance is returned.</span></span>

<span data-ttu-id="adba1-105">Questo argomento usa Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="adba1-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="adba1-106">Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="adba1-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="adba1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="adba1-107">Syntax</span></span>


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a><span data-ttu-id="adba1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="adba1-108">Parameters</span></span>

<span data-ttu-id="adba1-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="adba1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="adba1-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="adba1-110">Return value</span></span>

<span data-ttu-id="adba1-111">Diritti di accesso alla condivisione mantenuta dall'utente o dal gruppo.</span><span class="sxs-lookup"><span data-stu-id="adba1-111">Access rights to the share held by the user or group.</span></span>

<dl> <dt>

<span data-ttu-id="adba1-112">**DIRECTORY \_ ELENCO \_ FILE**</span><span class="sxs-lookup"><span data-stu-id="adba1-112">**FILE\_LIST\_DIRECTORY**</span></span>
</dt> <dd>

<span data-ttu-id="adba1-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="adba1-113">1 (0x1)</span></span>

<span data-ttu-id="adba1-114">Concede il diritto di leggere i dati dal file.</span><span class="sxs-lookup"><span data-stu-id="adba1-114">Grants the right to read data from the file.</span></span> <span data-ttu-id="adba1-115">Per una directory, questo valore concede il diritto di elencare il contenuto della directory.</span><span class="sxs-lookup"><span data-stu-id="adba1-115">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span data-ttu-id="adba1-116">**FILE \_ ADD \_ FILE**</span><span class="sxs-lookup"><span data-stu-id="adba1-116">**FILE\_ADD\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="adba1-117">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="adba1-117">2 (0x2)</span></span>

<span data-ttu-id="adba1-118">Concede il diritto di scrivere dati nel file.</span><span class="sxs-lookup"><span data-stu-id="adba1-118">Grants the right to write data to the file.</span></span> <span data-ttu-id="adba1-119">Per una directory, questo valore concede il diritto di creare un file nella directory.</span><span class="sxs-lookup"><span data-stu-id="adba1-119">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span data-ttu-id="adba1-120">**FILE \_ ADD \_ SUBDIRECTORY**</span><span class="sxs-lookup"><span data-stu-id="adba1-120">**FILE\_ADD\_SUBDIRECTORY**</span></span>
</dt> <dd>

<span data-ttu-id="adba1-121">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="adba1-121">4 (0x4)</span></span>

<span data-ttu-id="adba1-122">Concede il diritto di aggiungere dati al file.</span><span class="sxs-lookup"><span data-stu-id="adba1-122">Grants the right to append data to the file.</span></span> <span data-ttu-id="adba1-123">Per una directory, questo valore concede il diritto di creare una sottodirectory.</span><span class="sxs-lookup"><span data-stu-id="adba1-123">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="adba1-124">**FILE \_ READ \_ EA**</span><span class="sxs-lookup"><span data-stu-id="adba1-124">**FILE\_READ\_EA**</span></span>
</dt> <dd>

<span data-ttu-id="adba1-125">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="adba1-125">8 (0x8)</span></span>

<span data-ttu-id="adba1-126">Concede il diritto di leggere gli attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="adba1-126">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span data-ttu-id="adba1-127">**FILE \_ WRITE \_ EA**</span><span class="sxs-lookup"><span data-stu-id="adba1-127">**FILE\_WRITE\_EA**</span></span>
</dt> <dd>

<span data-ttu-id="adba1-128">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="adba1-128">16 (0x10)</span></span>

<span data-ttu-id="adba1-129">Concede il diritto di scrivere attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="adba1-129">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span data-ttu-id="adba1-130">**ATTRAVERSAMENTO \_ FILE**</span><span class="sxs-lookup"><span data-stu-id="adba1-130">**FILE\_TRAVERSE**</span></span>
</dt> <dd>

<span data-ttu-id="adba1-131">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="adba1-131">32 (0x20)</span></span>

<span data-ttu-id="adba1-132">Concede il diritto di eseguire un file.</span><span class="sxs-lookup"><span data-stu-id="adba1-132">Grants the right to execute a file.</span></span> <span data-ttu-id="adba1-133">Per una directory, la directory può essere attraversata.</span><span class="sxs-lookup"><span data-stu-id="adba1-133">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span data-ttu-id="adba1-134">**FILE \_ DELETE \_ CHILD**</span><span class="sxs-lookup"><span data-stu-id="adba1-134">**FILE\_DELETE\_CHILD**</span></span>
</dt> <dd>

<span data-ttu-id="adba1-135">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="adba1-135">64 (0x40)</span></span>

<span data-ttu-id="adba1-136">Concede il diritto di eliminare una directory e tutti i file che contiene (i relativi elementi figlio), anche se i file sono di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="adba1-136">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span data-ttu-id="adba1-137">**ATTRIBUTI \_ DI LETTURA \_ FILE**</span><span class="sxs-lookup"><span data-stu-id="adba1-137">**FILE\_READ\_ATTRIBUTES**</span></span>
</dt> <dd>

<span data-ttu-id="adba1-138">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="adba1-138">128 (0x80)</span></span>

<span data-ttu-id="adba1-139">Concede il diritto di leggere gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="adba1-139">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span data-ttu-id="adba1-140">**ATTRIBUTI \_ DI SCRITTURA \_ FILE**</span><span class="sxs-lookup"><span data-stu-id="adba1-140">**FILE\_WRITE\_ATTRIBUTES**</span></span>
</dt> <dd>

<span data-ttu-id="adba1-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="adba1-141">256 (0x100)</span></span>

<span data-ttu-id="adba1-142">Concede il diritto di modificare gli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="adba1-142">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span data-ttu-id="adba1-143">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="adba1-143">**DELETE**</span></span>
</dt> <dd>

<span data-ttu-id="adba1-144">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="adba1-144">65536 (0x10000)</span></span>

<span data-ttu-id="adba1-145">Concede l'accesso per l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="adba1-145">Grants delete access.</span></span>

</dd> <dt>

<span data-ttu-id="adba1-146">**CONTROLLO \_ LETTURA**</span><span class="sxs-lookup"><span data-stu-id="adba1-146">**READ\_CONTROL**</span></span>
</dt> <dd>

<span data-ttu-id="adba1-147">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="adba1-147">131072 (0x20000)</span></span>

<span data-ttu-id="adba1-148">Concede l'accesso in lettura al descrittore di sicurezza e al proprietario.</span><span class="sxs-lookup"><span data-stu-id="adba1-148">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span data-ttu-id="adba1-149">**APPLICAZIONE \_ LIVELLO DATI WRITE**</span><span class="sxs-lookup"><span data-stu-id="adba1-149">**WRITE\_DAC**</span></span>
</dt> <dd>

<span data-ttu-id="adba1-150">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="adba1-150">262144 (0x40000)</span></span>

<span data-ttu-id="adba1-151">Concede l'accesso in scrittura all'elenco di controllo di accesso discrezionale (DACL).</span><span class="sxs-lookup"><span data-stu-id="adba1-151">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span data-ttu-id="adba1-152">**WRITE \_ OWNER**</span><span class="sxs-lookup"><span data-stu-id="adba1-152">**WRITE\_OWNER**</span></span>
</dt> <dd>

<span data-ttu-id="adba1-153">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="adba1-153">524288 (0x80000)</span></span>

<span data-ttu-id="adba1-154">Assegna il proprietario della scrittura.</span><span class="sxs-lookup"><span data-stu-id="adba1-154">Assigns the write owner.</span></span>

</dd> <dt>

<span data-ttu-id="adba1-155">**Sincronizzare**</span><span class="sxs-lookup"><span data-stu-id="adba1-155">**SYNCHRONIZE**</span></span>
</dt> <dd>

<span data-ttu-id="adba1-156">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="adba1-156">1048576 (0x100000)</span></span>

<span data-ttu-id="adba1-157">Sincronizza l'accesso e consente a un processo di attendere che un oggetto entri nello stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="adba1-157">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="adba1-158">Commenti</span><span class="sxs-lookup"><span data-stu-id="adba1-158">Remarks</span></span>

<span data-ttu-id="adba1-159">**Il metodo GetAccessMask** è un metodo oggetto e viene usato in un'occorrenza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="adba1-159">**GetAccessMask** method is an object method and is used on an occurrence of this class.</span></span>

## <a name="examples"></a><span data-ttu-id="adba1-160">Esempio</span><span class="sxs-lookup"><span data-stu-id="adba1-160">Examples</span></span>

<span data-ttu-id="adba1-161">L'esempio di codice VBScript seguente crea una cartella di condivisione e quindi ottiene il valore della maschera di accesso nel descrittore di sicurezza che protegge la cartella di condivisione.</span><span class="sxs-lookup"><span data-stu-id="adba1-161">The following VBScript code example creates a share folder and then gets the value of the access mask in the security descriptor that secures the share folder.</span></span>


```VB
Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 4000 
strComputer = "."

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objNewShare = objWMIService.Get("Win32_Share")
Return = objNewShare.Create ("C:\Temp", "TestShare", FILE_SHARE, MAXIMUM_CONNECTIONS, "test share")

If Return <> 0 Then
          WScript.Echo Return
          WScript.Quit
End If

Set objShare = objWMIService.Get("Win32_Share.Name='TestShare'")
Return = objShare.GetAccessMask
WScript.Echo Return
```



## <a name="requirements"></a><span data-ttu-id="adba1-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="adba1-162">Requirements</span></span>



| <span data-ttu-id="adba1-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="adba1-163">Requirement</span></span> | <span data-ttu-id="adba1-164">Valore</span><span class="sxs-lookup"><span data-stu-id="adba1-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="adba1-165">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="adba1-165">Minimum supported client</span></span><br/> | <span data-ttu-id="adba1-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="adba1-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="adba1-167">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="adba1-167">Minimum supported server</span></span><br/> | <span data-ttu-id="adba1-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="adba1-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="adba1-169">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="adba1-169">Namespace</span></span><br/>                | <span data-ttu-id="adba1-170">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="adba1-170">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="adba1-171">MOF</span><span class="sxs-lookup"><span data-stu-id="adba1-171">MOF</span></span><br/>                      | <dl> <span data-ttu-id="adba1-172"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="adba1-172"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="adba1-173">DLL</span><span class="sxs-lookup"><span data-stu-id="adba1-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adba1-174"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adba1-174"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adba1-175">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="adba1-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adba1-176">**Condivisione \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="adba1-176">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

