---
title: Metodi di proprietà IADsSecurityDescriptor (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsSecurityDescriptor ottengono o impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: e0c50740-de98-4913-b3df-6fd53263bcc8
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsSecurityDescriptor ADSI
topic_type:
- apiref
api_name:
- IADsSecurityDescriptor Property Methods
- IADsSecurityDescriptor.Revision
- IADsSecurityDescriptor.get_Revision
- IADsSecurityDescriptor.put_Revision
- IADsSecurityDescriptor.Control
- IADsSecurityDescriptor.get_Control
- IADsSecurityDescriptor.put_Control
- IADsSecurityDescriptor.Owner
- IADsSecurityDescriptor.get_Owner
- IADsSecurityDescriptor.put_Owner
- IADsSecurityDescriptor.OwnerDefaulted
- IADsSecurityDescriptor.get_OwnerDefaulted
- IADsSecurityDescriptor.put_OwnerDefaulted
- IADsSecurityDescriptor.Group
- IADsSecurityDescriptor.get_Group
- IADsSecurityDescriptor.put_Group
- IADsSecurityDescriptor.GroupDefaulted
- IADsSecurityDescriptor.get_GroupDefaultedY
- IADsSecurityDescriptor.put_GroupDefaulted
- IADsSecurityDescriptor.DiscretionaryAcl
- IADsSecurityDescriptor.get_DiscretionaryAcl
- IADsSecurityDescriptor.put_DiscretionaryAcl
- IADsSecurityDescriptor.DaclDefaulted
- IADsSecurityDescriptor.get_DaclDefaulted
- IADsSecurityDescriptor.put_DaclDefaulted
- IADsSecurityDescriptor.SystemAcl
- IADsSecurityDescriptor.get_SystemAcl
- IADsSecurityDescriptor.put_SystemAcl
- IADsSecurityDescriptor.SaclDefaulted
- IADsSecurityDescriptor.get_SaclDefaulted
- IADsSecurityDescriptor.put_SaclDefaulted
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5c07213a2d2a3a1b64621dbc40f707b0900703
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119603"
---
# <a name="iadssecuritydescriptor-property-methods"></a><span data-ttu-id="7cba7-105">Metodi di proprietà IADsSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="7cba7-105">IADsSecurityDescriptor Property Methods</span></span>

<span data-ttu-id="7cba7-106">I metodi di proprietà dell'interfaccia [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) ottengono o impostano le proprietà descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7cba7-106">The property methods of the [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="7cba7-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="7cba7-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="7cba7-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7cba7-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="7cba7-109">**Controllo**</span><span class="sxs-lookup"><span data-stu-id="7cba7-109">**Control**</span></span>
<span data-ttu-id="7cba7-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7cba7-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="7cba7-111">Flag che qualificano il significato del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="7cba7-111">Flags that qualify the meaning of the security descriptor.</span></span> <span data-ttu-id="7cba7-112">I valori vengono ricavati dalla struttura del [**\_ \_ controllo descrittore di sicurezza**](/windows/desktop/SecAuthZ/security-descriptor-control) Win32.</span><span class="sxs-lookup"><span data-stu-id="7cba7-112">Values are taken from the Win32 [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) structure.</span></span>

<dt>

<span data-ttu-id="7cba7-113">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7cba7-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7cba7-114">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="7cba7-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Control(
  [out] LONG* plControl
);
HRESULT put_Control(
  [in] LONG lControl
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7cba7-115">**DaclDefaulted**</span><span class="sxs-lookup"><span data-stu-id="7cba7-115">**DaclDefaulted**</span></span>
<span data-ttu-id="7cba7-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7cba7-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="7cba7-117">Flag del tipo BOOL che indica se l'elenco DACL deriva da un meccanismo predefinito, anziché essere specificato in modo esplicito dal provider originale del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="7cba7-117">A flag of the BOOL type that indicates if the DACL is derived from a default mechanism, rather than being provided explicitly by the original provider of the security descriptor.</span></span> <span data-ttu-id="7cba7-118">Se, ad esempio, il creatore di un oggetto non specifica un DACL, l'oggetto riceve l'elenco DACL predefinito dal token di accesso del creatore.</span><span class="sxs-lookup"><span data-stu-id="7cba7-118">For example, if an object's creator does not specify a DACL, the object receives the default DACL from the creator's access token.</span></span> <span data-ttu-id="7cba7-119">Questo flag può influire sul modo in cui il sistema considera l'elenco DACL rispetto all'ereditarietà ACE.</span><span class="sxs-lookup"><span data-stu-id="7cba7-119">This flag can affect how the system treats the DACL, with respect to ACE inheritance.</span></span> <span data-ttu-id="7cba7-120">Questo flag viene ignorato dal sistema se il \_ flag if \_ non è impostato.</span><span class="sxs-lookup"><span data-stu-id="7cba7-120">The system ignores this flag if the SE\_DACL\_PRESENT flag is not set.</span></span>

<dt>

<span data-ttu-id="7cba7-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7cba7-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7cba7-122">Tipo di dati di scripting: **\_ bool Variant**</span><span class="sxs-lookup"><span data-stu-id="7cba7-122">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DaclDefaulted(
  [out] VARIANT_BOOL* fDaclDefaulted
);
HRESULT put_DaclDefaulted(
  [in] VARIANT_BOOL fDaclDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7cba7-123">**DiscretionaryAcl**</span><span class="sxs-lookup"><span data-stu-id="7cba7-123">**DiscretionaryAcl**</span></span>
<span data-ttu-id="7cba7-124"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7cba7-124"></dt> <dd> <dl></span></span>

<span data-ttu-id="7cba7-125">Elenco di controllo di accesso discrezionale (DACL) che specifica i tipi di accesso concessi all'oggetto per utenti e gruppi specificati.</span><span class="sxs-lookup"><span data-stu-id="7cba7-125">Discretionary access-control list (DACL) that specifies the types of access granted to the object for specified users and groups.</span></span> <span data-ttu-id="7cba7-126">Per ulteriori informazioni sugli elenchi DACL, vedere [DACL null e elenchi DACL vuoti](/windows/desktop/AD/null-dacls-and-empty-dacls).</span><span class="sxs-lookup"><span data-stu-id="7cba7-126">For more information about DACLs, see [Null DACLs and Empty DACLs](/windows/desktop/AD/null-dacls-and-empty-dacls).</span></span>

<dt>

<span data-ttu-id="7cba7-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7cba7-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7cba7-128">Tipo di dati di scripting: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="7cba7-128">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DiscretionaryAcl(
  [out] IDispatch** ppIDispDACL
);
HRESULT put_DiscretionaryAcl(
  [in] IDispatch* pIDispDACL
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7cba7-129">**Gruppo**</span><span class="sxs-lookup"><span data-stu-id="7cba7-129">**Group**</span></span>
<span data-ttu-id="7cba7-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7cba7-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="7cba7-131">Gruppo a cui appartiene l'ID di sicurezza del proprietario.</span><span class="sxs-lookup"><span data-stu-id="7cba7-131">Group to which the owner's security ID belongs.</span></span>

<dt>

<span data-ttu-id="7cba7-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7cba7-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7cba7-133">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7cba7-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Group(
  [out] BSTR* pbstrGroupl
);
HRESULT put_Group(
  [in] BSTR bstrGroup
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7cba7-134">**GroupDefaulted**</span><span class="sxs-lookup"><span data-stu-id="7cba7-134">**GroupDefaulted**</span></span>
<span data-ttu-id="7cba7-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7cba7-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="7cba7-136">Flag del tipo BOOL che indica se i dati di gruppo sono derivati da un meccanismo predefinito, anziché essere forniti in modo esplicito dal provider originale del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="7cba7-136">A flag of the BOOL type that indicates if the group data is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span>

<dt>

<span data-ttu-id="7cba7-137">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7cba7-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7cba7-138">Tipo di dati di scripting: **\_ bool Variant**</span><span class="sxs-lookup"><span data-stu-id="7cba7-138">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GroupDefaultedY(
  [out] VARIANT_BOOL* fGroupDefaulted
);
HRESULT put_GroupDefaulted(
  [in] VARIANT_BOOL fGroupDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7cba7-139">**Proprietario**</span><span class="sxs-lookup"><span data-stu-id="7cba7-139">**Owner**</span></span>
<span data-ttu-id="7cba7-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7cba7-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="7cba7-141">Proprietario dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7cba7-141">Object owner.</span></span>

<dt>

<span data-ttu-id="7cba7-142">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7cba7-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7cba7-143">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7cba7-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Owner(
  [out] BSTR* pbstrOwnerl
);
HRESULT put_Owner(
  [in] BSTR bstrOwner
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7cba7-144">**OwnerDefaulted**</span><span class="sxs-lookup"><span data-stu-id="7cba7-144">**OwnerDefaulted**</span></span>
<span data-ttu-id="7cba7-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7cba7-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="7cba7-146">Flag del tipo BOOL che indica che i dati del proprietario sono derivati da un meccanismo predefinito, anziché essere forniti in modo esplicito dal provider originale del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="7cba7-146">A flag of the BOOL type that indicates that the owner data is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span>

<dt>

<span data-ttu-id="7cba7-147">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7cba7-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7cba7-148">Tipo di dati di scripting: **\_ bool Variant**</span><span class="sxs-lookup"><span data-stu-id="7cba7-148">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OwnerDefaulted(
  [out] VARIANT_BOOL* fOwnerDefaulted
);
HRESULT put_OwnerDefaulted(
  [in] VARIANT_BOOL fOwnerDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7cba7-149">**Revisione**</span><span class="sxs-lookup"><span data-stu-id="7cba7-149">**Revision**</span></span>
<span data-ttu-id="7cba7-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7cba7-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="7cba7-151">Livello di revisione del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="7cba7-151">Revision level of the security descriptor.</span></span> <span data-ttu-id="7cba7-152">Questo valore viene ricavato dalla struttura delle [**\_ \_ informazioni di revisione ACL**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) Win32.</span><span class="sxs-lookup"><span data-stu-id="7cba7-152">This value is taken from the Win32 [**ACL\_REVISION\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) structure.</span></span> <span data-ttu-id="7cba7-153">Tutte le voci ACE in un ACL devono avere lo stesso livello di revisione.</span><span class="sxs-lookup"><span data-stu-id="7cba7-153">All ACEs in an ACL must be at the same revision level.</span></span>

<dt>

<span data-ttu-id="7cba7-154">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7cba7-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7cba7-155">Tipo di dati di scripting: **Long**</span><span class="sxs-lookup"><span data-stu-id="7cba7-155">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Revision(
  [out] LONG* plRevision
);
HRESULT put_Revision(
  [in] LONG lRevision
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7cba7-156">**SaclDefaulted**</span><span class="sxs-lookup"><span data-stu-id="7cba7-156">**SaclDefaulted**</span></span>
<span data-ttu-id="7cba7-157"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7cba7-157"></dt> <dd> <dl></span></span>

<span data-ttu-id="7cba7-158">Flag del tipo BOOL che indica che l'elenco SACL è derivato da un meccanismo predefinito, anziché essere fornito in modo esplicito dal provider originale del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="7cba7-158">A flag of the BOOL type that indicates that the SACL is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span> <span data-ttu-id="7cba7-159">Questo flag può influire sul modo in cui il sistema gestisce l'elenco SACL, rispetto all'ereditarietà ACE.</span><span class="sxs-lookup"><span data-stu-id="7cba7-159">This flag can affect how the system handles the SACL, with respect to ACE inheritance.</span></span> <span data-ttu-id="7cba7-160">Questo flag viene ignorato dal sistema se \_ \_ non è impostato il flag se è presente.</span><span class="sxs-lookup"><span data-stu-id="7cba7-160">The system ignores this flag if the SE\_SACL\_PRESENT flag is not set.</span></span>

<dt>

<span data-ttu-id="7cba7-161">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7cba7-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7cba7-162">Tipo di dati di scripting: **\_ bool Variant**</span><span class="sxs-lookup"><span data-stu-id="7cba7-162">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SaclDefaulted(
  [out] VARIANT_BOOL* fSaclDefaulted
);
HRESULT put_SaclDefaulted(
  [in] VARIANT_BOOL fSaclDefaulted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7cba7-163">**SystemAcl**</span><span class="sxs-lookup"><span data-stu-id="7cba7-163">**SystemAcl**</span></span>
<span data-ttu-id="7cba7-164"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7cba7-164"></dt> <dd> <dl></span></span>

<span data-ttu-id="7cba7-165">Elenco di controllo di accesso di sistema usato per generare record di controllo per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7cba7-165">System access-control list used to generate audit records for the object.</span></span>

<dt>

<span data-ttu-id="7cba7-166">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="7cba7-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7cba7-167">Tipo di dati di scripting: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="7cba7-167">Scripting data type: **IDispatch**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SystemAcl(
  [out] IDispatch** ppIDispSACL
);
HRESULT put_SystemAcl(
  [in] IDispatch* pIDispSACL
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="7cba7-168">Esempio</span><span class="sxs-lookup"><span data-stu-id="7cba7-168">Examples</span></span>

<span data-ttu-id="7cba7-169">Nell'esempio di codice riportato di seguito viene illustrato come enumerare un descrittore di sicurezza esistente.</span><span class="sxs-lookup"><span data-stu-id="7cba7-169">The following code example shows how to enumerate an existing security descriptor.</span></span>


```VB
Dim ou As IADs
Dim sd As IADsSecurityDescriptor
Dim dacl As IADsAccessControlList
Dim sacl As IADsAccessControlList

On Error GoTo Cleanup 
 
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
Set sd = ou.Get("ntSecurityDescriptor")
Debug.Print sd.Owner
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision
Set dacl = sd.DiscretionaryAcl
Set sacl = sd.SystemAcl
' Add code to perform an operation with the Discretionary and System ACLs.

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
    Set sd = Nothing
    Set dacl = Nothing
    Set sacl = Nothing
```



## <a name="requirements"></a><span data-ttu-id="7cba7-170">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7cba7-170">Requirements</span></span>



| <span data-ttu-id="7cba7-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cba7-171">Requirement</span></span> | <span data-ttu-id="7cba7-172">Valore</span><span class="sxs-lookup"><span data-stu-id="7cba7-172">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cba7-173">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7cba7-173">Minimum supported client</span></span><br/> | <span data-ttu-id="7cba7-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7cba7-174">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="7cba7-175">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7cba7-175">Minimum supported server</span></span><br/> | <span data-ttu-id="7cba7-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7cba7-176">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="7cba7-177">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7cba7-177">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cba7-178"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cba7-178"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="7cba7-179">DLL</span><span class="sxs-lookup"><span data-stu-id="7cba7-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cba7-180"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cba7-180"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="7cba7-181">IID</span><span class="sxs-lookup"><span data-stu-id="7cba7-181">IID</span></span><br/>                      | <span data-ttu-id="7cba7-182">IID \_ IADsSecurityDescriptor è definito come B8C787CA-9BDD-11D0-852C-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="7cba7-182">IID\_IADsSecurityDescriptor is defined as B8C787CA-9BDD-11D0-852C-00C04FD8D503</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7cba7-183">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7cba7-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cba7-184">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="7cba7-184">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[<span data-ttu-id="7cba7-185">**IADsAccessControlEntry**</span><span class="sxs-lookup"><span data-stu-id="7cba7-185">**IADsAccessControlEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[<span data-ttu-id="7cba7-186">**IADsAccessControlList**</span><span class="sxs-lookup"><span data-stu-id="7cba7-186">**IADsAccessControlList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> </dl>

 

