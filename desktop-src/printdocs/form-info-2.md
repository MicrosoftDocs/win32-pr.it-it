---
description: Contiene informazioni su un modulo di stampa localizzabile.
ms.assetid: 5cc11a77-2b9d-44a4-88de-6ed0b7460bc8
title: Struttura FORM_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_2
- _FORM_INFO_2A
- _FORM_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6e2129f9776706ce331677e75c5d9c81d82393c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227347"
---
# <a name="form_info_2-structure"></a><span data-ttu-id="776b4-103">\_Struttura info modulo \_ 2</span><span class="sxs-lookup"><span data-stu-id="776b4-103">FORM\_INFO\_2 structure</span></span>

<span data-ttu-id="776b4-104">Contiene informazioni su un modulo di stampa localizzabile.</span><span class="sxs-lookup"><span data-stu-id="776b4-104">Contains information about a localizable print form.</span></span>

## <a name="syntax"></a><span data-ttu-id="776b4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="776b4-105">Syntax</span></span>


```C++
typedef struct _FORM_INFO_2 {
  DWORD   Flags;
  LPTSTR  pName;
  SIZEL   Size;
  RECTL   ImageableArea;
  LPCSTR  pKeyword;
  DWORD   StringType;
  LPCTSTR pMuiDll;
  DWORD   dwResourceId;
  LPCTSTR pDisplayName;
  LANGID  wLangId;
} FORM_INFO_2, *PFORM_INFO_2;
```



## <a name="members"></a><span data-ttu-id="776b4-106">Members</span><span class="sxs-lookup"><span data-stu-id="776b4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="776b4-107">**Flag**</span><span class="sxs-lookup"><span data-stu-id="776b4-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="776b4-108">Proprietà del form.</span><span class="sxs-lookup"><span data-stu-id="776b4-108">The form properties.</span></span> <span data-ttu-id="776b4-109">Sono definiti i valori seguenti, ma è possibile impostarne solo uno.</span><span class="sxs-lookup"><span data-stu-id="776b4-109">The following values are defined, but only one can be set.</span></span> <span data-ttu-id="776b4-110">Quando il **modulo \_ info \_ 2** viene restituito da [**GetForm**](getform.md) o [**EnumForms**](enumforms.md), **Flags** viene impostato sul valore corrente nel database dei moduli.</span><span class="sxs-lookup"><span data-stu-id="776b4-110">When the **FORM\_INFO\_2** is returned by [**GetForm**](getform.md) or [**EnumForms**](enumforms.md), **Flags** is set to the current value in the forms database.</span></span>



| <span data-ttu-id="776b4-111">Valore</span><span class="sxs-lookup"><span data-stu-id="776b4-111">Value</span></span>         | <span data-ttu-id="776b4-112">Significato</span><span class="sxs-lookup"><span data-stu-id="776b4-112">Meaning</span></span>                                                                                                                                                                                                                                                                                  |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="776b4-113">utente del modulo \_</span><span class="sxs-lookup"><span data-stu-id="776b4-113">FORM\_USER</span></span>    | <span data-ttu-id="776b4-114">Se viene impostato questo flag di bit, il form è stato definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="776b4-114">If this bit flag is set, the form has been defined by the user.</span></span> <span data-ttu-id="776b4-115">I form con questo set di flag sono definiti nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="776b4-115">Forms with this flag set are defined in the registry.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="776b4-116">MODULO \_ incorporato</span><span class="sxs-lookup"><span data-stu-id="776b4-116">FORM\_BUILTIN</span></span> | <span data-ttu-id="776b4-117">Se viene impostato questo flag di bit, il form fa parte dello spooler.</span><span class="sxs-lookup"><span data-stu-id="776b4-117">If this bit-flag is set, the form is part of the spooler.</span></span> <span data-ttu-id="776b4-118">Le definizioni dei moduli con questo set di flag non vengono visualizzate nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="776b4-118">Form definitions with this flag set do not appear in the registry.</span></span> <span data-ttu-id="776b4-119">Non è possibile modificare i moduli predefiniti, pertanto non è necessario impostare questo flag quando la struttura viene passata a [**AddForm**](addform.md) o a [**form**](setform.md).</span><span class="sxs-lookup"><span data-stu-id="776b4-119">Built-in forms cannot be modified, so this flag should not be set when the structure is passed to [**AddForm**](addform.md) or [**SetForm**](setform.md).</span></span> |
| <span data-ttu-id="776b4-120">\_stampante modulo</span><span class="sxs-lookup"><span data-stu-id="776b4-120">FORM\_PRINTER</span></span> | <span data-ttu-id="776b4-121">Se viene impostato questo flag di bit, il form è associato a una determinata stampante e la relativa definizione viene visualizzata nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="776b4-121">If this bit flag is set, the form is associated with a certain printer, and its definition appears in the registry.</span></span>                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="776b4-122">**pName**</span><span class="sxs-lookup"><span data-stu-id="776b4-122">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="776b4-123">Puntatore a una stringa con terminazione null che specifica il nome del form.</span><span class="sxs-lookup"><span data-stu-id="776b4-123">A pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="776b4-124">Il nome del modulo non può superare i 31 caratteri.</span><span class="sxs-lookup"><span data-stu-id="776b4-124">The form name cannot exceed 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="776b4-125">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="776b4-125">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="776b4-126">Larghezza e altezza del form, in millesimi di millimetro.</span><span class="sxs-lookup"><span data-stu-id="776b4-126">The width and height of the form in thousandths of millimeters.</span></span>

