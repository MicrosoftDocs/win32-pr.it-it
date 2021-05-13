---
description: Converte un nome di accesso nell'ID di sicurezza utente corrispondente in formato stringa.
title: Metodo DiskQuotaControl.TranslateLogonNameToSID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.TranslateLogonNameToSID
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3b6b0d03-e9ef-4575-bb67-f7b7b39d2a16
ms.openlocfilehash: 5f0a2591b0f5df6bc0f50994fcbf101b7bfbb36d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841562"
---
# <a name="diskquotacontroltranslatelogonnametosid-method"></a><span data-ttu-id="b81d3-103">Metodo DiskQuotaControl.TranslateLogonNameToSID</span><span class="sxs-lookup"><span data-stu-id="b81d3-103">DiskQuotaControl.TranslateLogonNameToSID method</span></span>

<span data-ttu-id="b81d3-104">Converte un nome di accesso nell'ID di sicurezza utente corrispondente in formato stringa.</span><span class="sxs-lookup"><span data-stu-id="b81d3-104">Translates a logon name to the corresponding user security ID in string format.</span></span>

## <a name="syntax"></a><span data-ttu-id="b81d3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b81d3-105">Syntax</span></span>


```JScript
DiskQuotaControl.TranslateLogonNameToSID(
  logonname
)
```



## <a name="parameters"></a><span data-ttu-id="b81d3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b81d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b81d3-107">*logonname*</span><span class="sxs-lookup"><span data-stu-id="b81d3-107">*logonname*</span></span> 
</dt> <dd>

<span data-ttu-id="b81d3-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="b81d3-108">Type: **String**</span></span>

<span data-ttu-id="b81d3-109">Valore stringa che specifica il nome di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b81d3-109">A string value that specifies the user's logon name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b81d3-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b81d3-110">Return value</span></span>

<span data-ttu-id="b81d3-111">Restituisce l'ID di sicurezza utente (SID) in formato stringa corrispondente al nome di accesso specificato.</span><span class="sxs-lookup"><span data-stu-id="b81d3-111">Returns the user security ID (SID) in string format corresponding to the provided logon name.</span></span> <span data-ttu-id="b81d3-112">La stringa restituita include le parentesi graffe di inclusione standard.</span><span class="sxs-lookup"><span data-stu-id="b81d3-112">The returned string includes the standard enclosing braces.</span></span> <span data-ttu-id="b81d3-113">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="b81d3-113">For example:</span></span>

<span data-ttu-id="b81d3-114">"{S-1-5-21-2127521184-1604012920-1887927527-19009}"</span><span class="sxs-lookup"><span data-stu-id="b81d3-114">"{S-1-5-21-2127521184-1604012920-1887927527-19009}"</span></span>

## <a name="remarks"></a><span data-ttu-id="b81d3-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="b81d3-115">Remarks</span></span>

<span data-ttu-id="b81d3-116">La stringa SID restituita può essere passata al [**metodo FindUser**](diskquotacontrol-finduser.md) al posto di un nome di accesso.</span><span class="sxs-lookup"><span data-stu-id="b81d3-116">The returned SID string can be passed to the [**FindUser**](diskquotacontrol-finduser.md) method in place of a logon name.</span></span>

<span data-ttu-id="b81d3-117">Quando una chiamata al metodo [**FindUser**](diskquotacontrol-finduser.md)( *logonname*) ha esito negativo, potrebbe essere dovuta a una mancata corrispondenza tra il modulo (ad esempio, compatibile con SECURITY Account Manager SAM e l'UPN nome dell'entità utente ) del nome di accesso specificato e il modulo archiviato nella \[ cache \] \[ \] siD-name.</span><span class="sxs-lookup"><span data-stu-id="b81d3-117">When a call to the [**FindUser**](diskquotacontrol-finduser.md)( *logonname*) method fails, it could be due to a mismatch between the form (for example, Security Account Manager \[SAM\] compatible and User Principal Name \[UPN\]) of the logon name provided and the form stored in the SID-name cache.</span></span> <span data-ttu-id="b81d3-118">In questi casi, il nome di accesso può essere convertito in un SID e la chiamata a **FindUser ripetuta.**</span><span class="sxs-lookup"><span data-stu-id="b81d3-118">In such cases, the logon name can be converted to a SID and the call to **FindUser** repeated.</span></span> <span data-ttu-id="b81d3-119">**FindUser** riconosce una stringa SID e ignora la ricerca nella cache dei nomi SID.</span><span class="sxs-lookup"><span data-stu-id="b81d3-119">**FindUser** recognizes a SID string and will bypass the SID-name cache lookup.</span></span> <span data-ttu-id="b81d3-120">Il codice Microsoft Visual Basic Scripting Edition (VBScript) seguente illustra questa tecnica.</span><span class="sxs-lookup"><span data-stu-id="b81d3-120">The following Microsoft Visual Basic Scripting Edition (VBScript) code illustrates this technique.</span></span>


```
Function Find(dqc, name)
    On Error Resume Next
    SET Find = dqc.FindUser(name)

    If Err.Number <> 0 Then
        Err.Clear
        SET Find = dqc.FindUser(dqc.TranslateLogonNameToSID(name))
    End If    

End Function
```



<span data-ttu-id="b81d3-121">La conversione da nome a SID può essere un processo lento rispetto alle ricerche nella cache dei nomi SID.</span><span class="sxs-lookup"><span data-stu-id="b81d3-121">Name-to-SID translation can be a slow process when compared to lookups in the SID-name cache.</span></span> <span data-ttu-id="b81d3-122">Pertanto, è consigliabile chiamare [**prima FindUser**](diskquotacontrol-finduser.md) con un nome di accesso.</span><span class="sxs-lookup"><span data-stu-id="b81d3-122">Therefore, it is recommended that [**FindUser**](diskquotacontrol-finduser.md) first be called with a logon name.</span></span> <span data-ttu-id="b81d3-123">L'esempio precedente usa questa tecnica.</span><span class="sxs-lookup"><span data-stu-id="b81d3-123">The example above uses this technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="b81d3-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b81d3-124">Requirements</span></span>



| <span data-ttu-id="b81d3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b81d3-125">Requirement</span></span> | <span data-ttu-id="b81d3-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b81d3-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b81d3-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b81d3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b81d3-128">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b81d3-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b81d3-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b81d3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b81d3-130">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b81d3-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b81d3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b81d3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b81d3-132"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="b81d3-132"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b81d3-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b81d3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b81d3-134">**Oggetto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="b81d3-134">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




