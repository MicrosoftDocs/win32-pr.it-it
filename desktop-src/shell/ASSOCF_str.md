---
description: Fornisce informazioni ai metodi dell'interfaccia IQueryAssociations.
ms.assetid: e67d0282-9090-43e6-aedf-bb1fc0443221
title: Enumerazione ASSOCF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70ddb0b4fb89925c643eb01c276772b9a7151578
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234549"
---
# <a name="assocf-enumeration"></a><span data-ttu-id="e3cd4-103">Enumerazione ASSOCF</span><span class="sxs-lookup"><span data-stu-id="e3cd4-103">ASSOCF enumeration</span></span>

<span data-ttu-id="e3cd4-104">Fornisce informazioni ai metodi dell'interfaccia [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .</span><span class="sxs-lookup"><span data-stu-id="e3cd4-104">Provides information to the [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3cd4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3cd4-105">Syntax</span></span>

<span codelanguage="ManagedCPlusPlus"></span>

<table><colgroup><col style="width: 100%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="e3cd4-106">C++</span><span class="sxs-lookup"><span data-stu-id="e3cd4-106">C++</span></span></th></tr></thead><tbody><tr class="odd"><td><pre><code>typedef enum  { 
  ASSOCF_NONE                  = 0x00000000,
  ASSOCF_INIT_NOREMAPCLSID     = 0x00000001,
  ASSOCF_INIT_BYEXENAME        = 0x00000002,
  ASSOCF_OPEN_BYEXENAME        = 0x00000002,
  ASSOCF_INIT_DEFAULTTOSTAR    = 0x00000004,
  ASSOCF_INIT_DEFAULTTOFOLDER  = 0x00000008,
  ASSOCF_NOUSERSETTINGS        = 0x00000010,
  ASSOCF_NOTRUNCATE            = 0x00000020,
  ASSOCF_VERIFY                = 0x00000040,
  ASSOCF_REMAPRUNDLL           = 0x00000080,
  ASSOCF_NOFIXUPS              = 0x00000100,
  ASSOCF_IGNOREBASECLASS       = 0x00000200,
  ASSOCF_INIT_IGNOREUNKNOWN    = 0x00000400,
  ASSOCF_INIT_FIXED_PROGID     = 0x00000800,
  ASSOCF_IS_PROTOCOL           = 0x00001000,
  ASSOCF_INIT_FOR_FILE         = 0x00002000
} ASSOCF;</code></pre></td></tr></tbody></table>



## <a name="constants"></a><span data-ttu-id="e3cd4-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="e3cd4-107">Constants</span></span>

 <span data-ttu-id="e3cd4-108"><span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF \_ None**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-108"><span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF\_NONE**</span></span> 

<span data-ttu-id="e3cd4-109">Nessuna delle opzioni seguenti è impostata.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-109">None of the following options are set.</span></span>

 <span data-ttu-id="e3cd4-110"><span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF \_ init \_ NOREMAPCLSID**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-110"><span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF\_INIT\_NOREMAPCLSID**</span></span> 

<span data-ttu-id="e3cd4-111">Indica ai metodi dell'interfaccia [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) di non eseguire il mapping dei valori CLSID ai valori ProgID.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-111">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface methods not to map CLSID values to ProgID values.</span></span>

 <span data-ttu-id="e3cd4-112"><span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF \_ init \_ BYEXENAME**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-112"><span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF\_INIT\_BYEXENAME**</span></span> 

<span data-ttu-id="e3cd4-113">Identifica il valore del parametro *pwszAssoc* di [**IQueryAssociations:: init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) come nome file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-113">Identifies the value of the *pwszAssoc* parameter of [**IQueryAssociations::Init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) as an executable file name.</span></span> <span data-ttu-id="e3cd4-114">Se questo flag non è impostato, la chiave radice verrà impostata sul ProgID associato alla chiave **exe** anziché sul ProgID del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-114">If this flag is not set, the root key will be set to the ProgID associated with the **.exe** key instead of the executable file's ProgID.</span></span>

 <span data-ttu-id="e3cd4-115"><span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF \_ Open \_ BYEXENAME**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-115"><span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF\_OPEN\_BYEXENAME**</span></span> 

<span data-ttu-id="e3cd4-116">Identico a **ASSOCF \_ init \_ BYEXENAME**.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-116">Identical to **ASSOCF\_INIT\_BYEXENAME**.</span></span>

 <span data-ttu-id="e3cd4-117"><span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF \_ init \_ DEFAULTTOSTAR**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-117"><span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF\_INIT\_DEFAULTTOSTAR**</span></span> 

