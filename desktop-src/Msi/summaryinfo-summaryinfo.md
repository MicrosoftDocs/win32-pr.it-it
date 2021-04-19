---
description: La proprietà Property dell'oggetto SummaryInfo imposta o ottiene il valore per la proprietà specificata nel flusso di informazioni di riepilogo.
ms.assetid: 8e8f0987-c92b-43f3-a61a-35099188c629
title: Proprietà SummaryInfo. Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e51773a930b8868e31a7e88848300a62b717912
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327309"
---
# <a name="summaryinfoproperty-property"></a><span data-ttu-id="6a1ef-103">Proprietà SummaryInfo. Property</span><span class="sxs-lookup"><span data-stu-id="6a1ef-103">SummaryInfo.Property property</span></span>

<span data-ttu-id="6a1ef-104">La proprietà **Property** dell'oggetto [**SummaryInfo**](summaryinfo-object.md) imposta o ottiene il valore per la proprietà specificata nel flusso di informazioni di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="6a1ef-104">The **Property** property of the [**SummaryInfo**](summaryinfo-object.md) object sets or gets the value for the specified property in the summary information stream.</span></span> <span data-ttu-id="6a1ef-105">Le proprietà vengono lette quando viene creato l'oggetto [**SummaryInfo**](summaryinfo-object.md) , ma non vengono scritte fino a quando non viene chiamato il metodo di [**salvataggio permanente**](summaryinfo-persist.md) .</span><span class="sxs-lookup"><span data-stu-id="6a1ef-105">The properties are read when the [**SummaryInfo**](summaryinfo-object.md) object is created, but they are not written until the [**Persist**](summaryinfo-persist.md) method is called.</span></span> <span data-ttu-id="6a1ef-106">L'impostazione di una proprietà su Empty ne causa la rimozione. Analogamente, la richiesta di una proprietà inesistente restituisce un valore vuoto.</span><span class="sxs-lookup"><span data-stu-id="6a1ef-106">Setting a property to Empty causes its removal; likewise, requesting a nonexistent property returns an Empty value.</span></span> <span data-ttu-id="6a1ef-107">In caso contrario, i valori possono essere trasferiti come stringhe, numeri interi o tipi di data (data e ora).</span><span class="sxs-lookup"><span data-stu-id="6a1ef-107">Otherwise values may be transferred as strings, integers, or date (date time) types.</span></span>

<span data-ttu-id="6a1ef-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6a1ef-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a1ef-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a1ef-109">Syntax</span></span>


```JScript
propVal = SummaryInfo.Property
```



## <a name="property-value"></a><span data-ttu-id="6a1ef-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6a1ef-110">Property value</span></span>

<span data-ttu-id="6a1ef-111">ID di proprietà obbligatorio di una delle proprietà di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="6a1ef-111">Required property ID of one of the summary properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a1ef-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a1ef-112">Remarks</span></span>

<span data-ttu-id="6a1ef-113">**ID di proprietà di riepilogo standard**</span><span class="sxs-lookup"><span data-stu-id="6a1ef-113">**Standard Summary Property IDs**</span></span>