</dd> <dt>

<span data-ttu-id="776b4-127">**ImageableArea**</span><span class="sxs-lookup"><span data-stu-id="776b4-127">**ImageableArea**</span></span>
</dt> <dd>

<span data-ttu-id="776b4-128">Larghezza e altezza, in millesimi di millimetri, dell'area della pagina in cui la stampante è in grado di stampare.</span><span class="sxs-lookup"><span data-stu-id="776b4-128">The width and height, in thousandths of millimeters, of the area of the page on which the printer can print.</span></span>

</dd> <dt>

<span data-ttu-id="776b4-129">**pKeyword**</span><span class="sxs-lookup"><span data-stu-id="776b4-129">**pKeyword**</span></span>
</dt> <dd>

<span data-ttu-id="776b4-130">Puntatore a un identificatore di stringa non localizzabile del form.</span><span class="sxs-lookup"><span data-stu-id="776b4-130">A pointer to a non-localizable string identifier of the form.</span></span> <span data-ttu-id="776b4-131">Quando viene passato a [**AddForm**](addform.md) o a [**Subform**](setform.md), questo fornisce al chiamante un mezzo per identificare il form in tutte le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="776b4-131">When passed to [**AddForm**](addform.md) or [**SetForm**](setform.md), this gives the caller a means of identifying the form in all locales.</span></span>

</dd> <dt>

<span data-ttu-id="776b4-132">**StringType**</span><span class="sxs-lookup"><span data-stu-id="776b4-132">**StringType**</span></span>
</dt> <dd>

<span data-ttu-id="776b4-133">Specifica il modo in cui viene ottenuto un nome visualizzato localizzato per il form in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="776b4-133">Specifies how a localized display name for the form is obtained at runtime.</span></span> <span data-ttu-id="776b4-134">Vengono definiti i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="776b4-134">The following values are defined.</span></span> <span data-ttu-id="776b4-135">È possibile impostare un solo in una determinata chiamata a [**AddForm**](addform.md) o a [**form**](setform.md).</span><span class="sxs-lookup"><span data-stu-id="776b4-135">Only one can be set in any given call to [**AddForm**](addform.md) or [**SetForm**](setform.md).</span></span> <span data-ttu-id="776b4-136">Sia \_ la stringa MUIDLL che \_ la stringa LANGPAIR possono essere impostate nel **formato \_ info \_ 2** (s) restituito da [**GetForm**](getform.md) o [**EnumForms**](enumforms.md).</span><span class="sxs-lookup"><span data-stu-id="776b4-136">Both STRING\_MUIDLL and STRING\_LANGPAIR can be set in the **FORM\_INFO\_2** (s) returned by [**GetForm**](getform.md) or [**EnumForms**](enumforms.md).</span></span> <span data-ttu-id="776b4-137">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="776b4-137">See Remarks.</span></span>