<span data-ttu-id="e3cd4-118">Specifica che quando un metodo [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) non trova il valore richiesto sotto la chiave radice, deve tentare di recuperare il valore confrontabile dalla **\*** sottochiave.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-118">Specifies that when an [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) method does not find the requested value under the root key, it should attempt to retrieve the comparable value from the **\*** subkey.</span></span>

 <span data-ttu-id="e3cd4-119"><span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF \_ init \_ DEFAULTTOFOLDER**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-119"><span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF\_INIT\_DEFAULTTOFOLDER**</span></span> 

<span data-ttu-id="e3cd4-120">Specifica che quando un metodo [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) non trova il valore richiesto sotto la chiave radice, deve tentare di recuperare il valore confrontabile dalla sottochiave della **cartella** .</span><span class="sxs-lookup"><span data-stu-id="e3cd4-120">Specifies that when a [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) method does not find the requested value under the root key, it should attempt to retrieve the comparable value from the **Folder** subkey.</span></span>

 <span data-ttu-id="e3cd4-121"><span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**\_NOUSERSETTINGS ASSOCF**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-121"><span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**ASSOCF\_NOUSERSETTINGS**</span></span> 

<span data-ttu-id="e3cd4-122">Specifica che deve essere eseguita la ricerca solo nella **\_ \_ radice delle classi HKEY** e che l' **\_ \_ utente corrente di HKEY** deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-122">Specifies that only **HKEY\_CLASSES\_ROOT** should be searched, and that **HKEY\_CURRENT\_USER** should be ignored.</span></span>

 <span data-ttu-id="e3cd4-123"><span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF \_ NOtruncate**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-123"><span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF\_NOTRUNCATE**</span></span> 

<span data-ttu-id="e3cd4-124">Specifica che la stringa restituita non deve essere troncata.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-124">Specifies that the return string should not be truncated.</span></span> <span data-ttu-id="e3cd4-125">Restituire invece un valore di errore e le dimensioni necessarie per la stringa completa.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-125">Instead, return an error value and the required size for the complete string.</span></span>

 <span data-ttu-id="e3cd4-126"><span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**\_Verifica ASSOCF**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-126"><span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**ASSOCF\_VERIFY**</span></span> 

<span data-ttu-id="e3cd4-127">Indica ai metodi [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) di verificare che i dati siano accurati.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-127">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods to verify that data is accurate.</span></span> <span data-ttu-id="e3cd4-128">Questa impostazione consente ai metodi **IQueryAssociations** di leggere i dati dal disco rigido dell'utente per la verifica.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-128">This setting allows **IQueryAssociations** methods to read data from the user's hard disk for verification.</span></span> <span data-ttu-id="e3cd4-129">Ad esempio, è possibile controllare il nome descrittivo nel registro di sistema rispetto a quello archiviato nel file con estensione exe.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-129">For example, they can check the friendly name in the registry against the one stored in the .exe file.</span></span> <span data-ttu-id="e3cd4-130">L'impostazione di questo flag in genere riduce l'efficienza del metodo.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-130">Setting this flag typically reduces the efficiency of the method.</span></span>

 <span data-ttu-id="e3cd4-131"><span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**\_REMAPRUNDLL ASSOCF**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-131"><span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**ASSOCF\_REMAPRUNDLL**</span></span> 

<span data-ttu-id="e3cd4-132">Indica ai metodi [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) di ignorare Rundll.exe e restituire informazioni sulla propria destinazione.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-132">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods to ignore Rundll.exe and return information about its target.</span></span> <span data-ttu-id="e3cd4-133">In genere i metodi **IQueryAssociations** restituiscono informazioni sul primo file con estensione exe o dll in una stringa di comando.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-133">Typically **IQueryAssociations** methods return information about the first .exe or .dll in a command string.</span></span> <span data-ttu-id="e3cd4-134">Se un comando USA Rundll.exe, l'impostazione di questo flag indica al metodo di ignorare Rundll.exe e restituire informazioni sulla destinazione.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-134">If a command uses Rundll.exe, setting this flag tells the method to ignore Rundll.exe and return information about its target.</span></span>

 <span data-ttu-id="e3cd4-135"><span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**\_NOFIXUPS ASSOCF**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-135"><span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**ASSOCF\_NOFIXUPS**</span></span> 

