---
title: Metodi di proprietà IADsNamespaces (IADs. h)
description: I metodi di proprietà dell'interfaccia IADsNamespaces ottengono e impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: fe959741-429e-480a-8111-3ebadaf55f77
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsNamespaces ADSI
topic_type:
- apiref
api_name:
- IADsNamespaces Property Methods
- IADsNamespaces.DefaultContainer
- IADsNamespaces.get_DefaultContainer
- IADsNamespaces.put_DefaultContainer
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b30467e931d7e8790f9a17542d5da2070525fe0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742695"
---
# <a name="iadsnamespaces-property-methods"></a><span data-ttu-id="10f05-105">Metodi di proprietà IADsNamespaces</span><span class="sxs-lookup"><span data-stu-id="10f05-105">IADsNamespaces Property Methods</span></span>

<span data-ttu-id="10f05-106">I metodi di proprietà dell'interfaccia [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) ottengono e impostano le proprietà descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="10f05-106">The [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) interface property methods get and set the properties described in the following table.</span></span> <span data-ttu-id="10f05-107">Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="10f05-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="10f05-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="10f05-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="10f05-109">**DefaultContainer**</span><span class="sxs-lookup"><span data-stu-id="10f05-109">**DefaultContainer**</span></span>
<span data-ttu-id="10f05-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="10f05-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="10f05-111">La proprietà **DefaultContainer** identifica un oggetto contenitore di base a cui è possibile associare e utilizzare come punto di partenza per l'esplorazione.</span><span class="sxs-lookup"><span data-stu-id="10f05-111">The **DefaultContainer** property identifies a base container object to which you can bind and use as a starting point when browsing.</span></span> <span data-ttu-id="10f05-112">Questi dati vengono archiviati e recuperati dal seguente valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="10f05-112">This data is stored and retrieved from the following registry value.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         ADs
            DefaultContainer
```

<span data-ttu-id="10f05-113">ADSI definisce la proprietà **DefaultContainer** per fornire un metodo rapido per ottenere un puntatore a un oggetto contenitore ADSI definito in precedenza.</span><span class="sxs-lookup"><span data-stu-id="10f05-113">ADSI defines the **DefaultContainer** property to provide a quick way of getting a pointer to a previously defined ADSI container object.</span></span>

<dt>

<span data-ttu-id="10f05-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="10f05-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10f05-115">Tipo di dati di scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="10f05-115">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultContainer(
  [out] BSTR* pbstrDefault
);
HRESULT put_DefaultContainer(
  [in] BSTR bstrDefault
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="10f05-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="10f05-116">Remarks</span></span>

<span data-ttu-id="10f05-117">I provider devono fornire questa proprietà per ogni singolo utente.</span><span class="sxs-lookup"><span data-stu-id="10f05-117">Providers must supply this property on a per-user basis.</span></span> <span data-ttu-id="10f05-118">Il contenitore predefinito viene impostato immediatamente dopo la chiamata di **IADsNamespaces::p UT \_ DefaultContainer**.</span><span class="sxs-lookup"><span data-stu-id="10f05-118">The default container is set immediately after the invocation of **IADsNamespaces::put\_DefaultContainer**.</span></span> <span data-ttu-id="10f05-119">La chiamata a [**IADs. seinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) non è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="10f05-119">Calling [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) is not required.</span></span> <span data-ttu-id="10f05-120">Infatti, l'oggetto Namespaces fornito dal sistema restituisce **E \_ NOTIMPL** per il metodo **IADs. seinfo** chiamato su questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="10f05-120">In fact, the system-supplied namespaces object returns **E\_NOTIMPL** for the **IADs.SetInfo** method called on this object.</span></span> <span data-ttu-id="10f05-121">Quando un contenitore è l'oggetto Namespaces, un'operazione di enumerazione restituisce sempre un elenco di oggetti spazio dei nomi specifici del provider.</span><span class="sxs-lookup"><span data-stu-id="10f05-121">When a container is the namespaces object, an enumeration operation always results in a list of provider-specific namespace objects.</span></span> <span data-ttu-id="10f05-122">Quando si usa [**IADsContainer. GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) per ottenere un oggetto spazio dei nomi, il parametro *bstrClass* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="10f05-122">When [**IADsContainer.GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) is used to obtain a namespace object, the *bstrClass* parameter is ignored.</span></span> <span data-ttu-id="10f05-123">Questo è dovuto al fatto che il contenitore, ovvero l'oggetto Namespaces, contiene un solo tipo di oggetto, ovvero oggetti spazio dei nomi specifici del provider.</span><span class="sxs-lookup"><span data-stu-id="10f05-123">This is because the container, that is, the namespaces object, contains only one type of object, namely, provider-specific namespace objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="10f05-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10f05-124">Requirements</span></span>



| <span data-ttu-id="10f05-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="10f05-125">Requirement</span></span> | <span data-ttu-id="10f05-126">Valore</span><span class="sxs-lookup"><span data-stu-id="10f05-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10f05-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10f05-127">Minimum supported client</span></span><br/> | <span data-ttu-id="10f05-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10f05-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10f05-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10f05-129">Minimum supported server</span></span><br/> | <span data-ttu-id="10f05-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10f05-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10f05-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10f05-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="10f05-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="10f05-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="10f05-133">DLL</span><span class="sxs-lookup"><span data-stu-id="10f05-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10f05-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10f05-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="10f05-135">IID</span><span class="sxs-lookup"><span data-stu-id="10f05-135">IID</span></span><br/>                      | <span data-ttu-id="10f05-136">IID \_ IADsNamespaces è definito come 28B96BA0-B330-11CF-A9AD-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="10f05-136">IID\_IADsNamespaces is defined as 28B96BA0-B330-11CF-A9AD-00AA006BC149</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="10f05-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10f05-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10f05-138">**IADsContainer. GetObject**</span><span class="sxs-lookup"><span data-stu-id="10f05-138">**IADsContainer.GetObject**</span></span>](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)
</dt> <dt>

[<span data-ttu-id="10f05-139">**IADsNamespaces**</span><span class="sxs-lookup"><span data-stu-id="10f05-139">**IADsNamespaces**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)
</dt> <dt>

[<span data-ttu-id="10f05-140">Metodi di proprietà dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="10f05-140">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





