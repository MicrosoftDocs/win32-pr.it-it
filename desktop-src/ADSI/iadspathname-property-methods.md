---
title: Metodi di proprietà IADsPathname (IADs. h)
description: Ottiene o imposta le proprietà EscapedMode.
ms.assetid: 007ec617-cff2-492a-a62c-50d65fefcd3b
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsPathname ADSI
topic_type:
- apiref
api_name:
- IADsPathname Property Methods
- IADsPathname.EscapedMode
- IADsPathname.get_EscapedMode
- IADsPathname.get_EscapedMode
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 949bd41ddb04618d238c0ddf09782e12fb228b26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225222"
---
# <a name="iadspathname-property-methods"></a><span data-ttu-id="32f69-104">Metodi di proprietà IADsPathname</span><span class="sxs-lookup"><span data-stu-id="32f69-104">IADsPathname Property Methods</span></span>

<span data-ttu-id="32f69-105">I metodi di proprietà dell'interfaccia [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) ottengono o impostano le proprietà **EscapedMode** .</span><span class="sxs-lookup"><span data-stu-id="32f69-105">The property methods of the [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) interface get or set the **EscapedMode** properties.</span></span> <span data-ttu-id="32f69-106">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="32f69-106">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="32f69-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="32f69-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="32f69-108">**EscapedMode**</span><span class="sxs-lookup"><span data-stu-id="32f69-108">**EscapedMode**</span></span>
<span data-ttu-id="32f69-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="32f69-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="32f69-110">Esaminare o specificare il modo in cui i caratteri di escape vengono gestiti in un percorso.</span><span class="sxs-lookup"><span data-stu-id="32f69-110">Examine or specify how escaped characters are handled in a pathname.</span></span> <span data-ttu-id="32f69-111">Per altre informazioni e per le opzioni definite, vedere [**\_ enumerazione della \_ modalità \_ di escape ADS**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span><span class="sxs-lookup"><span data-stu-id="32f69-111">For more information and defined options, see [**ADS\_ESCAPE\_MODE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span></span>

<dt>

<span data-ttu-id="32f69-112">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="32f69-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="32f69-113">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="32f69-113">Scripting data type: **Long**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EscapedMode(
  [out] long* retval
);
HRESULT get_EscapedMode(
  [in] long* lnEscapedMode
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="32f69-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="32f69-114">Remarks</span></span>

<span data-ttu-id="32f69-115">**EscapedMode** rappresenta uno stato.</span><span class="sxs-lookup"><span data-stu-id="32f69-115">**EscapedMode** represents a state.</span></span> <span data-ttu-id="32f69-116">È possibile attivarla o disattivarla impostando il valore ADS \_ ESCAPEDMODE \_ on o ADS \_ ESCAPEDMODE \_ off/Ads \_ ESCAPEDMODE \_ off \_ es.</span><span class="sxs-lookup"><span data-stu-id="32f69-116">You can turn it on or off, by setting it to ADS\_ESCAPEDMODE\_ON or ADS\_ESCAPEDMODE\_OFF/ADS\_ESCAPEDMODE\_OFF\_EX.</span></span> <span data-ttu-id="32f69-117">Quando è attivato o disattivato, tutti i recuperi successivi producono stringhe di percorso di escape o senza caratteri di escape.</span><span class="sxs-lookup"><span data-stu-id="32f69-117">When it is turned on, or off, all subsequent retrievals produce escaped or unescaped path strings.</span></span>

<span data-ttu-id="32f69-118">Solo in ADSI il [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) è in grado di uscire dall'escape dei percorsi.</span><span class="sxs-lookup"><span data-stu-id="32f69-118">In ADSI only the [**IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname) is capable of unescaping paths.</span></span> <span data-ttu-id="32f69-119">Tutte le altre interfacce ADSI restituiscono sempre percorsi di escape.</span><span class="sxs-lookup"><span data-stu-id="32f69-119">All other ADSI interfaces always return escaped paths.</span></span> <span data-ttu-id="32f69-120">Lo stato predefinito di **EscapedMode** è Ads \_ EscapedMode \_ default come definito in [**Ads \_ escape \_ mode \_ enum**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span><span class="sxs-lookup"><span data-stu-id="32f69-120">The default state of **EscapedMode** is ADS\_ESCAPEDMODE\_DEFAULT as defined in [**ADS\_ESCAPE\_MODE\_ENUM**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum).</span></span>

## <a name="examples"></a><span data-ttu-id="32f69-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="32f69-121">Examples</span></span>

<span data-ttu-id="32f69-122">Nell'esempio di codice seguente viene illustrato come utilizzare la proprietà **EscapedMode** per attivare/disattivare l'escape dei tre caratteri speciali seguenti: "=", "," e "/".</span><span class="sxs-lookup"><span data-stu-id="32f69-122">The following code example shows how to use the **EscapedMode** property turn on/off escaping of the following three special characters: "=",",", and "/".</span></span>


```VB
Dim path As New Pathname
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All escaped, producing:
                                          ' "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' Only "/" is unescaped:
                                          ' "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
MsgBox path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
```



<span data-ttu-id="32f69-123">Nell'esempio di codice seguente viene illustrato come utilizzare la proprietà **EscapedMode** per attivare/disattivare l'escape dei tre caratteri speciali seguenti: "=", "," e "/".</span><span class="sxs-lookup"><span data-stu-id="32f69-123">The following code example shows how to use the **EscapedMode** property turn on/off escaping of the following three special characters: "=",",", and "/".</span></span>


```VB
<%
Dim path
const ADS_SETTYPE_FULL = 1
const ADS_SETTYPE_DN   = 4
const ADS_FORMAT_WINDOWS = 1
const ADS_ESCAPEDMODE_ON = 2
const ADS_ESCAPEDMODE_OFF = 3
const ADS_ESCAPEDMODE_OFF_EX = 4
 
Set path = CreateObject("Pathname")
path.Set "CN=joy\=ful\,\/*", ADS_SETTYPE_DN
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' All escaped, producing:  "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  
' Only "/" is unescaped: "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEDMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)  ' All are unescaped:
                                          ' "LDAP://CN=joy=ful,/*"
 
 
path.Set "LDAP://CN=joy\=ful\,\/*", ADS_SETTYPE_FULL
 
path.EscapedMode = ADS_ESCAPEDMODE_ON
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,\/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy\=ful\,/*"
 
path.EscapedMode = ADS_ESCAPEMODE_OFF_EX
Response.Write path.Retrieve(ADS_FORMAT_WINDOWS)
                                  ' Produces "LDAP://CN=joy=ful,/*"
%>
```



<span data-ttu-id="32f69-124">Nell'esempio di codice riportato di seguito viene illustrato come utilizzare la proprietà **EscapedMode** .</span><span class="sxs-lookup"><span data-stu-id="32f69-124">The following code example shows how to work with the **EscapedMode** property.</span></span> <span data-ttu-id="32f69-125">Il controllo degli errori viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="32f69-125">Error checking is ignored.</span></span>


```C++
IADsPathname *pPathname=NULL;
HRESULT hr;
 
hr = CoCreateInstance(CLSID_Pathname,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsPathname,
                      (void**)&pPathname);
 
if(FAILED(hr)) 
{
    if(pPathname) pPathname->Release();
    return NULL;
}
 
pPathname->AddRef();
hr = pPathname->Set(CComBSTR("LDAP://CN=joy/ful\/*"), 
                    ADS_SETTYPE_FULL); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy/ful\/*"

SysFreeString(bstr);
 
// Set the path using ADS_SETTYPE_DN
 
hr = pPathname->Set(CComBSTR("CN=joy/ful\/*"), ADS_SETTYPE_DN); 
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_OFF);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Unescaped path: %S\n",bstr);   

// Producing "LDAP://CN=joy/ful/*"

SysFreeString(bstr);
 
hr = pPathname->put_EscapedMode(ADS_ESCAPEDMODE_ON);
hr = pPathname->Retrieve(ADS_FORMAT_WINDOWS_DN,&bstr);
printf("Escaped path: %S\n",bstr);

// Producing "LDAP://CN=joy\/ful\/*"

SysFreeString(bstr);
 
hr = pPathname->Release();
```



## <a name="requirements"></a><span data-ttu-id="32f69-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32f69-126">Requirements</span></span>



| <span data-ttu-id="32f69-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="32f69-127">Requirement</span></span> | <span data-ttu-id="32f69-128">Valore</span><span class="sxs-lookup"><span data-stu-id="32f69-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32f69-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32f69-129">Minimum supported client</span></span><br/> | <span data-ttu-id="32f69-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32f69-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="32f69-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="32f69-131">Minimum supported server</span></span><br/> | <span data-ttu-id="32f69-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32f69-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="32f69-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32f69-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="32f69-134"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="32f69-134"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="32f69-135">DLL</span><span class="sxs-lookup"><span data-stu-id="32f69-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32f69-136"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32f69-136"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="32f69-137">IID</span><span class="sxs-lookup"><span data-stu-id="32f69-137">IID</span></span><br/>                      | <span data-ttu-id="32f69-138">IID \_ IADsPathname è definito come D592AED4-F420-11D0-A36E-00C04FB950DC</span><span class="sxs-lookup"><span data-stu-id="32f69-138">IID\_IADsPathname is defined as D592AED4-F420-11D0-A36E-00C04FB950DC</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="32f69-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32f69-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32f69-140">**IADsPathname**</span><span class="sxs-lookup"><span data-stu-id="32f69-140">**IADsPathname**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspathname)
</dt> <dt>

[<span data-ttu-id="32f69-141">**\_enumerazione della \_ modalità di escape Ads \_**</span><span class="sxs-lookup"><span data-stu-id="32f69-141">**ADS\_ESCAPE\_MODE\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)
</dt> </dl>

 

 





