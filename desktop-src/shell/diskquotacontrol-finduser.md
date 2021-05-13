---
description: Trova la voce di un utente, in base al nome, nel file di quota del volume.
title: Metodo DiskQuotaControl.FindUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.FindUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e5767d28-4c0a-49bc-a1d3-ba809411456d
ms.openlocfilehash: eab539a5ec5a360ae28fc87d5ffbb9dd4f9f1cc8
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841522"
---
# <a name="diskquotacontrolfinduser-method"></a><span data-ttu-id="7c22e-103">Metodo DiskQuotaControl.FindUser</span><span class="sxs-lookup"><span data-stu-id="7c22e-103">DiskQuotaControl.FindUser method</span></span>

<span data-ttu-id="7c22e-104">Trova la voce di un utente, in base al nome, nel file di quota del volume.</span><span class="sxs-lookup"><span data-stu-id="7c22e-104">Finds a user's entry, by name, in the volume's quota file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c22e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c22e-105">Syntax</span></span>


```JScript
DiskQuotaControl.FindUser(
  sLogonName
)
```



## <a name="parameters"></a><span data-ttu-id="7c22e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c22e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c22e-107">*sLogonName*</span><span class="sxs-lookup"><span data-stu-id="7c22e-107">*sLogonName*</span></span> 
</dt> <dd>

<span data-ttu-id="7c22e-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="7c22e-108">Type: **String**</span></span>

<span data-ttu-id="7c22e-109">Valore stringa che contiene il nome di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7c22e-109">A string value that contains the user's logon name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c22e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c22e-110">Return value</span></span>

<span data-ttu-id="7c22e-111">Restituisce un'espressione di oggetto che restituisce l'oggetto [**DIDiskQuotaUser dell'utente.**](didiskquotauser-object.md)</span><span class="sxs-lookup"><span data-stu-id="7c22e-111">Returns an object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c22e-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c22e-112">Remarks</span></span>

<span data-ttu-id="7c22e-113">Questo metodo restituisce un [**oggetto DIDiskQuotaUser**](didiskquotauser-object.md) anche se non è presente alcuna voce per l'utente nel file di quota.</span><span class="sxs-lookup"><span data-stu-id="7c22e-113">This method returns a [**DIDiskQuotaUser**](didiskquotauser-object.md) object even if there is no entry for the user in the quota file.</span></span> <span data-ttu-id="7c22e-114">L'oggetto utente restituito ha una soglia di avviso e limiti di quota rigida impostati su valori predefiniti del volume.</span><span class="sxs-lookup"><span data-stu-id="7c22e-114">The returned user object has warning threshold and hard quota limits set to the volume's default values.</span></span>

<span data-ttu-id="7c22e-115">La stringa restituita [**da TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) può essere passata al posto del *parametro sLogonName.*</span><span class="sxs-lookup"><span data-stu-id="7c22e-115">The string returned from [**TranslateLogonNameToSID**](diskquotacontrol-translatelogonnametosid.md) may be passed in place of the *sLogonName* parameter.</span></span> <span data-ttu-id="7c22e-116">Quando **FindUser** riceve una stringa SID, usa il SID corrispondente per la ricerca diretta del record di quota dell'utente nel volume.</span><span class="sxs-lookup"><span data-stu-id="7c22e-116">When **FindUser** receives a SID string it uses the corresponding SID for direct lookup of the user's quota record on the volume.</span></span> <span data-ttu-id="7c22e-117">In questo modo viene ignorata la cache dei nomi SID.</span><span class="sxs-lookup"><span data-stu-id="7c22e-117">This bypasses the SID-name cache.</span></span> <span data-ttu-id="7c22e-118">Nei casi in cui **FindUser** ha esito negativo a causa di una mancata corrispondenza nel formato (ad esempio, compatibile con SAM e UPN) del nome di accesso specificato e del nome di accesso memorizzato nella cache, il nome di accesso può essere convertito in una stringa SID usando **TranslateLogonNameToSID** e quindi passato nuovamente a **FindUser**.</span><span class="sxs-lookup"><span data-stu-id="7c22e-118">In cases where **FindUser** fails due to a mismatch in format (for example, SAM-compatible and UPN) of the logon name provided and the logon name cached, the logon name can be translated to a SID string using **TranslateLogonNameToSID** then passed again to **FindUser**.</span></span> <span data-ttu-id="7c22e-119">Il codice VBScript seguente illustra questa tecnica.</span><span class="sxs-lookup"><span data-stu-id="7c22e-119">The following VBScript code illustrates this technique.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="7c22e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c22e-120">Requirements</span></span>



| <span data-ttu-id="7c22e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c22e-121">Requirement</span></span> | <span data-ttu-id="7c22e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7c22e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c22e-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c22e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7c22e-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7c22e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7c22e-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c22e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7c22e-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7c22e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7c22e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7c22e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c22e-128"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="7c22e-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c22e-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c22e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c22e-130">**Oggetto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="7c22e-130">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




