---
description: Restituisce una rappresentazione XML di un oggetto o di un'istanza di. Il file di testo è formattato nel formato XML specificato come indicato in WbemObjectTextFormatEnum.
ms.assetid: 98961d94-8360-4ed7-b1b1-20b4fca45d45
ms.tgt_platform: multiple
title: Metodo SWbemObjectEx.GetText_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6f174397b1ace85acd90ffe3def6b8122bf8d7f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058219"
---
# <a name="swbemobjectexgettext_-method"></a><span data-ttu-id="62c7e-104">Metodo SWbemObjectEx. GetText \_</span><span class="sxs-lookup"><span data-stu-id="62c7e-104">SWbemObjectEx.GetText\_ method</span></span>

<span data-ttu-id="62c7e-105">Il metodo **gettext \_** dell'oggetto [**SWBEMOBJECTEX**](swbemobjectex.md) restituisce una rappresentazione XML di un oggetto o di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="62c7e-105">The **GetText\_** method of the [**SWbemObjectEx**](swbemobjectex.md) object returns an XML representation of an object or instance.</span></span> <span data-ttu-id="62c7e-106">Il file di testo è formattato nel formato XML specificato come indicato in [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum).</span><span class="sxs-lookup"><span data-stu-id="62c7e-106">The text file is formatted in the XML format specified as shown in [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum).</span></span>

<span data-ttu-id="62c7e-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="62c7e-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="62c7e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62c7e-108">Syntax</span></span>