<span data-ttu-id="e3cd4-136">Indica ai metodi [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) di non correggere gli errori nel registro di sistema, ad esempio il nome descrittivo di una funzione che non corrisponde a quella presente nel file con estensione exe.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-136">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods not to fix errors in the registry, such as the friendly name of a function not matching the one found in the .exe file.</span></span>

 <span data-ttu-id="e3cd4-137"><span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**\_IGNOREBASECLASS ASSOCF**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-137"><span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**ASSOCF\_IGNOREBASECLASS**</span></span> 

<span data-ttu-id="e3cd4-138">Specifica che il valore di BaseClass deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-138">Specifies that the BaseClass value should be ignored.</span></span>

 <span data-ttu-id="e3cd4-139"><span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF \_ init \_ IGNOREUNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-139"><span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF\_INIT\_IGNOREUNKNOWN**</span></span> 

<span data-ttu-id="e3cd4-140">**Introdotta in Windows 7**.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-140">**Introduced in Windows 7**.</span></span> <span data-ttu-id="e3cd4-141">Specifica che il ProgID "Unknown" deve essere ignorato. in alternativa, ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-141">Specifies that the "Unknown" ProgID should be ignored; instead, fail.</span></span>

 <span data-ttu-id="e3cd4-142"><span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**\_ \_ ProgID fisso ASSOCF \_ init**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-142"><span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**ASSOCF\_INIT\_FIXED\_PROGID**</span></span> 

<span data-ttu-id="e3cd4-143">**Introdotta in Windows 8**.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-143">**Introduced in Windows 8**.</span></span> <span data-ttu-id="e3cd4-144">Specifica che il ProgID fornito deve essere mappato utilizzando le impostazioni predefinite del sistema, anziché le impostazioni predefinite dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-144">Specifies that the supplied ProgID should be mapped using the system defaults, rather than the current user defaults.</span></span>

 <span data-ttu-id="e3cd4-145"><span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF \_ è un \_ protocollo**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-145"><span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF\_IS\_PROTOCOL**</span></span> 

<span data-ttu-id="e3cd4-146">**Introdotta in Windows 8**.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-146">**Introduced in Windows 8**.</span></span> <span data-ttu-id="e3cd4-147">Specifica che il valore è un protocollo e deve essere mappato utilizzando le impostazioni predefinite dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-147">Specifies that the value is a protocol, and should be mapped using the current user defaults.</span></span>

 <span data-ttu-id="e3cd4-148"><span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF \_ init \_ per \_ file**</span><span class="sxs-lookup"><span data-stu-id="e3cd4-148"><span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF\_INIT\_FOR\_FILE**</span></span> 

<span data-ttu-id="e3cd4-149">**Introdotta in Windows 8.1**.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-149">**Introduced in Windows 8.1**.</span></span> <span data-ttu-id="e3cd4-150">Specifica che il ProgID corrisponde a un'associazione basata sull'estensione di file.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-150">Specifies that the ProgID corresponds with a file extension based association.</span></span> <span data-ttu-id="e3cd4-151">Usare insieme al **\_ \_ \_ ProgID fisso ASSOCF init**.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-151">Use together with **ASSOCF\_INIT\_FIXED\_PROGID**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e3cd4-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3cd4-152">Requirements</span></span>



| <span data-ttu-id="e3cd4-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3cd4-153">Requirement</span></span> | <span data-ttu-id="e3cd4-154">Valore</span><span class="sxs-lookup"><span data-stu-id="e3cd4-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e3cd4-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3cd4-155">Minimum supported client</span></span> | <span data-ttu-id="e3cd4-156">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e3cd4-156">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span>               |
| <span data-ttu-id="e3cd4-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3cd4-157">Minimum supported server</span></span> | <span data-ttu-id="e3cd4-158">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e3cd4-158">Windows 2000 Server \[desktop apps only\]</span></span>                                 |
| <span data-ttu-id="e3cd4-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3cd4-159">Header</span></span>                   |  <span data-ttu-id="e3cd4-160">Shlwapi. h</span><span class="sxs-lookup"><span data-stu-id="e3cd4-160">Shlwapi.h</span></span>  |



## <a name="see-also"></a><span data-ttu-id="e3cd4-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3cd4-161">See also</span></span>

 <span data-ttu-id="e3cd4-162">[**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa)</span><span class="sxs-lookup"><span data-stu-id="e3cd4-162">[**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa)</span></span> 

 

 

<span data-ttu-id="e3cd4-163">© 2017 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-163">© 2017 Microsoft.</span></span> <span data-ttu-id="e3cd4-164">Tutti i diritti sono riservati.</span><span class="sxs-lookup"><span data-stu-id="e3cd4-164">All rights reserved.</span></span>
