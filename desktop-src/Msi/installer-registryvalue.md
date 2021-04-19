---
description: Il metodo RegistryValue dell'oggetto Installer legge le informazioni relative a una chiave del registro di sistema specificata.
ms.assetid: 63c258f9-8649-419d-9f79-3681f9f97302
title: Installer. RegistryValue, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RegistryValue
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6da79ff08eebe62ad177119a35bfc29b21c9350
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329126"
---
# <a name="installerregistryvalue-method"></a><span data-ttu-id="95dec-103">Installer. RegistryValue, metodo</span><span class="sxs-lookup"><span data-stu-id="95dec-103">Installer.RegistryValue method</span></span>

<span data-ttu-id="95dec-104">Il metodo **RegistryValue** dell'oggetto [**Installer**](installer-object.md) legge le informazioni relative a una chiave del registro di sistema specificata.</span><span class="sxs-lookup"><span data-stu-id="95dec-104">The **RegistryValue** method of the [**Installer**](installer-object.md) object reads information about a specified registry key of value.</span></span> <span data-ttu-id="95dec-105">Se la chiave o il valore specificato non esiste, il metodo restituisce un errore pari a 9, ovvero "indice non compreso nell'intervallo".</span><span class="sxs-lookup"><span data-stu-id="95dec-105">If the key or value specified does not exist, the method returns an error of 9, "Subscript out of Range."</span></span>

## <a name="syntax"></a><span data-ttu-id="95dec-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95dec-106">Syntax</span></span>