```VB
strObj = .GetText_( _
  ByVal iTextFormat, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="62c7e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="62c7e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62c7e-110">*iTextFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62c7e-110">*iTextFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c7e-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="62c7e-111">Required.</span></span> <span data-ttu-id="62c7e-112">Valore di [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) che specifica il formato XML risultante.</span><span class="sxs-lookup"><span data-stu-id="62c7e-112">A value from [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) that specifies the resulting XML format.</span></span>

</dd> <dt>

<span data-ttu-id="62c7e-113">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="62c7e-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="62c7e-114">Flag di operazione riservati.</span><span class="sxs-lookup"><span data-stu-id="62c7e-114">Reserved operation flags.</span></span> <span data-ttu-id="62c7e-115">Il valore predefinito è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="62c7e-115">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="62c7e-116">*objWbemNamedValueSet* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="62c7e-116">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="62c7e-117">Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che imposta il contesto per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="62c7e-117">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that sets context for the operation.</span></span> <span data-ttu-id="62c7e-118">Il valore predefinito è Null.</span><span class="sxs-lookup"><span data-stu-id="62c7e-118">The default is null.</span></span> <span data-ttu-id="62c7e-119">Per ulteriori informazioni sulle coppie nome/valore consentite, vedere la sezione Osservazioni di seguito.</span><span class="sxs-lookup"><span data-stu-id="62c7e-119">For more information about the name/value pairs permitted, see Remarks below.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62c7e-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62c7e-120">Return value</span></span>

<span data-ttu-id="62c7e-121">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="62c7e-121">This method has no return values.</span></span>

## <a name="error-codes"></a><span data-ttu-id="62c7e-122">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="62c7e-122">Error codes</span></span>

<span data-ttu-id="62c7e-123">Dopo il completamento del metodo **gettext \_** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="62c7e-123">After completion of the **GetText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="62c7e-124">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="62c7e-124">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="62c7e-125">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="62c7e-125">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="62c7e-126">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="62c7e-126">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="62c7e-127">Il formato richiesto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="62c7e-127">The requested format was not found.</span></span>

</dd> <dt>

<span data-ttu-id="62c7e-128">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="62c7e-128">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="62c7e-129">Uno dei parametri della chiamata non è corretto.</span><span class="sxs-lookup"><span data-stu-id="62c7e-129">One of the parameters to the call is not correct.</span></span>

</dd> <dt>

<span data-ttu-id="62c7e-130">**wbemErrCriticalError** -2147749898 (0x8004100a)</span><span class="sxs-lookup"><span data-stu-id="62c7e-130">**wbemErrCriticalError** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="62c7e-131">Si è verificato un errore interno, irreversibile e inaspettato.</span><span class="sxs-lookup"><span data-stu-id="62c7e-131">An internal, critical, and unexpected error occurred.</span></span> <span data-ttu-id="62c7e-132">Segnalare l'errore al Servizio Supporto Tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="62c7e-132">Report this error to Microsoft Technical Support.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62c7e-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="62c7e-133">Remarks</span></span>

<span data-ttu-id="62c7e-134">Quando si costruisce il [**SWbemNamedValueSet**](swbemnamedvalueset.md), sono consentite solo le seguenti coppie nome/valore.</span><span class="sxs-lookup"><span data-stu-id="62c7e-134">When constructing your [**SWbemNamedValueSet**](swbemnamedvalueset.md), only the following name/value pairs are permitted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="62c7e-135">Nome</span><span class="sxs-lookup"><span data-stu-id="62c7e-135">Name</span></span></th>
<th><span data-ttu-id="62c7e-136">Valore</span><span class="sxs-lookup"><span data-stu-id="62c7e-136">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="62c7e-137">LocalOnly</span><span class="sxs-lookup"><span data-stu-id="62c7e-137">LocalOnly</span></span></td>
<td><span data-ttu-id="62c7e-138"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="62c7e-138"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="62c7e-139">Se <strong>true</strong>, nel codice XML risultante sono presenti solo metodi e proprietà definite localmente.</span><span class="sxs-lookup"><span data-stu-id="62c7e-139">If <strong>TRUE</strong>, only locally defined properties and methods are present in the resulting XML.</span></span> <span data-ttu-id="62c7e-140">Il valore predefinito è <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="62c7e-140">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62c7e-141">IncludeQualifiers</span><span class="sxs-lookup"><span data-stu-id="62c7e-141">IncludeQualifiers</span></span></td>
<td><span data-ttu-id="62c7e-142"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="62c7e-142"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="62c7e-143">Se <strong>true</strong>, i qualificatori delle classi, delle istanze, delle proprietà e dei metodi sono inclusi nel codice XML risultante.</span><span class="sxs-lookup"><span data-stu-id="62c7e-143">If <strong>TRUE</strong>, qualifiers of classes, instances, properties, and methods are included in the resulting XML.</span></span> <span data-ttu-id="62c7e-144">Il valore predefinito è <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="62c7e-144">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62c7e-145">PathLevel</span><span class="sxs-lookup"><span data-stu-id="62c7e-145">PathLevel</span></span></td>
<td><span data-ttu-id="62c7e-146"><strong>VT-I4</strong></span><span class="sxs-lookup"><span data-stu-id="62c7e-146"><strong>VT-I4</strong></span></span><br/> <span data-ttu-id="62c7e-147">Il valore predefinito è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="62c7e-147">Default is 0 (zero).</span></span> <span data-ttu-id="62c7e-148">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="62c7e-148">Possible values are:</span></span><br/>
<ul>
<li><span data-ttu-id="62c7e-149">0: un <CLASS> <INSTANCE> elemento o viene creato a seconda che l'oggetto sia una classe o un'istanza.</span><span class="sxs-lookup"><span data-stu-id="62c7e-149">0: A <CLASS> or <INSTANCE> element is created depending on whether the object is a class or instance.</span></span></li>
<li><span data-ttu-id="62c7e-150">1: <VALUE.NAMEDOBJECT> viene generato un elemento.</span><span class="sxs-lookup"><span data-stu-id="62c7e-150">1: A <VALUE.NAMEDOBJECT> element is generated.</span></span></li>
<li><span data-ttu-id="62c7e-151">2: <VALUE.OBJECTWITHLOCALPATH> viene generato un elemento.</span><span class="sxs-lookup"><span data-stu-id="62c7e-151">2: A <VALUE.OBJECTWITHLOCALPATH> element is generated.</span></span></li>
<li><span data-ttu-id="62c7e-152">3: <VALUE.OBJECTWITHPATH> viene generato un elemento.</span><span class="sxs-lookup"><span data-stu-id="62c7e-152">3: A <VALUE.OBJECTWITHPATH> element is generated.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="62c7e-153">ExcludeSystemProperties</span><span class="sxs-lookup"><span data-stu-id="62c7e-153">ExcludeSystemProperties</span></span></td>
<td><span data-ttu-id="62c7e-154"><strong>VT-BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="62c7e-154"><strong>VT-BOOL</strong></span></span><br/> <span data-ttu-id="62c7e-155">Se <strong>true</strong>, le proprietà di sistema, come __NAMESPACE, sono escluse dall'output.</span><span class="sxs-lookup"><span data-stu-id="62c7e-155">If <strong>TRUE</strong>, system properties, like __NAMESPACE, are excluded from the output.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="62c7e-156">IncludeClassOrigin</span><span class="sxs-lookup"><span data-stu-id="62c7e-156">IncludeClassOrigin</span></span></td>
<td><span data-ttu-id="62c7e-157"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="62c7e-157"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="62c7e-158">Se <strong>true</strong>, l'attributo Origin della classe viene impostato negli <PROPERTY> <METHOD> elementi e.</span><span class="sxs-lookup"><span data-stu-id="62c7e-158">If <strong>TRUE</strong>, the class origin attribute is set on the <PROPERTY> and <METHOD> elements.</span></span> <span data-ttu-id="62c7e-159">Il valore predefinito è <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="62c7e-159">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="62c7e-160">Per ulteriori informazioni sulla creazione di un [**SWbemNamedValueSet**](swbemnamedvalueset.md), vedere [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md).</span><span class="sxs-lookup"><span data-stu-id="62c7e-160">For more information about creating an [**SWbemNamedValueSet**](swbemnamedvalueset.md), see [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md).</span></span>

## <a name="examples"></a><span data-ttu-id="62c7e-161">Esempio</span><span class="sxs-lookup"><span data-stu-id="62c7e-161">Examples</span></span>

<span data-ttu-id="62c7e-162">Nello script seguente viene illustrato come ottenere una rappresentazione XML della definizione della classe [**\_ BIOS Win32**](/windows/desktop/CIMWin32Prov/win32-bios) .</span><span class="sxs-lookup"><span data-stu-id="62c7e-162">The following script shows how to obtain an XML representation of the [**Win32\_Bios**](/windows/desktop/CIMWin32Prov/win32-bios) class definition.</span></span> <span data-ttu-id="62c7e-163">Specificando una particolare istanza di **\_ BIOS Win32**, è possibile ottenere i dati dell'oggetto in formato XML.</span><span class="sxs-lookup"><span data-stu-id="62c7e-163">By specifying a particular instance of **Win32\_Bios**, you can obtain that object's data in XML.</span></span>


```VB
' Connect to the default namespace (root\cimv2) with the default
' impersonation level ("impersonate") and obtain a Win32_Bios class
' object.
Set obj = GetObject("winmgmts:win32_bios")