| <span data-ttu-id="776b4-138">Valore</span><span class="sxs-lookup"><span data-stu-id="776b4-138">Value</span></span>            | <span data-ttu-id="776b4-139">Significato</span><span class="sxs-lookup"><span data-stu-id="776b4-139">Meaning</span></span>                                                                                                                                                                                        |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="776b4-140">STRINGA \_ None</span><span class="sxs-lookup"><span data-stu-id="776b4-140">STRING\_NONE</span></span>     | <span data-ttu-id="776b4-141">Nessun nome visualizzato localizzato.</span><span class="sxs-lookup"><span data-stu-id="776b4-141">There is no localized display name.</span></span>                                                                                                                                                            |
| <span data-ttu-id="776b4-142">STRINGA \_ MUIDLL</span><span class="sxs-lookup"><span data-stu-id="776b4-142">STRING\_MUIDLL</span></span>   | <span data-ttu-id="776b4-143">Il nome visualizzato viene estratto dalla DLL delle risorse localizzate dell' [interfaccia utente multilingue](/windows/desktop/Intl/mui-resource-management) specificata in **pMuiDll**.</span><span class="sxs-lookup"><span data-stu-id="776b4-143">The display name is extracted from the [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) localized resources DLL specified in **pMuiDll**.</span></span> <span data-ttu-id="776b4-144">L'ID si trova nel membro **dwResourceId** .</span><span class="sxs-lookup"><span data-stu-id="776b4-144">The ID is in the **dwResourceId** member.</span></span> |
| <span data-ttu-id="776b4-145">STRINGA \_ LANGPAIR</span><span class="sxs-lookup"><span data-stu-id="776b4-145">STRING\_LANGPAIR</span></span> | <span data-ttu-id="776b4-146">Il nome visualizzato e l'ID lingua vengono forniti direttamente da **pDisplayName** e la lingua viene specificata da **wLangId**.</span><span class="sxs-lookup"><span data-stu-id="776b4-146">The display name and language ID are provided directly by **pDisplayName** and the language is specified by **wLangId**.</span></span>                                                                       |



 

</dd> <dt>

<span data-ttu-id="776b4-147">**pMuiDll**</span><span class="sxs-lookup"><span data-stu-id="776b4-147">**pMuiDll**</span></span>
</dt> <dd>

<span data-ttu-id="776b4-148">DLL di risorse localizzate dell' [interfaccia utente multilingue](/windows/desktop/Intl/mui-resource-management) che contiene il nome visualizzato localizzato.</span><span class="sxs-lookup"><span data-stu-id="776b4-148">The [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) localized resource DLL that contains the localized display name.</span></span>

</dd> <dt>

<span data-ttu-id="776b4-149">**dwResourceId**</span><span class="sxs-lookup"><span data-stu-id="776b4-149">**dwResourceId**</span></span>
</dt> <dd>

<span data-ttu-id="776b4-150">ID risorsa del nome visualizzato del modulo in **pMuiDll**.</span><span class="sxs-lookup"><span data-stu-id="776b4-150">The resource ID of the form's display name in **pMuiDll**.</span></span>

</dd> <dt>

<span data-ttu-id="776b4-151">**pDisplayName**</span><span class="sxs-lookup"><span data-stu-id="776b4-151">**pDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="776b4-152">Nome visualizzato del modulo nella lingua specificata da **wLangId**.</span><span class="sxs-lookup"><span data-stu-id="776b4-152">The form's display name in the language specified by **wLangId**.</span></span>

</dd> <dt>

<span data-ttu-id="776b4-153">**wLangId**</span><span class="sxs-lookup"><span data-stu-id="776b4-153">**wLangId**</span></span>
</dt> <dd>

<span data-ttu-id="776b4-154">Lingua del **pDisplayName**.</span><span class="sxs-lookup"><span data-stu-id="776b4-154">The language of the **pDisplayName**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="776b4-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="776b4-155">Remarks</span></span>

<span data-ttu-id="776b4-156">In una chiamata a [**AddForm**](addform.md) o a [**form**](setform.md):</span><span class="sxs-lookup"><span data-stu-id="776b4-156">On a call to [**AddForm**](addform.md) or [**SetForm**](setform.md):</span></span>

-   <span data-ttu-id="776b4-157">Se **StringType** è una stringa \_ None, **pMuiDll** e **pDisplayName** devono essere **null** e **dwResourceId** e **wLangId** devono essere 0.</span><span class="sxs-lookup"><span data-stu-id="776b4-157">If **StringType** is STRING\_NONE, both **pMuiDll** and **pDisplayName** must be **NULL** and both **dwResourceId** and **wLangId** must be 0.</span></span>
-   <span data-ttu-id="776b4-158">Se **StringType** è di stringa \_ MUIDLL, **pDisplayName** deve essere **null** e **wLangId** deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="776b4-158">If **StringType** is STRING\_MUIDLL, **pDisplayName** must be **NULL** and **wLangId** must be 0.</span></span>
-   <span data-ttu-id="776b4-159">Se **StringType** è di stringa \_ LANGPAIR, **pMuiDll** deve essere **null** e **dwResourceId** deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="776b4-159">If **StringType** is STRING\_LANGPAIR, **pMuiDll** must be **NULL** and **dwResourceId** must be 0.</span></span>