<span data-ttu-id="6a1ef-114">(non un'enumerazione)</span><span class="sxs-lookup"><span data-stu-id="6a1ef-114">(not an enumeration)</span></span>



| <span data-ttu-id="6a1ef-115">Nome parametro</span><span class="sxs-lookup"><span data-stu-id="6a1ef-115">Parameter name</span></span>     | <span data-ttu-id="6a1ef-116">valore</span><span class="sxs-lookup"><span data-stu-id="6a1ef-116">Value</span></span> | <span data-ttu-id="6a1ef-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a1ef-117">Description</span></span>                                       |
|--------------------|-------|---------------------------------------------------|
| <span data-ttu-id="6a1ef-118">\_dizionario PID</span><span class="sxs-lookup"><span data-stu-id="6a1ef-118">PID\_DICTIONARY</span></span>    | <span data-ttu-id="6a1ef-119">0</span><span class="sxs-lookup"><span data-stu-id="6a1ef-119">0</span></span>     | <span data-ttu-id="6a1ef-120">Formato speciale, non supportato dall'oggetto SummaryInfo</span><span class="sxs-lookup"><span data-stu-id="6a1ef-120">Special format, not support by SummaryInfo object</span></span> |
| <span data-ttu-id="6a1ef-121">tabella \_ codici PID</span><span class="sxs-lookup"><span data-stu-id="6a1ef-121">PID\_CODEPAGE</span></span>      | <span data-ttu-id="6a1ef-122">1</span><span class="sxs-lookup"><span data-stu-id="6a1ef-122">1</span></span>     | <span data-ttu-id="6a1ef-123">\_I2 VT</span><span class="sxs-lookup"><span data-stu-id="6a1ef-123">VT\_I2</span></span>                                            |
| <span data-ttu-id="6a1ef-124">\_titolo PID</span><span class="sxs-lookup"><span data-stu-id="6a1ef-124">PID\_TITLE</span></span>         | <span data-ttu-id="6a1ef-125">2</span><span class="sxs-lookup"><span data-stu-id="6a1ef-125">2</span></span>     | <span data-ttu-id="6a1ef-126">\_LPSTR VT</span><span class="sxs-lookup"><span data-stu-id="6a1ef-126">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="6a1ef-127">\_oggetto PID</span><span class="sxs-lookup"><span data-stu-id="6a1ef-127">PID\_SUBJECT</span></span>       | <span data-ttu-id="6a1ef-128">3</span><span class="sxs-lookup"><span data-stu-id="6a1ef-128">3</span></span>     | <span data-ttu-id="6a1ef-129">\_LPSTR VT</span><span class="sxs-lookup"><span data-stu-id="6a1ef-129">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="6a1ef-130">\_autore PID</span><span class="sxs-lookup"><span data-stu-id="6a1ef-130">PID\_AUTHOR</span></span>        | <span data-ttu-id="6a1ef-131">4</span><span class="sxs-lookup"><span data-stu-id="6a1ef-131">4</span></span>     | <span data-ttu-id="6a1ef-132">\_LPSTR VT</span><span class="sxs-lookup"><span data-stu-id="6a1ef-132">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="6a1ef-133">\_parole chiave PID</span><span class="sxs-lookup"><span data-stu-id="6a1ef-133">PID\_KEYWORDS</span></span>      | <span data-ttu-id="6a1ef-134">5</span><span class="sxs-lookup"><span data-stu-id="6a1ef-134">5</span></span>     | <span data-ttu-id="6a1ef-135">\_LPSTR VT</span><span class="sxs-lookup"><span data-stu-id="6a1ef-135">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="6a1ef-136">\_Commenti PID</span><span class="sxs-lookup"><span data-stu-id="6a1ef-136">PID\_COMMENTS</span></span>      | <span data-ttu-id="6a1ef-137">6</span><span class="sxs-lookup"><span data-stu-id="6a1ef-137">6</span></span>     | <span data-ttu-id="6a1ef-138">\_LPSTR VT</span><span class="sxs-lookup"><span data-stu-id="6a1ef-138">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="6a1ef-139">\_modello PID</span><span class="sxs-lookup"><span data-stu-id="6a1ef-139">PID\_TEMPLATE</span></span>      | <span data-ttu-id="6a1ef-140">7</span><span class="sxs-lookup"><span data-stu-id="6a1ef-140">7</span></span>     | <span data-ttu-id="6a1ef-141">\_LPSTR VT</span><span class="sxs-lookup"><span data-stu-id="6a1ef-141">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="6a1ef-142">\_LASTAUTHOR PID</span><span class="sxs-lookup"><span data-stu-id="6a1ef-142">PID\_LASTAUTHOR</span></span>    | <span data-ttu-id="6a1ef-143">8</span><span class="sxs-lookup"><span data-stu-id="6a1ef-143">8</span></span>     | <span data-ttu-id="6a1ef-144">\_LPSTR VT</span><span class="sxs-lookup"><span data-stu-id="6a1ef-144">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="6a1ef-145">\_REVNUMBER PID</span><span class="sxs-lookup"><span data-stu-id="6a1ef-145">PID\_REVNUMBER</span></span>     | <span data-ttu-id="6a1ef-146">9</span><span class="sxs-lookup"><span data-stu-id="6a1ef-146">9</span></span>     | <span data-ttu-id="6a1ef-147">\_LPSTR VT</span><span class="sxs-lookup"><span data-stu-id="6a1ef-147">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="6a1ef-148">\_EDITTIME PID</span><span class="sxs-lookup"><span data-stu-id="6a1ef-148">PID\_EDITTIME</span></span>      | <span data-ttu-id="6a1ef-149">10</span><span class="sxs-lookup"><span data-stu-id="6a1ef-149">10</span></span>    | <span data-ttu-id="6a1ef-150">FILETIME VT \_</span><span class="sxs-lookup"><span data-stu-id="6a1ef-150">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="6a1ef-151">\_LASTPRINTED PID</span><span class="sxs-lookup"><span data-stu-id="6a1ef-151">PID\_LASTPRINTED</span></span>   | <span data-ttu-id="6a1ef-152">11</span><span class="sxs-lookup"><span data-stu-id="6a1ef-152">11</span></span>    | <span data-ttu-id="6a1ef-153">FILETIME VT \_</span><span class="sxs-lookup"><span data-stu-id="6a1ef-153">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="6a1ef-154">PID \_ creare il \_ DTM</span><span class="sxs-lookup"><span data-stu-id="6a1ef-154">PID\_CREATE\_DTM</span></span>   | <span data-ttu-id="6a1ef-155">12</span><span class="sxs-lookup"><span data-stu-id="6a1ef-155">12</span></span>    | <span data-ttu-id="6a1ef-156">FILETIME VT \_</span><span class="sxs-lookup"><span data-stu-id="6a1ef-156">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="6a1ef-157">PID \_ LASTSAVE \_ DTM</span><span class="sxs-lookup"><span data-stu-id="6a1ef-157">PID\_LASTSAVE\_DTM</span></span> | <span data-ttu-id="6a1ef-158">13</span><span class="sxs-lookup"><span data-stu-id="6a1ef-158">13</span></span>    | <span data-ttu-id="6a1ef-159">FILETIME VT \_</span><span class="sxs-lookup"><span data-stu-id="6a1ef-159">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="6a1ef-160">\_PageCount PID</span><span class="sxs-lookup"><span data-stu-id="6a1ef-160">PID\_PAGECOUNT</span></span>     | <span data-ttu-id="6a1ef-161">14</span><span class="sxs-lookup"><span data-stu-id="6a1ef-161">14</span></span>    | <span data-ttu-id="6a1ef-162">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="6a1ef-162">VT\_I4</span></span>                                            |
| <span data-ttu-id="6a1ef-163">\_WORDCOUNT PID</span><span class="sxs-lookup"><span data-stu-id="6a1ef-163">PID\_WORDCOUNT</span></span>     | <span data-ttu-id="6a1ef-164">15</span><span class="sxs-lookup"><span data-stu-id="6a1ef-164">15</span></span>    | <span data-ttu-id="6a1ef-165">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="6a1ef-165">VT\_I4</span></span>                                            |
| <span data-ttu-id="6a1ef-166">\_charCount PID</span><span class="sxs-lookup"><span data-stu-id="6a1ef-166">PID\_CHARCOUNT</span></span>     | <span data-ttu-id="6a1ef-167">16</span><span class="sxs-lookup"><span data-stu-id="6a1ef-167">16</span></span>    | <span data-ttu-id="6a1ef-168">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="6a1ef-168">VT\_I4</span></span>                                            |
| <span data-ttu-id="6a1ef-169">\_Anteprima PID</span><span class="sxs-lookup"><span data-stu-id="6a1ef-169">PID\_THUMBNAIL</span></span>     | <span data-ttu-id="6a1ef-170">17</span><span class="sxs-lookup"><span data-stu-id="6a1ef-170">17</span></span>    | <span data-ttu-id="6a1ef-171">VT \_ CF (non supportato)</span><span class="sxs-lookup"><span data-stu-id="6a1ef-171">VT\_CF (not supported)</span></span>                            |
| <span data-ttu-id="6a1ef-172">\_appname PID</span><span class="sxs-lookup"><span data-stu-id="6a1ef-172">PID\_APPNAME</span></span>       | <span data-ttu-id="6a1ef-173">18</span><span class="sxs-lookup"><span data-stu-id="6a1ef-173">18</span></span>    | <span data-ttu-id="6a1ef-174">\_LPSTR VT</span><span class="sxs-lookup"><span data-stu-id="6a1ef-174">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="6a1ef-175">\_sicurezza PID</span><span class="sxs-lookup"><span data-stu-id="6a1ef-175">PID\_SECURITY</span></span>      | <span data-ttu-id="6a1ef-176">19</span><span class="sxs-lookup"><span data-stu-id="6a1ef-176">19</span></span>    | <span data-ttu-id="6a1ef-177">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="6a1ef-177">VT\_I4</span></span>                                            |



 

<span data-ttu-id="6a1ef-178">**Tipi di dati delle proprietà**</span><span class="sxs-lookup"><span data-stu-id="6a1ef-178">**Property Data Types**</span></span>

<span data-ttu-id="6a1ef-179">(non un'enumerazione)</span><span class="sxs-lookup"><span data-stu-id="6a1ef-179">(not an enumeration)</span></span>



| <span data-ttu-id="6a1ef-180">Nome parametro</span><span class="sxs-lookup"><span data-stu-id="6a1ef-180">Parameter name</span></span> | <span data-ttu-id="6a1ef-181">valore</span><span class="sxs-lookup"><span data-stu-id="6a1ef-181">Value</span></span> | <span data-ttu-id="6a1ef-182">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a1ef-182">Description</span></span>                                                                              |
|----------------|-------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a1ef-183">\_I2 VT</span><span class="sxs-lookup"><span data-stu-id="6a1ef-183">VT\_I2</span></span>         | <span data-ttu-id="6a1ef-184">2</span><span class="sxs-lookup"><span data-stu-id="6a1ef-184">2</span></span>     | <span data-ttu-id="6a1ef-185">intero a 16 bit</span><span class="sxs-lookup"><span data-stu-id="6a1ef-185">16-bit integer</span></span>                                                                           |
| <span data-ttu-id="6a1ef-186">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="6a1ef-186">VT\_I4</span></span>         | <span data-ttu-id="6a1ef-187">3</span><span class="sxs-lookup"><span data-stu-id="6a1ef-187">3</span></span>     | <span data-ttu-id="6a1ef-188">Intero a 32 bit</span><span class="sxs-lookup"><span data-stu-id="6a1ef-188">32-bit integer</span></span>                                                                           |
| <span data-ttu-id="6a1ef-189">\_LPSTR VT</span><span class="sxs-lookup"><span data-stu-id="6a1ef-189">VT\_LPSTR</span></span>      | <span data-ttu-id="6a1ef-190">30</span><span class="sxs-lookup"><span data-stu-id="6a1ef-190">30</span></span>    | <span data-ttu-id="6a1ef-191">string</span><span class="sxs-lookup"><span data-stu-id="6a1ef-191">String</span></span>                                                                                   |
| <span data-ttu-id="6a1ef-192">FILETIME VT \_</span><span class="sxs-lookup"><span data-stu-id="6a1ef-192">VT\_FILETIME</span></span>   | <span data-ttu-id="6a1ef-193">64</span><span class="sxs-lookup"><span data-stu-id="6a1ef-193">64</span></span>    | <span data-ttu-id="6a1ef-194">Data/ora (FILETIME, convertita in ora Variant)</span><span class="sxs-lookup"><span data-stu-id="6a1ef-194">Date time (FILETIME, converted to Variant time)</span></span>                                          |
| <span data-ttu-id="6a1ef-195">VT \_ CF</span><span class="sxs-lookup"><span data-stu-id="6a1ef-195">VT\_CF</span></span>         | <span data-ttu-id="6a1ef-196">71</span><span class="sxs-lookup"><span data-stu-id="6a1ef-196">71</span></span>    | <span data-ttu-id="6a1ef-197">Formato degli Appunti + dati, non gestiti dall'oggetto [**SummaryInfo**](summaryinfo-object.md)</span><span class="sxs-lookup"><span data-stu-id="6a1ef-197">Clipboard format + data, not handled by [**SummaryInfo**](summaryinfo-object.md) object</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="6a1ef-198">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a1ef-198">Requirements</span></span>



| <span data-ttu-id="6a1ef-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a1ef-199">Requirement</span></span> | <span data-ttu-id="6a1ef-200">Valore</span><span class="sxs-lookup"><span data-stu-id="6a1ef-200">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a1ef-201">Versione</span><span class="sxs-lookup"><span data-stu-id="6a1ef-201">Version</span></span><br/> | <span data-ttu-id="6a1ef-202">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6a1ef-202">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6a1ef-203">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6a1ef-203">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6a1ef-204">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="6a1ef-204">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="6a1ef-205">DLL</span><span class="sxs-lookup"><span data-stu-id="6a1ef-205">DLL</span></span><br/>     | <dl> <span data-ttu-id="6a1ef-206"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a1ef-206"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="6a1ef-207">IID</span><span class="sxs-lookup"><span data-stu-id="6a1ef-207">IID</span></span><br/>     | <span data-ttu-id="6a1ef-208">IID \_ ISummaryInfo è definito come 000C109B-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6a1ef-208">IID\_ISummaryInfo is defined as 000C109B-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="6a1ef-209">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a1ef-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a1ef-210">**MsiSummaryInfoSetProperty**</span><span class="sxs-lookup"><span data-stu-id="6a1ef-210">**MsiSummaryInfoSetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)
</dt> <dt>

[<span data-ttu-id="6a1ef-211">**MsiSummaryInfoGetProperty**</span><span class="sxs-lookup"><span data-stu-id="6a1ef-211">**MsiSummaryInfoGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)
</dt> </dl>

 

 