' Use the value for the desired XML CIM DTD format. 
XMLDtd = 1
Text = obj.GetText_(XMLDtd)
wscript.echo Text
```



## <a name="requirements"></a><span data-ttu-id="62c7e-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62c7e-164">Requirements</span></span>



| <span data-ttu-id="62c7e-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="62c7e-165">Requirement</span></span> | <span data-ttu-id="62c7e-166">Valore</span><span class="sxs-lookup"><span data-stu-id="62c7e-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62c7e-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62c7e-167">Minimum supported client</span></span><br/> | <span data-ttu-id="62c7e-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62c7e-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62c7e-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62c7e-169">Minimum supported server</span></span><br/> | <span data-ttu-id="62c7e-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62c7e-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62c7e-171">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62c7e-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="62c7e-172"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="62c7e-172"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="62c7e-173">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="62c7e-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="62c7e-174"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="62c7e-174"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="62c7e-175">DLL</span><span class="sxs-lookup"><span data-stu-id="62c7e-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62c7e-176"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62c7e-176"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="62c7e-177">CLSID</span><span class="sxs-lookup"><span data-stu-id="62c7e-177">CLSID</span></span><br/>                    | <span data-ttu-id="62c7e-178">\_SWBEMOBJECTEX CLSID</span><span class="sxs-lookup"><span data-stu-id="62c7e-178">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="62c7e-179">IID</span><span class="sxs-lookup"><span data-stu-id="62c7e-179">IID</span></span><br/>                      | <span data-ttu-id="62c7e-180">\_ISWBEMOBJECTEX IID</span><span class="sxs-lookup"><span data-stu-id="62c7e-180">IID\_ISWbemObjectEx</span></span><br/>                                                          |



 

