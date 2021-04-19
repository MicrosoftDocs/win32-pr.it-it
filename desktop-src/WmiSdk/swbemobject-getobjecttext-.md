---
description: Il \_ metodo GetObjectText dell'oggetto SWbemObject restituisce un rendering testuale dell'oggetto.
ms.assetid: 8b980863-14ad-4884-8897-dd076d927824
ms.tgt_platform: multiple
title: Metodo SWbemObject.GetObjectText_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2447d8361d02626e1f5ea8fae1928ffd563d52ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309826"
---
# <a name="swbemobjectgetobjecttext_-method"></a><span data-ttu-id="40a65-103">SWbemObject. GetObjectText, \_ Metodo</span><span class="sxs-lookup"><span data-stu-id="40a65-103">SWbemObject.GetObjectText\_ method</span></span>

<span data-ttu-id="40a65-104">Il **metodo \_ GetObjectText** dell'oggetto [**SWbemObject**](swbemobject.md) restituisce un rendering testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="40a65-104">The **GetObjectText\_** method of the [**SWbemObject**](swbemobject.md) object returns a textual rendering of the object.</span></span> <span data-ttu-id="40a65-105">Questo oggetto può essere utilizzato per visualizzare il contenuto di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="40a65-105">This object can be used to display an object's contents.</span></span> <span data-ttu-id="40a65-106">Attualmente, solo la sintassi MOF è supportata come formato di output.</span><span class="sxs-lookup"><span data-stu-id="40a65-106">Currently, only the MOF syntax is supported as an output format.</span></span> <span data-ttu-id="40a65-107">Si noti che il testo MOF restituito non contiene tutte le informazioni sull'oggetto. il testo MOF contiene solo informazioni sufficienti per consentire al compilatore MOF di ricreare l'oggetto originale.</span><span class="sxs-lookup"><span data-stu-id="40a65-107">Notice that the MOF text returned does not contain all the information about the object; the MOF text contains only enough information for the MOF compiler to be able to re-create the original object.</span></span> <span data-ttu-id="40a65-108">Non sono ad esempio disponibili informazioni sui qualificatori propagati o sulle proprietà della classe padre.</span><span class="sxs-lookup"><span data-stu-id="40a65-108">For instance, there is no information about the propagated qualifiers or the parent class properties.</span></span>

<span data-ttu-id="40a65-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="40a65-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="40a65-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40a65-110">Syntax</span></span>


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="40a65-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="40a65-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40a65-112">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="40a65-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="40a65-113">Riservato e deve essere 0 (zero) se specificato.</span><span class="sxs-lookup"><span data-stu-id="40a65-113">Reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40a65-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="40a65-114">Return value</span></span>

<span data-ttu-id="40a65-115">Se ha esito positivo, questo metodo restituisce una stringa che contiene il testo di output.</span><span class="sxs-lookup"><span data-stu-id="40a65-115">If successful, this method returns a string that contains the output text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="40a65-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="40a65-116">Error codes</span></span>

<span data-ttu-id="40a65-117">Dopo il completamento del metodo **GetObjectText \_** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="40a65-117">After the completion of the **GetObjectText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="40a65-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="40a65-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="40a65-119">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="40a65-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="40a65-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="40a65-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="40a65-121">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="40a65-121">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="40a65-122">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="40a65-122">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="40a65-123">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="40a65-123">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="40a65-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="40a65-124">Examples</span></span>

<span data-ttu-id="40a65-125">Il codice seguente, tratto dall' [elenco della definizione di una classe WMI nell'](https://Gallery.TechNet.Microsoft.Com/6bb54091-dd6f-4d0b-87af-2431fb8c3be6) esempio di codice VBScript formato MOF nella raccolta TechNet, recupera e visualizza la rappresentazione testuale di una definizione di classe WMI nella sintassi mof (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="40a65-125">The following code, taken from the [List the Definition of a WMI Class in MOF Format](https://Gallery.TechNet.Microsoft.Com/6bb54091-dd6f-4d0b-87af-2431fb8c3be6) VBScript code sample in the TechNet Gallery, retrieves and displays the textual representation of a WMI class definition in MOF (Managed Object Format) syntax.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Const wbemFlagUseAmendedQualifiers = &h20000 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace) 
 
Set objClass = objWMIService.Get(strClass, wbemFlagUseAmendedQualifiers) 
strMOF = objClass.GetObjectText_ 
  
WScript.Echo strMOF 
```



## <a name="requirements"></a><span data-ttu-id="40a65-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40a65-126">Requirements</span></span>



| <span data-ttu-id="40a65-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="40a65-127">Requirement</span></span> | <span data-ttu-id="40a65-128">Valore</span><span class="sxs-lookup"><span data-stu-id="40a65-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40a65-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40a65-129">Minimum supported client</span></span><br/> | <span data-ttu-id="40a65-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40a65-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="40a65-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40a65-131">Minimum supported server</span></span><br/> | <span data-ttu-id="40a65-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40a65-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="40a65-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40a65-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="40a65-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="40a65-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="40a65-135">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="40a65-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="40a65-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="40a65-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="40a65-137">DLL</span><span class="sxs-lookup"><span data-stu-id="40a65-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40a65-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40a65-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="40a65-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="40a65-139">CLSID</span></span><br/>                    | <span data-ttu-id="40a65-140">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="40a65-140">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="40a65-141">IID</span><span class="sxs-lookup"><span data-stu-id="40a65-141">IID</span></span><br/>                      | <span data-ttu-id="40a65-142">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="40a65-142">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




