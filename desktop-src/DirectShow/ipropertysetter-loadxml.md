---
description: Il metodo LoadXML carica i dati delle proprietà espressi in Extensible Markup Language (XML).
ms.assetid: cc67e7e0-a6e0-43d1-b35d-5d64caf24e6e
title: 'Metodo IPropertySetter:: LoadXML (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 65127d313309ca7d670a99c912531db0657a9b51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325476"
---
# <a name="ipropertysetterloadxml-method"></a><span data-ttu-id="c34e0-103">Metodo IPropertySetter:: LoadXML</span><span class="sxs-lookup"><span data-stu-id="c34e0-103">IPropertySetter::LoadXML method</span></span>

> [!Note]  
> <span data-ttu-id="c34e0-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c34e0-104">\[Deprecated.</span></span> <span data-ttu-id="c34e0-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c34e0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c34e0-106">Il `LoadXML` metodo carica i dati delle proprietà espressi in Extensible Markup Language (XML).</span><span class="sxs-lookup"><span data-stu-id="c34e0-106">The `LoadXML` method loads property data expressed in Extensible Markup Language (XML).</span></span>

## <a name="syntax"></a><span data-ttu-id="c34e0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c34e0-107">Syntax</span></span>


```C++
HRESULT LoadXML(
  [in] IUnknown *pxml
);
```



## <a name="parameters"></a><span data-ttu-id="c34e0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c34e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c34e0-109">*pXML* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c34e0-109">*pxml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c34e0-110">Puntatore all'interfaccia **IUnknown** di un elemento XML creato da Microsoft XML parser.</span><span class="sxs-lookup"><span data-stu-id="c34e0-110">Pointer to the **IUnknown** interface of an XML element created by the Microsoft XML parser.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c34e0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c34e0-111">Return value</span></span>

<span data-ttu-id="c34e0-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c34e0-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c34e0-113">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="c34e0-113">Possible values include the following.</span></span>



| <span data-ttu-id="c34e0-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c34e0-114">Return code</span></span>                                                                                                  | <span data-ttu-id="c34e0-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c34e0-115">Description</span></span>                     |
|--------------------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="c34e0-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="c34e0-116"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="c34e0-117">Nessun dato della proprietà.</span><span class="sxs-lookup"><span data-stu-id="c34e0-117">No property data.</span></span><br/>    |
| <dl> <span data-ttu-id="c34e0-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c34e0-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="c34e0-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c34e0-119">Success.</span></span><br/>             |
| <dl> <span data-ttu-id="c34e0-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="c34e0-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                | <span data-ttu-id="c34e0-121">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="c34e0-121">Insufficient memory.</span></span><br/> |
| <dl> <span data-ttu-id="c34e0-122"><dt>**\_formato file VFW E \_ non valido \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c34e0-122"><dt>**VFW\_E\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="c34e0-123">Formato non valido.</span><span class="sxs-lookup"><span data-stu-id="c34e0-123">Invalid format.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="c34e0-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="c34e0-124">Remarks</span></span>

<span data-ttu-id="c34e0-125">In genere, le applicazioni non dovranno utilizzare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="c34e0-125">Typically, applications will not need to use this method.</span></span> <span data-ttu-id="c34e0-126">DES lo usa internamente per caricare le proprietà dai file XTL.</span><span class="sxs-lookup"><span data-stu-id="c34e0-126">DES uses it internally to load properties from XTL files.</span></span>

<span data-ttu-id="c34e0-127">Per usare questo metodo, creare un oggetto **IXMLDocument** e usarlo per analizzare un file XML.</span><span class="sxs-lookup"><span data-stu-id="c34e0-127">To use this method, create an **IXMLDocument** object and use it to parse an XML file.</span></span> <span data-ttu-id="c34e0-128">Usare quindi l'oggetto **IXMLDocument** per recuperare gli oggetti **IXMLElement** .</span><span class="sxs-lookup"><span data-stu-id="c34e0-128">Then use the **IXMLDocument** object to retrieve **IXMLElement** objects.</span></span> <span data-ttu-id="c34e0-129">Se l'oggetto dispone di proprietà, è possibile passare il puntatore **IXMLElement** al metodo **LoadXml** .</span><span class="sxs-lookup"><span data-stu-id="c34e0-129">If the object has properties, you can pass the **IXMLElement** pointer to the **LoadXML** method.</span></span> <span data-ttu-id="c34e0-130">Il metodo carica le proprietà nel setter della proprietà.</span><span class="sxs-lookup"><span data-stu-id="c34e0-130">The method loads the properties into the property setter.</span></span>

> [!Note]  
> <span data-ttu-id="c34e0-131">Le interfacce **IXMLDocument** e **IXMLElement** sono implementate in Microsoft XML Core Services (MSXML) versione 1,0, ma non sono implementate nelle versioni più recenti di MSXML.</span><span class="sxs-lookup"><span data-stu-id="c34e0-131">The **IXMLDocument** and **IXMLElement** interfaces are implemented in Microsoft XML Core Services (MSXML) version 1.0, but are not implemented in more recent versions of MSXML.</span></span>

 

> [!Note]  
> <span data-ttu-id="c34e0-132">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="c34e0-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c34e0-133">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c34e0-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c34e0-134">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c34e0-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c34e0-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c34e0-135">Requirements</span></span>



| <span data-ttu-id="c34e0-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c34e0-136">Requirement</span></span> | <span data-ttu-id="c34e0-137">Valore</span><span class="sxs-lookup"><span data-stu-id="c34e0-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c34e0-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c34e0-138">Header</span></span><br/>  | <dl> <span data-ttu-id="c34e0-139"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c34e0-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c34e0-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="c34e0-140">Library</span></span><br/> | <dl> <span data-ttu-id="c34e0-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c34e0-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c34e0-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c34e0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c34e0-143">**Interfaccia IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="c34e0-143">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="c34e0-144">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="c34e0-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




