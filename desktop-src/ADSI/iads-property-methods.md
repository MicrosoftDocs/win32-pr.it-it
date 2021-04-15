---
title: Metodi di proprietà IADs (IADs. h)
description: I metodi di proprietà dell'interfaccia IADs ottengono o impostano le proprietà descritte nella tabella seguente. Per ulteriori informazioni sui metodi di proprietà, vedere Metodi della proprietà di interfaccia.
ms.assetid: d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADs ADSI
topic_type:
- apiref
api_name:
- IADs Property Methods
- IADs.ADsPath
- IADs.get_ADsPath
- IADs.Class
- IADs.get_Class
- IADs.GUID
- IADs.get_GUID
- IADs.Name
- IADs.get_Name
- IADs.Parent
- IADs.get_Parent
- IADs.Schema
- IADs.get_Schema
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1134260c780958bcdba8d1f14eac535ddbf4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517433"
---
# <a name="iads-property-methods"></a><span data-ttu-id="5fa70-105">Metodi di proprietà IADs</span><span class="sxs-lookup"><span data-stu-id="5fa70-105">IADs Property Methods</span></span>

<span data-ttu-id="5fa70-106">I metodi di proprietà dell'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) ottengono o impostano le proprietà descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5fa70-106">The property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="5fa70-107">Per ulteriori informazioni sui metodi di proprietà, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="5fa70-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="5fa70-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5fa70-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="5fa70-109">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="5fa70-109">**ADsPath**</span></span>
<span data-ttu-id="5fa70-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5fa70-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="5fa70-111">Stringa ADsPath di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="5fa70-111">The ADsPath string of this object.</span></span> <span data-ttu-id="5fa70-112">La stringa identifica in modo univoco l'oggetto in un ambiente di rete.</span><span class="sxs-lookup"><span data-stu-id="5fa70-112">The string uniquely identifies this object in a network environment.</span></span> <span data-ttu-id="5fa70-113">L'oggetto può essere sempre recuperato utilizzando questo percorso.</span><span class="sxs-lookup"><span data-stu-id="5fa70-113">The object can always be retrieved using this path.</span></span>

<dt>

<span data-ttu-id="5fa70-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5fa70-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fa70-115">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5fa70-115">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsPath(
  [out] BSTR* pbstrADsPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5fa70-116">**Classe**</span><span class="sxs-lookup"><span data-stu-id="5fa70-116">**Class**</span></span>
<span data-ttu-id="5fa70-117"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5fa70-117"></dt> <dd> <dl></span></span>

<span data-ttu-id="5fa70-118">Nome della classe dello schema dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5fa70-118">The name of the object Schema class.</span></span>

<dt>

<span data-ttu-id="5fa70-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5fa70-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fa70-120">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5fa70-120">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Class(
  [out] BSTR* pbstrClass
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5fa70-121">**GUID**</span><span class="sxs-lookup"><span data-stu-id="5fa70-121">**GUID**</span></span>
<span data-ttu-id="5fa70-122"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5fa70-122"></dt> <dd> <dl></span></span>

