---
description: Elimina un nome di condivisione dall'elenco di risorse condivise di un server, disconnettendo le connessioni alla risorsa condivisa.
ms.assetid: 175f9c0e-0017-4a86-8e05-ad78e2c93c11
ms.tgt_platform: multiple
title: Metodo Delete della classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2048ba9dac91b139888f27c037d64849de8a4ee8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126922"
---
# <a name="delete-method-of-the-win32_share-class"></a><span data-ttu-id="2da5a-103">Metodo Delete della \_ classe Share Win32</span><span class="sxs-lookup"><span data-stu-id="2da5a-103">Delete method of the Win32\_Share class</span></span>

<span data-ttu-id="2da5a-104">Il metodo **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) Elimina un nome di condivisione dall'elenco di risorse condivise di un server, disconnettendo le connessioni alla risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="2da5a-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes a share name from a server's list of shared resources, disconnecting connections to the shared resource.</span></span>

<span data-ttu-id="2da5a-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="2da5a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2da5a-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2da5a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2da5a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2da5a-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="2da5a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2da5a-108">Parameters</span></span>

<span data-ttu-id="2da5a-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2da5a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2da5a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2da5a-110">Return value</span></span>

<span data-ttu-id="2da5a-111">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="2da5a-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="2da5a-112">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2da5a-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2da5a-113">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2da5a-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2da5a-114">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="2da5a-114">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2da5a-115">**Accesso negato** (2)</span><span class="sxs-lookup"><span data-stu-id="2da5a-115">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2da5a-116">**Errore sconosciuto** (8)</span><span class="sxs-lookup"><span data-stu-id="2da5a-116">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2da5a-117">**Nome non valido** (9)</span><span class="sxs-lookup"><span data-stu-id="2da5a-117">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2da5a-118">**Livello non valido** (10)</span><span class="sxs-lookup"><span data-stu-id="2da5a-118">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2da5a-119">**Parametro non valido** (21)</span><span class="sxs-lookup"><span data-stu-id="2da5a-119">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="2da5a-120">**Condivisione duplicata** (22)</span><span class="sxs-lookup"><span data-stu-id="2da5a-120">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="2da5a-121">**Percorso reindirizzato** (23)</span><span class="sxs-lookup"><span data-stu-id="2da5a-121">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="2da5a-122">**Dispositivo o directory sconosciuta** (24)</span><span class="sxs-lookup"><span data-stu-id="2da5a-122">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="2da5a-123">**Nome NET non trovato** (25)</span><span class="sxs-lookup"><span data-stu-id="2da5a-123">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="2da5a-124">**Altro** (26 4294967295)</span><span class="sxs-lookup"><span data-stu-id="2da5a-124">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="2da5a-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="2da5a-125">Remarks</span></span>

<span data-ttu-id="2da5a-126">Il metodo **Delete** è un metodo oggetto e viene utilizzato in un'istanza di una classe.</span><span class="sxs-lookup"><span data-stu-id="2da5a-126">The **Delete** method is an object method and is used on an instance of a class.</span></span>

<span data-ttu-id="2da5a-127">Per eseguire correttamente il metodo, solo i membri del gruppo locale Administrators o account Operators o quelli con appartenenza a gruppi di operatori di comunicazione, stampa o server possono eseguire correttamente il metodo.</span><span class="sxs-lookup"><span data-stu-id="2da5a-127">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute the method.</span></span> <span data-ttu-id="2da5a-128">L'operatore Print può eliminare solo le code di stampa.</span><span class="sxs-lookup"><span data-stu-id="2da5a-128">The Print operator can delete only printer queues.</span></span> <span data-ttu-id="2da5a-129">L'operatore di comunicazione può eliminare solo le code del dispositivo di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="2da5a-129">The Communication operator can delete only communication-device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="2da5a-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="2da5a-130">Examples</span></span>

<span data-ttu-id="2da5a-131">Nell'esempio di codice VBScript seguente viene eliminata la condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="2da5a-131">The following VBScript code sample deletes the specified share.</span></span>


```VB
On Error Resume Next

ComputerName = InputBox("Enter the computer name:", "Delete Share", "localhost")

SName = InputBox("Enter the name of the share:", "Delete Share")



Set Shares = GetObject("winmgmts:\\" & ComputerName & _
 "\root\cimv2").ExecQuery("SELECT * FROM Win32_Share WHERE name = '" & SName & "'")



For Each Share in Shares
 Share.Delete()
Next
```



<span data-ttu-id="2da5a-132">L'esempio di codice PowerShell seguente elimina le condivisioni vuote.</span><span class="sxs-lookup"><span data-stu-id="2da5a-132">The following PowerShell code sample deletes blank shares.</span></span>


```PowerShell
$Shares = Get-WMIObject Win32_Share | Where {$_.Name -eq ""}

Foreach ($Share in $Shares) {
   $Share.Delete()
}
"{0} blank shares found and removed" -f $shares.count
```



## <a name="requirements"></a><span data-ttu-id="2da5a-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2da5a-133">Requirements</span></span>



| <span data-ttu-id="2da5a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2da5a-134">Requirement</span></span> | <span data-ttu-id="2da5a-135">Valore</span><span class="sxs-lookup"><span data-stu-id="2da5a-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2da5a-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2da5a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2da5a-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2da5a-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2da5a-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2da5a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2da5a-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2da5a-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2da5a-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2da5a-140">Namespace</span></span><br/>                | <span data-ttu-id="2da5a-141">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="2da5a-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2da5a-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2da5a-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2da5a-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2da5a-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2da5a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2da5a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2da5a-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2da5a-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2da5a-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2da5a-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="2da5a-147">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2da5a-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2da5a-148">**\_Condivisione Win32**</span><span class="sxs-lookup"><span data-stu-id="2da5a-148">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