<span data-ttu-id="776b4-160">Per un **modulo \_ info \_ 2** restituito da una chiamata a [**GetForm**](getform.md) o [**EnumForms**](enumforms.md):</span><span class="sxs-lookup"><span data-stu-id="776b4-160">For a **FORM\_INFO\_2** returned by a call to [**GetForm**](getform.md) or [**EnumForms**](enumforms.md):</span></span>

-   <span data-ttu-id="776b4-161">Se **StringType** è la stringa \_ MUIDLL e la stringa \_ LANGPAIR **, pMuiDll**, **pDisplayName**, **dwResourceId** e **wLangId** avranno tutti valori validi.</span><span class="sxs-lookup"><span data-stu-id="776b4-161">If **StringType** is both STRING\_MUIDLL and STRING\_LANGPAIR, **pMuiDll**, **pDisplayName**, **dwResourceId**, and **wLangId** will all have valid values.</span></span>
-   <span data-ttu-id="776b4-162">Se **StringType** è \_ solo stringa MUIDLL, **pMuiDll** e **dwResourceId** avranno valori validi.</span><span class="sxs-lookup"><span data-stu-id="776b4-162">If **StringType** is STRING\_MUIDLL only, **pMuiDll** and **dwResourceId** will have valid values.</span></span> <span data-ttu-id="776b4-163">**pDisplayName** sarà **null** e **wLangId** sarà 0.</span><span class="sxs-lookup"><span data-stu-id="776b4-163">**pDisplayName** will be **NULL** and **wLangId** will be 0.</span></span>
-   <span data-ttu-id="776b4-164">Se **StringType** è \_ solo stringa LANGPAIR, **pDisplayName** e **wLangId** avranno valori validi.</span><span class="sxs-lookup"><span data-stu-id="776b4-164">If **StringType** is STRING\_LANGPAIR only, **pDisplayName** and **wLangId** will have valid values.</span></span> <span data-ttu-id="776b4-165">**pMuiDll** sarà **null** e **dwResourceId** sarà 0.</span><span class="sxs-lookup"><span data-stu-id="776b4-165">**pMuiDll** will be **NULL** and **dwResourceId** will be 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="776b4-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="776b4-166">Requirements</span></span>



| <span data-ttu-id="776b4-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="776b4-167">Requirement</span></span> | <span data-ttu-id="776b4-168">Valore</span><span class="sxs-lookup"><span data-stu-id="776b4-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="776b4-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="776b4-169">Minimum supported client</span></span><br/> | <span data-ttu-id="776b4-170">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="776b4-170">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="776b4-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="776b4-171">Minimum supported server</span></span><br/> | <span data-ttu-id="776b4-172">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="776b4-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="776b4-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="776b4-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="776b4-174"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="776b4-174"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="776b4-175">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="776b4-175">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="776b4-176">**\_ Informazioni sul modulo \_ \_ 2W** (Unicode) e **\_ info del modulo \_ \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="776b4-176">**\_FORM\_INFO\_2W** (Unicode) and **\_FORM\_INFO\_2A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="776b4-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="776b4-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="776b4-178">Stampa</span><span class="sxs-lookup"><span data-stu-id="776b4-178">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="776b4-179">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="776b4-179">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="776b4-180">Interfaccia utente multilingue</span><span class="sxs-lookup"><span data-stu-id="776b4-180">Multilingual User Interface</span></span>](/windows/desktop/Intl/mui-resource-management)
</dt> <dt>

[<span data-ttu-id="776b4-181">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="776b4-181">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="776b4-182">**GetForm**</span><span class="sxs-lookup"><span data-stu-id="776b4-182">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="776b4-183">**EnumForms**</span><span class="sxs-lookup"><span data-stu-id="776b4-183">**EnumForms**</span></span>](enumforms.md)
</dt> <dt>

[<span data-ttu-id="776b4-184">**Diformi**</span><span class="sxs-lookup"><span data-stu-id="776b4-184">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