<span data-ttu-id="5fa70-123">Identificatore univoco globale dell'oggetto directory.</span><span class="sxs-lookup"><span data-stu-id="5fa70-123">The globally unique identifier of the directory object.</span></span> <span data-ttu-id="5fa70-124">L'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) converte il **GUID** da una stringa di ottetto, archiviata in un server di directory, in un formato stringa.</span><span class="sxs-lookup"><span data-stu-id="5fa70-124">The [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface converts the **GUID** from an octet string, as stored on a directory server, into a string format.</span></span>

<dt>

<span data-ttu-id="5fa70-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5fa70-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fa70-126">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5fa70-126">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GUID(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5fa70-127">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5fa70-127">**Name**</span></span>
<span data-ttu-id="5fa70-128"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5fa70-128"></dt> <dd> <dl></span></span>

<span data-ttu-id="5fa70-129">Nome relativo dell'oggetto come denominato all'interno del servizio directory sottostante.</span><span class="sxs-lookup"><span data-stu-id="5fa70-129">The relative name of the object as named within the underlying directory service.</span></span> <span data-ttu-id="5fa70-130">Questo nome distingue questo oggetto dagli elementi di pari livello.</span><span class="sxs-lookup"><span data-stu-id="5fa70-130">This name distinguishes this object from its siblings.</span></span>

<dt>

<span data-ttu-id="5fa70-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5fa70-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fa70-132">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5fa70-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5fa70-133">**Parent**</span><span class="sxs-lookup"><span data-stu-id="5fa70-133">**Parent**</span></span>
<span data-ttu-id="5fa70-134"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5fa70-134"></dt> <dd> <dl></span></span>

<span data-ttu-id="5fa70-135">Stringa ADsPath del contenitore padre.</span><span class="sxs-lookup"><span data-stu-id="5fa70-135">The ADsPath string of the parent container.</span></span> <span data-ttu-id="5fa70-136">Active Directory non consente la creazione di ADsPath di un determinato oggetto concatenando le proprietà **Parent** e **Name** .</span><span class="sxs-lookup"><span data-stu-id="5fa70-136">Active Directory does not permit the formation of the ADsPath of a given object by concatenating the **Parent** and **Name** properties.</span></span> <span data-ttu-id="5fa70-137">Sebbene questa operazione potrebbe funzionare in alcuni provider, non è garantito che funzioni per tutte le implementazioni.</span><span class="sxs-lookup"><span data-stu-id="5fa70-137">While this operation might work in some providers, it is not guaranteed to work for all implementations.</span></span> <span data-ttu-id="5fa70-138">ADsPath è sicuramente valido e deve essere usato sempre per recuperare il puntatore all'interfaccia di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="5fa70-138">The ADsPath is guaranteed to be valid and should always be used to retrieve an object's interface pointer.</span></span>

<dt>

<span data-ttu-id="5fa70-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5fa70-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fa70-140">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5fa70-140">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parent(
  [out] BSTR* pbstrParent
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="5fa70-141">**Schema**</span><span class="sxs-lookup"><span data-stu-id="5fa70-141">**Schema**</span></span>
<span data-ttu-id="5fa70-142"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="5fa70-142"></dt> <dd> <dl></span></span>

<span data-ttu-id="5fa70-143">Stringa ADsPath dell'oggetto della classe dello schema di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="5fa70-143">The ADsPath string of the Schema class object of this object.</span></span>

<dt>

<span data-ttu-id="5fa70-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5fa70-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fa70-145">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5fa70-145">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Schema(
  [out] BSTR* pbstrSchema
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="5fa70-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="5fa70-146">Remarks</span></span>

<span data-ttu-id="5fa70-147">In Active Directory il **GUID** restituito dal GUID è una stringa di esadecimali.</span><span class="sxs-lookup"><span data-stu-id="5fa70-147">In Active Directory, the **GUID** returned from GUID is a string of hexadecimals.</span></span> <span data-ttu-id="5fa70-148">Usare il **GUID** risultante per eseguire l'associazione diretta all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5fa70-148">Use the resultant **GUID** to bind to the object directly.</span></span>


```VB
Dim x As IADs
Set x = GetObject("LDAP://servername/<GUID=xxx>")
```



<span data-ttu-id="5fa70-149">dove xxx è il valore restituito dalla proprietà GUID.</span><span class="sxs-lookup"><span data-stu-id="5fa70-149">where xxx is the value returned from the GUID property.</span></span> <span data-ttu-id="5fa70-150">Per ulteriori informazioni, vedere [utilizzo di objectGUID per l'associazione a un oggetto](/windows/desktop/AD/using-objectguid-to-bind-to-an-object).</span><span class="sxs-lookup"><span data-stu-id="5fa70-150">For more information, see [Using objectGUID to Bind to an Object](/windows/desktop/AD/using-objectguid-to-bind-to-an-object).</span></span> <span data-ttu-id="5fa70-151">Si noti che se si utilizza un GUID per eseguire l'associazione a un oggetto, il metodo di proprietà **ADsPath** restituisce valori diversi dai valori normali che verrebbero restituiti se è stato utilizzato un nome distinto (DN) per eseguire l'associazione allo stesso oggetto.</span><span class="sxs-lookup"><span data-stu-id="5fa70-151">Be aware that if you use a GUID to bind to an object, the **ADsPath** property method returns values that are different from the normal values that would be returned if you used a distinguished name (DN) to bind to the same object.</span></span> <span data-ttu-id="5fa70-152">Ad esempio, nella tabella seguente sono elencati i valori restituiti quando si utilizzano i due diversi metodi di associazione per associare lo stesso oggetto utente.</span><span class="sxs-lookup"><span data-stu-id="5fa70-152">For example, the following table lists the values returned when using the two different binding methods to bind to the same user object.</span></span>



|             | <span data-ttu-id="5fa70-153">Binding con DN</span><span class="sxs-lookup"><span data-stu-id="5fa70-153">Bind using DN</span></span>                                           | <span data-ttu-id="5fa70-154">Associa tramite GUID</span><span class="sxs-lookup"><span data-stu-id="5fa70-154">Bind using GUID</span></span>                                             |
|-------------|---------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="5fa70-155">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5fa70-155">**Name**</span></span>    | <span data-ttu-id="5fa70-156">CN = Jeff Smith</span><span class="sxs-lookup"><span data-stu-id="5fa70-156">CN=Jeff Smith</span></span>                                           | <span data-ttu-id="5fa70-157">CN = Jeff Smith</span><span class="sxs-lookup"><span data-stu-id="5fa70-157">CN=Jeff Smith</span></span>                                               |
| <span data-ttu-id="5fa70-158">**Parent**</span><span class="sxs-lookup"><span data-stu-id="5fa70-158">**Parent**</span></span>  | <span data-ttu-id="5fa70-159">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span><span class="sxs-lookup"><span data-stu-id="5fa70-159">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span></span>               | <span data-ttu-id="5fa70-160">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span><span class="sxs-lookup"><span data-stu-id="5fa70-160">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span></span>                   |
| <span data-ttu-id="5fa70-161">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="5fa70-161">**ADsPath**</span></span> | <span data-ttu-id="5fa70-162">LDAP://server/CN=Jeff Smith, CN = Users, DC = Fabrikam, DC = com</span><span class="sxs-lookup"><span data-stu-id="5fa70-162">LDAP://server/CN=Jeff Smith,CN=Users,DC=Fabrikam,DC=com</span></span> | <span data-ttu-id="5fa70-163">LDAP://server/<GUID = c0f59dfcf507d311a99e0000f879f7c7></span><span class="sxs-lookup"><span data-stu-id="5fa70-163">LDAP://server/<GUID=c0f59dfcf507d311a99e0000f879f7c7></span></span> |



 

> [!Note]  
> <span data-ttu-id="5fa70-164">Il provider WinNT non supporta l'associazione mediante il **GUID** dell'oggetto e restituisce la proprietà **GUID** in un formato di stringa leggermente diverso.</span><span class="sxs-lookup"><span data-stu-id="5fa70-164">The WinNT provider does not support binding using the object **GUID**, and returns the **GUID** property in a slightly different string format.</span></span>

 

## <a name="examples"></a><span data-ttu-id="5fa70-165">Esempio</span><span class="sxs-lookup"><span data-stu-id="5fa70-165">Examples</span></span>

<span data-ttu-id="5fa70-166">Nell'esempio di codice seguente viene illustrato come recuperare i dati oggetto utilizzando metodi di proprietà dell'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="5fa70-166">The following code example shows how to retrieve object data using property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


```VB
Dim x As IADs
Dim parent As IADsContainer
Dim cls As IADsClass
Dim op As Variant

On Error GoTo Cleanup

Set x = GetObject("WinNT://Fabrikam/Administrator")
Debug.Print "Object Name: " & x.Name
Debug.Print "Object Path: " & x.ADsPath
Debug.Print "Object Class: " & x.Class
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Debug.Print "Class Name is: " & cls.Name
For Each op In cls.OptionalProperties
    Debug.Print "Optional Property: " & op
Next op

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set x = Nothing
    Set parent = Nothing
    Set cls = Nothing
```



<span data-ttu-id="5fa70-167">Nell'esempio di codice seguente viene illustrato come recuperare i dati oggetto utilizzando metodi di proprietà dell'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="5fa70-167">The following code example shows how to retrieve object data using property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


```VB
<HTML>
<head><title></title></head>

<body>
<%
Dim x 
On Error Resume Next
 
Set x = GetObject("WinNT://Fabrikam/Administrator")
Response.Write "Object Name: " & x.Name & "<br>"
Response.Write "Object Path: " & x.ADsPath & "<br>"
Response.Write "Object Class: " & x.Class & "<br>"
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Response.Write "Class Name is: " & cls.Name & "<br>"
For Each op In cls.OptionalProperties
    Response.Write "Optional Property: " & op & "<br>"
Next op
%>

</body>
</html>
```



<span data-ttu-id="5fa70-168">Nell'esempio di codice seguente viene illustrato come utilizzare i metodi di proprietà dell'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="5fa70-168">The following code example shows how to work with the property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


```C++
#include <stdio.h>
#include <activeds.h>
 
int main(int argc, char* argv[])
{
    IADs *pADs = NULL;
    IADsUser *pADsUser = NULL;
    IADsClass *pCls = NULL;
    CComBSTR sbstr;
 
    HRESULT hr = CoInitialize(NULL);
    if (hr != S_OK) { return 0; }
 
    hr=ADsGetObject(L"WinNT://Fabrikam/Administrator",
                IID_IADsUser,
                (void**) &pADsUser);
    if (hr != S_OK) { goto Cleanup; }
 
    hr = pADsUser->QueryInterface(IID_IADs, (void**) &pADs);
    if( hr !=S_OK) { goto Cleanup;}
 
    pADsUser->Release();
 
    if( S_OK == pADs->get_Name(&sbstr) ) {
        printf("Object Name: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_ADsPath(&sbstr) ) {
        printf("Object path: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_Class(&sbstr) ) {
        printf("Object class: %S\n",sbstr);
    }
 
    hr = pADs->get_Schema(&sbstr);
    if ( hr != S_OK) {goto Cleanup;}
 
    hr = ADsGetObject(sbstr,IID_IADsClass, (void**)&pCls);
    if ( hr != S_OK) {goto Cleanup;}
    if( S_OK == pCls->get_Name(&sbstr) ) {
        printf("Class name is %S\n", sbstr);
    }
 
 Cleanup:
    if(pADs)
        pADs->Release();

    if(pIADsUser)
        pADsUser->Release();

    if(IADsClass)
        pADsClass->Release();

    CoUninitialize();

    if(hr==S_OK)
    {
        return 1;
    }
    else
    {
        return 0;
    }
}
```



## <a name="requirements"></a><span data-ttu-id="5fa70-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fa70-169">Requirements</span></span>



| <span data-ttu-id="5fa70-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fa70-170">Requirement</span></span> | <span data-ttu-id="5fa70-171">Valore</span><span class="sxs-lookup"><span data-stu-id="5fa70-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fa70-172">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fa70-172">Minimum supported client</span></span><br/> | <span data-ttu-id="5fa70-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5fa70-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5fa70-174">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fa70-174">Minimum supported server</span></span><br/> | <span data-ttu-id="5fa70-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5fa70-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5fa70-176">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5fa70-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fa70-177"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fa70-177"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="5fa70-178">DLL</span><span class="sxs-lookup"><span data-stu-id="5fa70-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fa70-179"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fa70-179"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="5fa70-180">IID</span><span class="sxs-lookup"><span data-stu-id="5fa70-180">IID</span></span><br/>                      | <span data-ttu-id="5fa70-181">IID \_ IADs è definito come FD8256D0-FD15-11CE-ABC4-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="5fa70-181">IID\_IADs is defined as FD8256D0-FD15-11CE-ABC4-02608C9E7553</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="5fa70-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5fa70-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fa70-183">**IADs**</span><span class="sxs-lookup"><span data-stu-id="5fa70-183">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="5fa70-184">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="5fa70-184">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> </dl>

 