```JScript
Installer.RegistryValue(
  root,
  key,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="95dec-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="95dec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95dec-108">*radice*</span><span class="sxs-lookup"><span data-stu-id="95dec-108">*root*</span></span> 
</dt> <dd>

<span data-ttu-id="95dec-109">In Windows NT 4,0 la radice del registro di sistema è una chiave radice numerica o un nome di computer sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="95dec-109">In Windows NT 4.0, the registry root is either a numeric root key or a machine name as a string.</span></span> <span data-ttu-id="95dec-110">I nomi dei computer sono sempre stringhe.</span><span class="sxs-lookup"><span data-stu-id="95dec-110">Machine names are always strings.</span></span> <span data-ttu-id="95dec-111">In Windows 95, Windows 98 o Windows me, la radice del registro di sistema è solo una chiave radice numerica.</span><span class="sxs-lookup"><span data-stu-id="95dec-111">In Windows 95, Windows 98, or Windows Me, the registry root is a numeric root key only.</span></span> <span data-ttu-id="95dec-112">È possibile accedere a HKLM solo in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="95dec-112">You can only access HKLM on a remote machine.</span></span>



| <span data-ttu-id="95dec-113">Radice</span><span class="sxs-lookup"><span data-stu-id="95dec-113">Root</span></span>                                                                                                                                                                                   | <span data-ttu-id="95dec-114">Significato</span><span class="sxs-lookup"><span data-stu-id="95dec-114">Meaning</span></span>      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span id="HKEY_CLASSES_ROOT"></span><span id="hkey_classes_root"></span><dl> <span data-ttu-id="95dec-115"><dt>**\_radice delle classi HKEY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="95dec-115"><dt>**HKEY\_CLASSES\_ROOT**</dt></span></span> </dl>             | <span data-ttu-id="95dec-116">0</span><span class="sxs-lookup"><span data-stu-id="95dec-116">0</span></span><br/> |
| <span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dl> <span data-ttu-id="95dec-117"><dt>**HKEY \_ \_ utente corrente**</dt></span><span class="sxs-lookup"><span data-stu-id="95dec-117"><dt>**HKEY\_CURRENT\_USER**</dt></span></span> </dl>             | <span data-ttu-id="95dec-118">1</span><span class="sxs-lookup"><span data-stu-id="95dec-118">1</span></span><br/> |
| <span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dl> <span data-ttu-id="95dec-119"><dt>**\_computer locale \_ HKEY**</dt></span><span class="sxs-lookup"><span data-stu-id="95dec-119"><dt>**HKEY\_LOCAL\_MACHINE**</dt></span></span> </dl>          | <span data-ttu-id="95dec-120">2</span><span class="sxs-lookup"><span data-stu-id="95dec-120">2</span></span><br/> |
| <span id="HKEY_USERS"></span><span id="hkey_users"></span><dl> <span data-ttu-id="95dec-121"><dt>**\_utenti HKEY**</dt></span><span class="sxs-lookup"><span data-stu-id="95dec-121"><dt>**HKEY\_USERS**</dt></span></span> </dl>                                   | <span data-ttu-id="95dec-122">3</span><span class="sxs-lookup"><span data-stu-id="95dec-122">3</span></span><br/> |
| <span id="HKEY_PERFORMANCE_DATA"></span><span id="hkey_performance_data"></span><dl> <span data-ttu-id="95dec-123"><dt>**\_dati sulle prestazioni di HKEY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="95dec-123"><dt>**HKEY\_PERFORMANCE\_DATA**</dt></span></span> </dl> | <span data-ttu-id="95dec-124">4</span><span class="sxs-lookup"><span data-stu-id="95dec-124">4</span></span><br/> |
| <span id="HKEY_CURRENT_CONFIG"></span><span id="hkey_current_config"></span><dl> <span data-ttu-id="95dec-125"><dt>**HKEY \_ \_ configurazione corrente**</dt></span><span class="sxs-lookup"><span data-stu-id="95dec-125"><dt>**HKEY\_CURRENT\_CONFIG**</dt></span></span> </dl>       | <span data-ttu-id="95dec-126">5</span><span class="sxs-lookup"><span data-stu-id="95dec-126">5</span></span><br/> |
| <span id="HKEY_DYN_DATA"></span><span id="hkey_dyn_data"></span><dl> <span data-ttu-id="95dec-127"><dt>**\_dati dyn di HKEY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="95dec-127"><dt>**HKEY\_DYN\_DATA**</dt></span></span> </dl>                         | <span data-ttu-id="95dec-128">6</span><span class="sxs-lookup"><span data-stu-id="95dec-128">6</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="95dec-129">*key*</span><span class="sxs-lookup"><span data-stu-id="95dec-129">*key*</span></span> 
</dt> <dd>

<span data-ttu-id="95dec-130">Stringa che contiene il percorso completo della chiave dalla radice.</span><span class="sxs-lookup"><span data-stu-id="95dec-130">A string containing the complete key path from the root.</span></span>

</dd> <dt>

<span data-ttu-id="95dec-131">*value*</span><span class="sxs-lookup"><span data-stu-id="95dec-131">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="95dec-132">Questo parametro facoltativo designa quale valore associato restituire per la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="95dec-132">This optional parameter designates which associated value to return for the specified key.</span></span> <span data-ttu-id="95dec-133">Il valore è uno dei valori mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="95dec-133">The value is one of the values shown in the following table.</span></span>



| <span data-ttu-id="95dec-134">Valore</span><span class="sxs-lookup"><span data-stu-id="95dec-134">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="95dec-135">Significato</span><span class="sxs-lookup"><span data-stu-id="95dec-135">Meaning</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Missing_or_blank"></span><span id="missing_or_blank"></span><span id="MISSING_OR_BLANK"></span><dl> <span data-ttu-id="95dec-136"><dt>**Mancante o vuoto**</dt></span><span class="sxs-lookup"><span data-stu-id="95dec-136"><dt>**Missing or blank**</dt></span></span> </dl> | <span data-ttu-id="95dec-137">Restituisce un valore booleano che indica se la chiave esiste.</span><span class="sxs-lookup"><span data-stu-id="95dec-137">Returns a Boolean designating whether the key exists.</span></span><br/>                                                                                        |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <span data-ttu-id="95dec-138"><dt>**Stringa**</dt></span><span class="sxs-lookup"><span data-stu-id="95dec-138"><dt>**String**</dt></span></span> </dl>                                         | <span data-ttu-id="95dec-139">Restituisce i dati associati al valore denominato, ha esito negativo se il nome del valore non esiste.</span><span class="sxs-lookup"><span data-stu-id="95dec-139">Returns the data associated with the named value, fails if the value name is non-existent.</span></span><br/>                                                   |
| <span id="Positive_integer"></span><span id="positive_integer"></span><span id="POSITIVE_INTEGER"></span><dl> <span data-ttu-id="95dec-140"><dt>**Intero positivo**</dt></span><span class="sxs-lookup"><span data-stu-id="95dec-140"><dt>**Positive integer**</dt></span></span> </dl> | <span data-ttu-id="95dec-141">Restituisce il nome del valore enumerato in base 1, ma è vuoto se non esiste.</span><span class="sxs-lookup"><span data-stu-id="95dec-141">Returns the 1-based enumerated value name, it is empty if non-existent.</span></span> <span data-ttu-id="95dec-142">Questa opzione Usa la funzione [**RegEnumValue**](/windows/win32/api/winreg/nf-winreg-regenumvaluea) .</span><span class="sxs-lookup"><span data-stu-id="95dec-142">This option uses the [**RegEnumValue**](/windows/win32/api/winreg/nf-winreg-regenumvaluea) function.</span></span><br/> |
| <span id="Negative_integer"></span><span id="negative_integer"></span><span id="NEGATIVE_INTEGER"></span><dl> <span data-ttu-id="95dec-143"><dt>**Numero intero negativo**</dt></span><span class="sxs-lookup"><span data-stu-id="95dec-143"><dt>**Negative integer**</dt></span></span> </dl> | <span data-ttu-id="95dec-144">Restituisce il nome della sottochiave enumerata in base 1, che è vuoto se non esiste.</span><span class="sxs-lookup"><span data-stu-id="95dec-144">Returns the 1-based enumerated subkey name, this is empty if non-existent.</span></span> <span data-ttu-id="95dec-145">Questa opzione Usa la funzione [**RegEnumKey**](/windows/win32/api/winreg/nf-winreg-regenumkeya) .</span><span class="sxs-lookup"><span data-stu-id="95dec-145">This option uses the [**RegEnumKey**](/windows/win32/api/winreg/nf-winreg-regenumkeya) function.</span></span><br/>  |
| <span id="Zero_integer"></span><span id="zero_integer"></span><span id="ZERO_INTEGER"></span><dl> <span data-ttu-id="95dec-146"><dt>**Intero zero**</dt></span><span class="sxs-lookup"><span data-stu-id="95dec-146"><dt>**Zero integer**</dt></span></span> </dl>                 | <span data-ttu-id="95dec-147">Restituisce il nome della classe stringa per la chiave designata.</span><span class="sxs-lookup"><span data-stu-id="95dec-147">Returns the string class name for the designated key.</span></span><br/>                                                                                        |
| <span id="Empty_string____"></span><span id="empty_string____"></span><span id="EMPTY_STRING____"></span><dl> <span data-ttu-id="95dec-148"><dt>**Stringa vuota ""**</dt></span><span class="sxs-lookup"><span data-stu-id="95dec-148"><dt>**Empty string " "**</dt></span></span> </dl> | <span data-ttu-id="95dec-149">Restituisce il valore predefinito della chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="95dec-149">Returns the default value of the registry key.</span></span><br/>                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95dec-150">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95dec-150">Return value</span></span>

<span data-ttu-id="95dec-151">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="95dec-151">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="95dec-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95dec-152">Requirements</span></span>



| <span data-ttu-id="95dec-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="95dec-153">Requirement</span></span> | <span data-ttu-id="95dec-154">Valore</span><span class="sxs-lookup"><span data-stu-id="95dec-154">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95dec-155">Versione</span><span class="sxs-lookup"><span data-stu-id="95dec-155">Version</span></span><br/> | <span data-ttu-id="95dec-156">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="95dec-156">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="95dec-157">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="95dec-157">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="95dec-158">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="95dec-158">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="95dec-159">DLL</span><span class="sxs-lookup"><span data-stu-id="95dec-159">DLL</span></span><br/>     | <dl> <span data-ttu-id="95dec-160"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95dec-160"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="95dec-161">IID</span><span class="sxs-lookup"><span data-stu-id="95dec-161">IID</span></span><br/>     | <span data-ttu-id="95dec-162">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="95dec-162">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 
