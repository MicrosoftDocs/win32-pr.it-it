---
description: Definisce i codici di errore restituiti da CAPICOM.
ms.assetid: e72b8290-b482-4629-8b87-5a15677865a6
title: Enumerazione CAPICOM_ERROR_CODE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ERROR_CODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: ccd4963c83f1ad7ce3bc686b7736ce47d699ce30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329228"
---
# <a name="capicom_error_code-enumeration"></a><span data-ttu-id="c1cf5-103">\_Enumerazione del codice di errore CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="c1cf5-103">CAPICOM\_ERROR\_CODE enumeration</span></span>

<span data-ttu-id="c1cf5-104">Il tipo di enumerazione del **\_ \_ codice di errore CAPICOM** definisce i codici di errore restituiti da CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-104">The **CAPICOM\_ERROR\_CODE** enumeration type defines error codes that are returned by CAPICOM.</span></span>

> [!Note]  
> <span data-ttu-id="c1cf5-105">Visual Basic errori di Scripting Edition restituiscono un valore **Err. Number** maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-105">Visual Basic Scripting Edition errors return an **Err.number** value greater than zero.</span></span> <span data-ttu-id="c1cf5-106">Per tali errori, i valori **Err. Description** forniscono informazioni sulla ragione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-106">For those errors, **Err.Description** values provide information about the cause of the error.</span></span> <span data-ttu-id="c1cf5-107">Oltre ai Visual Basic errori di Scripting Edition, gli errori di CAPICOM restituiscono i codici definiti dal **codice di \_ errore \_ di CAPICOM**.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-107">In addition to Visual Basic Scripting Edition errors, CAPICOM errors return the codes defined by **CAPICOM\_ERROR\_CODE**.</span></span>

 

## <a name="members"></a><span data-ttu-id="c1cf5-108">Membri</span><span class="sxs-lookup"><span data-stu-id="c1cf5-108">Members</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c1cf5-109">Membro</span><span class="sxs-lookup"><span data-stu-id="c1cf5-109">Member</span></span></th>
<th><span data-ttu-id="c1cf5-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1cf5-110">Description</span></span></th>
<th><span data-ttu-id="c1cf5-111">Valore</span><span class="sxs-lookup"><span data-stu-id="c1cf5-111">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c1cf5-112"><strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-112"><strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="c1cf5-113">È stato usato un tipo di codifica non valido.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-113">An encoding type that is not valid was used.</span></span><br/> <span data-ttu-id="c1cf5-114">Nell'elenco seguente sono riportati i tipi di codifica validi:</span><span class="sxs-lookup"><span data-stu-id="c1cf5-114">The following list shows the valid encoding types:</span></span>
<ul>
<li><span data-ttu-id="c1cf5-115">CAPICOM_ENCODE_ANY</span><span class="sxs-lookup"><span data-stu-id="c1cf5-115">CAPICOM_ENCODE_ANY</span></span></li>
<li><span data-ttu-id="c1cf5-116">CAPICOM_ENCODE_BASE64</span><span class="sxs-lookup"><span data-stu-id="c1cf5-116">CAPICOM_ENCODE_BASE64</span></span></li>
<li><span data-ttu-id="c1cf5-117">CAPICOM_ENCODE_BINARY</span><span class="sxs-lookup"><span data-stu-id="c1cf5-117">CAPICOM_ENCODE_BINARY</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="c1cf5-118">0x80880100</span><span class="sxs-lookup"><span data-stu-id="c1cf5-118">0x80880100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-119"><strong>CAPICOM_E_EKU_INVALID_OID</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-119"><strong>CAPICOM_E_EKU_INVALID_OID</strong></span></span></td>
<td><span data-ttu-id="c1cf5-120">Impossibile impostare la proprietà <a href="eku-oid.md"><strong>OID</strong></a> dell'oggetto <a href="eku.md"><strong>EKU</strong></a> perché la proprietà <a href="eku-name.md"><strong>Name</strong></a> non è impostata su CAPICOM_EKU_OTHER.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-120">The <a href="eku-oid.md"><strong>OID</strong></a> property of the <a href="eku.md"><strong>EKU</strong></a> object cannot be set because the <a href="eku-name.md"><strong>Name</strong></a> property is not set to CAPICOM_EKU_OTHER.</span></span><br/> <span data-ttu-id="c1cf5-121">Impostare la proprietà <a href="eku-name.md"><strong>Name</strong></a> su CAPICOM_EKU_OTHER prima di impostare la proprietà <a href="eku-oid.md"><strong>OID</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-121">Set the <a href="eku-name.md"><strong>Name</strong></a> property to CAPICOM_EKU_OTHER before setting the <a href="eku-oid.md"><strong>OID</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-122">0x80880200</span><span class="sxs-lookup"><span data-stu-id="c1cf5-122">0x80880200</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-123"><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-123"><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-124">La proprietà <a href="eku-oid.md"><strong>OID</strong></a> dell'oggetto <a href="eku.md"><strong>EKU</strong></a> non è stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-124">The <a href="eku-oid.md"><strong>OID</strong></a> property of the <a href="eku.md"><strong>EKU</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="c1cf5-125">Impostare la proprietà <a href="eku-name.md"><strong>Name</strong></a> su un valore diverso da CAPICOM_EKU_OTHER oppure impostare la proprietà <strong>Name</strong> su CAPICOM_EKU_OTHER e la proprietà <a href="eku-oid.md"><strong>OID</strong></a> su un valore.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-125">Either set the <a href="eku-name.md"><strong>Name</strong></a> property to anything other than CAPICOM_EKU_OTHER, or set the <strong>Name</strong> property to CAPICOM_EKU_OTHER and the <a href="eku-oid.md"><strong>OID</strong></a> property to a value.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-126">0x80880201</span><span class="sxs-lookup"><span data-stu-id="c1cf5-126">0x80880201</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-127"><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-127"><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-128">L'oggetto <a href="certificate.md"><strong>certificato</strong></a> non è stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-128">The <a href="certificate.md"><strong>Certificate</strong></a> object has not been initialized.</span></span><br/> <span data-ttu-id="c1cf5-129">Questo codice di errore viene in genere restituito quando viene creata un'istanza di un oggetto <a href="certificate.md"><strong>certificato</strong></a> , che non è associato a un certificato digitale.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-129">Usually, this error code is returned when a <a href="certificate.md"><strong>Certificate</strong></a> object is instantiated but not associated with a digital certificate.</span></span> <span data-ttu-id="c1cf5-130">Per associare l'oggetto a un certificato digitale, assegnarlo a un oggetto <strong>certificato</strong> esistente o chiamare il metodo <a href="certificate-import.md"><strong>Import</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-130">To associate the object with a digital certificate, either assign it to an existing <strong>Certificate</strong> object or call the <a href="certificate-import.md"><strong>Import</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-131">0x80880210</span><span class="sxs-lookup"><span data-stu-id="c1cf5-131">0x80880210</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-132"><strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-132"><strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong></span></span></td>
<td><span data-ttu-id="c1cf5-133">All'oggetto <a href="certificate.md"><strong>certificato</strong></a> non è associata una chiave privata.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-133">The <a href="certificate.md"><strong>Certificate</strong></a> object does not have an associated private key.</span></span><br/> <span data-ttu-id="c1cf5-134">Questo codice di errore viene restituito quando viene effettuato un tentativo di firmare i dati utilizzando la chiave privata del firmatario, ma l'oggetto <a href="certificate.md"><strong>certificato</strong></a> associato all'oggetto <a href="signer.md"><strong>firmatario</strong></a> non può essere utilizzato per l'operazione di firma.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-134">This error code is returned when an attempt is made to sign data using the signer's private key, but the <a href="certificate.md"><strong>Certificate</strong></a> object that is associated with the <a href="signer.md"><strong>Signer</strong></a> object cannot be used for the signing operation.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-135">0x80880211</span><span class="sxs-lookup"><span data-stu-id="c1cf5-135">0x80880211</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-136"><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-136"><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></span></span></td>
<td><span data-ttu-id="c1cf5-137">L'oggetto <a href="chain.md"><strong>Chain</strong></a> non è stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-137">The <a href="chain.md"><strong>Chain</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="c1cf5-138">Per inizializzare l'oggetto <a href="chain.md"><strong>Chain</strong></a> , chiamare il metodo di <a href="chain-build.md"><strong>compilazione</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-138">To initialize the <a href="chain.md"><strong>Chain</strong></a> object, call the <a href="chain-build.md"><strong>Build</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-139">0x80880220</span><span class="sxs-lookup"><span data-stu-id="c1cf5-139">0x80880220</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-140"><strong>CAPICOM_E_STORE_NOT_OPENED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-140"><strong>CAPICOM_E_STORE_NOT_OPENED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-141">L'oggetto <a href="store.md"><strong>Store</strong></a> non è stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-141">The <a href="store.md"><strong>Store</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="c1cf5-142">Per inizializzare l'oggetto <a href="store.md"><strong>Store</strong></a> , chiamare il metodo <a href="store-open.md"><strong>Open</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-142">To initialize the <a href="store.md"><strong>Store</strong></a> object, call the <a href="store-open.md"><strong>Open</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-143">0x80880230</span><span class="sxs-lookup"><span data-stu-id="c1cf5-143">0x80880230</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-144"><strong>CAPICOM_E_STORE_EMPTY</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-144"><strong>CAPICOM_E_STORE_EMPTY</strong></span></span></td>
<td><span data-ttu-id="c1cf5-145">L'oggetto <a href="store.md"><strong>Store</strong></a> non contiene oggetti <a href="certificate.md"><strong>Certificate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-145">The <a href="store.md"><strong>Store</strong></a> object does not contain any <a href="certificate.md"><strong>Certificate</strong></a> objects.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-146">0x80880231</span><span class="sxs-lookup"><span data-stu-id="c1cf5-146">0x80880231</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-147"><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-147"><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></span></span></td>
<td><span data-ttu-id="c1cf5-148">Il parametro <em>OpenMode</em> del metodo <a href="store-open.md"><strong>Store. Open</strong></a> non contiene un valore valido di CAPICOM_STORE_OPEN_MODE.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-148">The <em>OpenMode</em> parameter of the <a href="store-open.md"><strong>Store.Open</strong></a> method does not contain a valid value of CAPICOM_STORE_OPEN_MODE.</span></span><br/> <span data-ttu-id="c1cf5-149">L'elenco seguente mostra i valori validi di CAPICOM_STORE_OPEN_MODE:</span><span class="sxs-lookup"><span data-stu-id="c1cf5-149">The following list shows the valid values of CAPICOM_STORE_OPEN_MODE:</span></span>
<ul>
<li><span data-ttu-id="c1cf5-150">CAPICOM_STORE_OPEN_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="c1cf5-150">CAPICOM_STORE_OPEN_READ_ONLY</span></span></li>
<li><span data-ttu-id="c1cf5-151">CAPICOM_STORE_OPEN_READ_WRITE</span><span class="sxs-lookup"><span data-stu-id="c1cf5-151">CAPICOM_STORE_OPEN_READ_WRITE</span></span></li>
<li><span data-ttu-id="c1cf5-152">CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="c1cf5-152">CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</span></span></li>
<li><span data-ttu-id="c1cf5-153">CAPICOM_STORE_OPEN_EXISTING_ONLY</span><span class="sxs-lookup"><span data-stu-id="c1cf5-153">CAPICOM_STORE_OPEN_EXISTING_ONLY</span></span></li>
<li><span data-ttu-id="c1cf5-154">CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</span><span class="sxs-lookup"><span data-stu-id="c1cf5-154">CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="c1cf5-155">0x80880232</span><span class="sxs-lookup"><span data-stu-id="c1cf5-155">0x80880232</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-156"><strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-156"><strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong></span></span></td>
<td><span data-ttu-id="c1cf5-157">Il valore di <em>SaveAs</em> passato al metodo <a href="store-export.md"><strong>Export</strong></a> dell'oggetto <a href="store.md"><strong>Store</strong></a> non è valido.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-157">The <em>SaveAs</em> value passed to the <a href="store-export.md"><strong>Export</strong></a> method of the <a href="store.md"><strong>Store</strong></a> object was not valid.</span></span> <br/> <span data-ttu-id="c1cf5-158">Nell'elenco seguente sono riportati i valori di <em>SaveAs</em> validi:</span><span class="sxs-lookup"><span data-stu-id="c1cf5-158">The following list shows the valid <em>SaveAs</em> values:</span></span>
<ul>
<li><span data-ttu-id="c1cf5-159">CAPICOM_STORE_SAVE_AS_SERIALIZED</span><span class="sxs-lookup"><span data-stu-id="c1cf5-159">CAPICOM_STORE_SAVE_AS_SERIALIZED</span></span></li>
<li><span data-ttu-id="c1cf5-160">CAPICOM_STORE_SAVE_AS_PKCS7</span><span class="sxs-lookup"><span data-stu-id="c1cf5-160">CAPICOM_STORE_SAVE_AS_PKCS7</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="c1cf5-161">0x80880233</span><span class="sxs-lookup"><span data-stu-id="c1cf5-161">0x80880233</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-162"><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-162"><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-163">La proprietà <a href="attribute-name.md"><strong>Name</strong></a> dell'oggetto <a href="attribute.md"><strong>attribute</strong></a> non è stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-163">The <a href="attribute-name.md"><strong>Name</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="c1cf5-164">Impostare la proprietà <a href="attribute-name.md"><strong>Name</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-164">Set the <a href="attribute-name.md"><strong>Name</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-165">0x80880240</span><span class="sxs-lookup"><span data-stu-id="c1cf5-165">0x80880240</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-166"><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-166"><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-167">La proprietà <a href="attribute-value.md"><strong>value</strong></a> dell'oggetto <a href="attribute.md"><strong>attribute</strong></a> non è stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-167">The <a href="attribute-value.md"><strong>Value</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="c1cf5-168">Impostare la proprietà <a href="attribute-value.md"><strong>value</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-168">Set the <a href="attribute-value.md"><strong>Value</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-169">0x80880241</span><span class="sxs-lookup"><span data-stu-id="c1cf5-169">0x80880241</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-170"><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-170"><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></span></span></td>
<td><span data-ttu-id="c1cf5-171">La proprietà <a href="attribute-name.md"><strong>Name</strong></a> dell'oggetto <a href="attribute.md"><strong>attributo</strong></a> non è valida.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-171">The <a href="attribute-name.md"><strong>Name</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="c1cf5-172">Nell'elenco seguente sono riportati i nomi di attributo validi:</span><span class="sxs-lookup"><span data-stu-id="c1cf5-172">The following list shows the valid attribute names:</span></span>
<ul>
<li><span data-ttu-id="c1cf5-173">CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</span><span class="sxs-lookup"><span data-stu-id="c1cf5-173">CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</span></span></li>
<li><span data-ttu-id="c1cf5-174">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</span><span class="sxs-lookup"><span data-stu-id="c1cf5-174">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</span></span></li>
<li><span data-ttu-id="c1cf5-175">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c1cf5-175">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="c1cf5-176">0x80880242</span><span class="sxs-lookup"><span data-stu-id="c1cf5-176">0x80880242</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-177"><strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-177"><strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong></span></span></td>
<td><span data-ttu-id="c1cf5-178">La proprietà <a href="attribute-value.md"><strong>value</strong></a> dell'oggetto <a href="attribute.md"><strong>attribute</strong></a> non è valida perché il tipo di dati non corrisponde al tipo di dati indicato dalla proprietà <strong>Name</strong> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-178">The <a href="attribute-value.md"><strong>Value</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object is not valid because the data type does not match the data type indicated by the <strong>Name</strong> property.</span></span> <br/> <span data-ttu-id="c1cf5-179">Se, ad esempio, la proprietà <a href="attribute-value.md"><strong>Name</strong></a> è impostata su CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, il tipo di dati deve essere <strong>date</strong>.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-179">For example, if the <a href="attribute-value.md"><strong>Name</strong></a> property is set to CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, the data type must be <strong>DATE</strong>.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-180">0x80880243</span><span class="sxs-lookup"><span data-stu-id="c1cf5-180">0x80880243</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-181"><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-181"><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-182">L'oggetto <a href="signer.md"><strong>firmatario</strong></a> non è stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-182">The <a href="signer.md"><strong>Signer</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="c1cf5-183">Per inizializzare l'oggetto <a href="signer.md"><strong>firmatario</strong></a> , impostare la proprietà <a href="signer-certificate.md"><strong>Certificate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-183">To initialize the <a href="signer.md"><strong>Signer</strong></a> object, set the <a href="signer-certificate.md"><strong>Certificate</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-184">0x80880250</span><span class="sxs-lookup"><span data-stu-id="c1cf5-184">0x80880250</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-185"><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-185"><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></span></span></td>
<td><span data-ttu-id="c1cf5-186">Impossibile trovare il firmatario nell'oggetto <a href="signeddata.md"><strong>SignedData</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-186">The signer cannot be found in the <a href="signeddata.md"><strong>SignedData</strong></a> object.</span></span> <br/> <span data-ttu-id="c1cf5-187">In genere, questa operazione non viene eseguita con un oggetto <a href="signeddata.md"><strong>SignedData</strong></a> creato da CAPICOM; Tuttavia, se l'oggetto <strong>SignedData</strong> è stato creato da un prodotto di terze parti, il certificato del firmatario potrebbe non essere incluso nella struttura di #7 Pkcs.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-187">Usually, this does not happen with a <a href="signeddata.md"><strong>SignedData</strong></a> object that was created by CAPICOM; however, if the <strong>SignedData</strong> object was created by a third-party product, the signer's certificate may not be included in the PKCS #7 structure.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-188">0x80880251</span><span class="sxs-lookup"><span data-stu-id="c1cf5-188">0x80880251</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-189"><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-189"><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></span></span></td>
<td><span data-ttu-id="c1cf5-190">Impossibile trovare un oggetto <a href="chain.md"><strong>Chain</strong></a> nell'oggetto <a href="signer.md"><strong>firmatario</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-190">A <a href="chain.md"><strong>Chain</strong></a> object cannot be found in the <a href="signer.md"><strong>Signer</strong></a> object.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-191">0x80880252//v 2.0</span><span class="sxs-lookup"><span data-stu-id="c1cf5-191">0x80880252 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-192"><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-192"><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></span></span></td>
<td><span data-ttu-id="c1cf5-193">Viene effettuato un tentativo di utilizzare il firmatario in modo non valido.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-193">An attempt is made to use the signer in a way that is not valid.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-194">//V2.0 0x80880253</span><span class="sxs-lookup"><span data-stu-id="c1cf5-194">0x80880253 //v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-195"><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-195"><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-196">L'oggetto <a href="signeddata.md"><strong>SignedData</strong></a> non è stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-196">The <a href="signeddata.md"><strong>SignedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="c1cf5-197">Per inizializzare l'oggetto <a href="signeddata.md"><strong>SignedData</strong></a> , impostare la proprietà <a href="signeddata-content.md"><strong>Content</strong></a> o chiamare il metodo <a href="signeddata-verify.md"><strong>Verify</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-197">To initialize the <a href="signeddata.md"><strong>SignedData</strong></a> object, set the <a href="signeddata-content.md"><strong>Content</strong></a> property or call the <a href="signeddata-verify.md"><strong>Verify</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-198">0x80880260</span><span class="sxs-lookup"><span data-stu-id="c1cf5-198">0x80880260</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-199"><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-199"><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="c1cf5-200">L'oggetto <a href="signeddata.md"><strong>SignedData</strong></a> contiene un tipo non valido.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-200">The <a href="signeddata.md"><strong>SignedData</strong></a> object contains a type that is not valid.</span></span> <br/> <span data-ttu-id="c1cf5-201">In genere, ciò si verifica quando viene effettuato un tentativo di verificare un messaggio in busta con un oggetto <a href="signeddata.md"><strong>SignedData</strong></a> o viceversa.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-201">Usually, this happens when an attempt is made to verify an enveloped message with a <a href="signeddata.md"><strong>SignedData</strong></a> object or vice versa.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-202">0x80880261</span><span class="sxs-lookup"><span data-stu-id="c1cf5-202">0x80880261</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-203"><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-203"><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-204">L'oggetto <a href="signeddata.md"><strong>SignedData</strong></a> non è stato firmato.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-204">The <a href="signeddata.md"><strong>SignedData</strong></a> object has not been signed.</span></span> <br/> <span data-ttu-id="c1cf5-205">Per firmare l'oggetto <a href="signeddata.md"><strong>SignedData</strong></a> , chiamare il metodo <a href="signeddata-sign.md"><strong>Sign</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-205">To sign the <a href="signeddata.md"><strong>SignedData</strong></a> object, call the <a href="signeddata-sign.md"><strong>Sign</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-206">0x80880262</span><span class="sxs-lookup"><span data-stu-id="c1cf5-206">0x80880262</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-207"><strong>CAPICOM_E_INVALID_ALGORITHM</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-207"><strong>CAPICOM_E_INVALID_ALGORITHM</strong></span></span></td>
<td><span data-ttu-id="c1cf5-208">Il valore dell'algoritmo per la proprietà <a href="algorithm-name.md"><strong>Name</strong></a> dell'oggetto <a href="algorithm.md"><strong>Algorithm</strong></a> non è valido.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-208">The algorithm value for the <a href="algorithm-name.md"><strong>Name</strong></a> property of the <a href="algorithm.md"><strong>Algorithm</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="c1cf5-209">Nell'elenco seguente vengono illustrati i valori di algoritmo validi per la proprietà <a href="algorithm-name.md"><strong>Name</strong></a> :</span><span class="sxs-lookup"><span data-stu-id="c1cf5-209">The following list shows the valid algorithm values for the <a href="algorithm-name.md"><strong>Name</strong></a> property:</span></span>
<ul>
<li><span data-ttu-id="c1cf5-210">CAPICOM_ENCRYPTION_ALGORITHM_RC2</span><span class="sxs-lookup"><span data-stu-id="c1cf5-210">CAPICOM_ENCRYPTION_ALGORITHM_RC2</span></span></li>
<li><span data-ttu-id="c1cf5-211">CAPICOM_ENCRYPTION_ALGORITHM_RC4</span><span class="sxs-lookup"><span data-stu-id="c1cf5-211">CAPICOM_ENCRYPTION_ALGORITHM_RC4</span></span></li>
<li><span data-ttu-id="c1cf5-212">CAPICOM_ENCRYPTION_ALGORITHM_DES</span><span class="sxs-lookup"><span data-stu-id="c1cf5-212">CAPICOM_ENCRYPTION_ALGORITHM_DES</span></span></li>
<li><span data-ttu-id="c1cf5-213">CAPICOM_ENCRYPTION_ALGORITHM_3DES</span><span class="sxs-lookup"><span data-stu-id="c1cf5-213">CAPICOM_ENCRYPTION_ALGORITHM_3DES</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="c1cf5-214">0x80880270</span><span class="sxs-lookup"><span data-stu-id="c1cf5-214">0x80880270</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-215"><strong>CAPICOM_E_INVALID_KEY_LENGTH</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-215"><strong>CAPICOM_E_INVALID_KEY_LENGTH</strong></span></span></td>
<td><span data-ttu-id="c1cf5-216">Il valore della lunghezza della chiave per la proprietà della <a href="algorithm-keylength.md"><strong>lunghezza</strong></a> della chiave dell'oggetto <a href="algorithm.md"><strong>Algorithm</strong></a> non è valido.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-216">The key length value for the <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> property of the <a href="algorithm.md"><strong>Algorithm</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="c1cf5-217">Nell'elenco seguente sono riportati i valori validi per la lunghezza della chiave per la proprietà di <a href="algorithm-keylength.md"><strong>lunghezza</strong></a> della chiave:</span><span class="sxs-lookup"><span data-stu-id="c1cf5-217">The following list shows the valid key length values for the <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> property:</span></span>
<ul>
<li><span data-ttu-id="c1cf5-218">CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</span><span class="sxs-lookup"><span data-stu-id="c1cf5-218">CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</span></span></li>
<li><span data-ttu-id="c1cf5-219">CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</span><span class="sxs-lookup"><span data-stu-id="c1cf5-219">CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</span></span></li>
<li><span data-ttu-id="c1cf5-220">CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</span><span class="sxs-lookup"><span data-stu-id="c1cf5-220">CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</span></span></li>
<li><span data-ttu-id="c1cf5-221">CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</span><span class="sxs-lookup"><span data-stu-id="c1cf5-221">CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="c1cf5-222">0x80880271</span><span class="sxs-lookup"><span data-stu-id="c1cf5-222">0x80880271</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-223"><strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-223"><strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-224">L'oggetto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> non è stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-224">The <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="c1cf5-225">Per inizializzare l'oggetto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> , impostare la proprietà <a href="envelopeddata-content.md"><strong>Content</strong></a> o chiamare il metodo <a href="envelopeddata-decrypt.md"><strong>Decrypt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-225">To initialize the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object, either set the <a href="envelopeddata-content.md"><strong>Content</strong></a> property or call the <a href="envelopeddata-decrypt.md"><strong>Decrypt</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-226">0x80880280</span><span class="sxs-lookup"><span data-stu-id="c1cf5-226">0x80880280</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-227"><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-227"><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="c1cf5-228">L'oggetto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> contiene un tipo non valido.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-228">The <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object contains a type that is not valid.</span></span> <br/> <span data-ttu-id="c1cf5-229">In genere, ciò si verifica quando viene effettuato un tentativo di verificare un messaggio firmato con un oggetto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> o viceversa.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-229">Usually, this happens when an attempt is made to verify a signed message with an <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object or vice versa.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-230">0x80880281</span><span class="sxs-lookup"><span data-stu-id="c1cf5-230">0x80880281</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-231"><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-231"><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></span></span></td>
<td><span data-ttu-id="c1cf5-232">Non è stato specificato alcun destinatario nell'oggetto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> quando viene chiamato il metodo <a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a> di un oggetto <strong>EnvelopedData</strong> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-232">There is no recipient specified in the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object when the <a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a> method of an <strong>EnvelopedData</strong> object is called.</span></span> <br/> <span data-ttu-id="c1cf5-233">Per aggiungere un destinatario, chiamare il metodo <a href="recipients-add.md"><strong>Recipients. Add</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-233">To add a recipient, call the <a href="recipients-add.md"><strong>Recipients.Add</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-234">0x80880282</span><span class="sxs-lookup"><span data-stu-id="c1cf5-234">0x80880282</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-235"><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-235"><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></span></span></td>
<td><span data-ttu-id="c1cf5-236">Impossibile trovare il destinatario nell'oggetto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-236">The recipient cannot be found in the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object.</span></span> <br/> <span data-ttu-id="c1cf5-237">In genere, questa operazione non viene eseguita con un oggetto <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> creato da CAPICOM; Tuttavia, se l'oggetto <strong>EnvelopedData</strong> è stato creato da un prodotto di terze parti, il certificato del destinatario potrebbe non essere incluso nella struttura di #7 Pkcs.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-237">Usually, this does not happen with an <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object that was created by CAPICOM; however, if the <strong>EnvelopedData</strong> object was created by a third-party product, the recipient's certificate may not be included in the PKCS #7 structure.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-238">0x80880283</span><span class="sxs-lookup"><span data-stu-id="c1cf5-238">0x80880283</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-239"><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-239"><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-240">L'oggetto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> non è stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-240">The <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="c1cf5-241">Per inizializzare l'oggetto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> , impostare la proprietà <a href="encrypteddata-content.md"><strong>Content</strong></a> o chiamare il metodo <a href="encrypteddata-decrypt.md"><strong>Decrypt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-241">To initialize the <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object, either set the <a href="encrypteddata-content.md"><strong>Content</strong></a> property or call the <a href="encrypteddata-decrypt.md"><strong>Decrypt</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-242">0x80880290</span><span class="sxs-lookup"><span data-stu-id="c1cf5-242">0x80880290</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-243"><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-243"><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="c1cf5-244">L'oggetto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> non è un tipo valido.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-244">The <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object is not a valid type.</span></span> <br/> <span data-ttu-id="c1cf5-245">In genere, ciò significa che i dati sono danneggiati.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-245">Usually, this means the data is corrupted.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-246">0x80880291</span><span class="sxs-lookup"><span data-stu-id="c1cf5-246">0x80880291</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-247"><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-247"><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></span></span></td>
<td><span data-ttu-id="c1cf5-248">Il segreto di un oggetto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> non è stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-248">The secret of an <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="c1cf5-249">Per inizializzare il segreto di un oggetto <a href="encrypteddata.md"><strong>EncryptedData</strong></a> , chiamare il metodo <a href="encrypteddata-setsecret.md"><strong>sesecret</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-249">To initialize the secret of an <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object, call the <a href="encrypteddata-setsecret.md"><strong>SetSecret</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-250">0x80880292</span><span class="sxs-lookup"><span data-stu-id="c1cf5-250">0x80880292</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-251"><strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-251"><strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-252">L'oggetto <a href="privatekey.md"><strong>PrivateKey</strong></a> non è stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-252">The <a href="privatekey.md"><strong>PrivateKey</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-253">0x80880300//v 2.0</span><span class="sxs-lookup"><span data-stu-id="c1cf5-253">0x80880300 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-254"><strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-254"><strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong></span></span></td>
<td><span data-ttu-id="c1cf5-255">Impossibile esportare l'oggetto <a href="privatekey.md"><strong>PrivateKey</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-255">The <a href="privatekey.md"><strong>PrivateKey</strong></a> object cannot be exported.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-256">0x80880301//v 2.0</span><span class="sxs-lookup"><span data-stu-id="c1cf5-256">0x80880301 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-257"><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-257"><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-258">L'oggetto <a href="encodeddata.md"><strong>EncodedData</strong></a> non è stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-258">The <a href="encodeddata.md"><strong>EncodedData</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-259">0x80880320//v 2.0</span><span class="sxs-lookup"><span data-stu-id="c1cf5-259">0x80880320 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-260"><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-260"><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-261">L'oggetto di <a href="extension.md"><strong>estensione</strong></a> non è stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-261">The <a href="extension.md"><strong>Extension</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-262">0x80880330//v 2.0</span><span class="sxs-lookup"><span data-stu-id="c1cf5-262">0x80880330 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-263"><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-263"><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-264">La proprietà <a href="extendedproperty-propid.md"><strong>propid</strong></a> dell'oggetto <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> non è stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-264">The <a href="extendedproperty-propid.md"><strong>PropID</strong></a> property of the <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-265">0x80880340//v 2.0</span><span class="sxs-lookup"><span data-stu-id="c1cf5-265">0x80880340 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-266"><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-266"><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="c1cf5-267">Il parametro <em>FindType</em> del metodo <a href="certificates-find.md"><strong>Certificates. Find</strong></a> non è un valore dell'enumerazione <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-267">The <em>FindType</em> parameter of the <a href="certificates-find.md"><strong>Certificates.Find</strong></a> method is not a value of the <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> enumeration.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-268">0x80880350//v 2.0</span><span class="sxs-lookup"><span data-stu-id="c1cf5-268">0x80880350 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-269"><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-269"><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></span></span></td>
<td><span data-ttu-id="c1cf5-270">Il criterio predefinito specificato per l'operazione di ricerca non è valido.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-270">The specified predefined policy for the find operation is not valid.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-271">0x80880351//v 2.0</span><span class="sxs-lookup"><span data-stu-id="c1cf5-271">0x80880351 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-272"><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-272"><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-273">L'oggetto <a href="signedcode.md"><strong>SignedCode</strong></a> non è stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-273">The <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-274">0x80880360//v 2.0</span><span class="sxs-lookup"><span data-stu-id="c1cf5-274">0x80880360 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-275"><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-275"><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-276">L'oggetto <a href="signedcode.md"><strong>SignedCode</strong></a> non è stato firmato.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-276">The <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been signed.</span></span><br/> <span data-ttu-id="c1cf5-277">Per firmare l'oggetto <a href="signedcode.md"><strong>SignedCode</strong></a> , chiamare il metodo <a href="signedcode-sign.md"><strong>Sign</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-277">To sign the <a href="signedcode.md"><strong>SignedCode</strong></a> object, call the <a href="signedcode-sign.md"><strong>Sign</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-278">0x80880361//v 2.0</span><span class="sxs-lookup"><span data-stu-id="c1cf5-278">0x80880361 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-279"><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-279"><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-280">La proprietà <a href="signedcode-description.md"><strong>Description</strong></a> dell'oggetto <a href="signedcode.md"><strong>SignedCode</strong></a> non è stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-280">The <a href="signedcode-description.md"><strong>Description</strong></a> property of the <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-281">0x80880362//v 2.0</span><span class="sxs-lookup"><span data-stu-id="c1cf5-281">0x80880362 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-282"><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-282"><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-283">La proprietà <a href="signedcode-descriptionurl.md"><strong>DescriptionURL</strong></a> dell'oggetto <a href="signedcode.md"><strong>SignedCode</strong></a> non è stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-283">The <a href="signedcode-descriptionurl.md"><strong>DescriptionURL</strong></a> property of the <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-284">0x80880363//v 2.0</span><span class="sxs-lookup"><span data-stu-id="c1cf5-284">0x80880363 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-285"><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-285"><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></span></span></td>
<td><span data-ttu-id="c1cf5-286">Il parametro <em>URL</em> del metodo <a href="signedcode-timestamp.md"><strong>SignedCode. timestamp</strong></a> non è valido.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-286">The <em>URL</em> parameter of the <a href="signedcode-timestamp.md"><strong>SignedCode.Timestamp</strong></a> method is not valid.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-287">0x80880364//v 2.0</span><span class="sxs-lookup"><span data-stu-id="c1cf5-287">0x80880364 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-288"><strong>CAPICOM_E_HASH_NO_DATA</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-288"><strong>CAPICOM_E_HASH_NO_DATA</strong></span></span></td>
<td><span data-ttu-id="c1cf5-289">L'oggetto <a href="hasheddata.md"><strong>HashedData</strong></a> non contiene dati.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-289">The <a href="hasheddata.md"><strong>HashedData</strong></a> object does not contain any data.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-290">0x80880370//v 2.0</span><span class="sxs-lookup"><span data-stu-id="c1cf5-290">0x80880370 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-291"><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-291"><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></span></span></td>
<td><span data-ttu-id="c1cf5-292">Il tipo di conversione non è valido.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-292">The convert type is not valid.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-293">0x80880380//v 2.0</span><span class="sxs-lookup"><span data-stu-id="c1cf5-293">0x80880380 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-294"><strong>CAPICOM_E_NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-294"><strong>CAPICOM_E_NOT_SUPPORTED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-295">L'operazione richiesta non è supportata nella piattaforma corrente.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-295">The requested operation is not supported in the current platform.</span></span> <br/></td>
<td><span data-ttu-id="c1cf5-296">0x80880900</span><span class="sxs-lookup"><span data-stu-id="c1cf5-296">0x80880900</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-297"><strong>CAPICOM_E_UI_DISABLED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-297"><strong>CAPICOM_E_UI_DISABLED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-298">Quando si esegue la firma, la proprietà <a href="signer-certificate.md"><strong>Certificate</strong></a> dell'oggetto <a href="signer.md"><strong>firmatario</strong></a> non è stata impostata, ma la richiesta del certificato utente è stata disabilitata.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-298">When signing, the <a href="signer-certificate.md"><strong>Certificate</strong></a> property of the <a href="signer.md"><strong>Signer</strong></a> object has not been set, but the prompt for the user certificate has been disabled.</span></span> <br/> <span data-ttu-id="c1cf5-299">Abilitare la richiesta impostando la proprietà <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> dell'oggetto <a href="settings.md"><strong>Settings</strong></a> oppure impostare la proprietà <a href="signer-certificate.md"><strong>Certificate</strong></a> dell'oggetto <a href="signer.md"><strong>firmatario</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c1cf5-299">Either enable the prompt by setting the <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> property of the <a href="settings.md"><strong>Settings</strong></a> object, or set the <a href="signer-certificate.md"><strong>Certificate</strong></a> property of the <a href="signer.md"><strong>Signer</strong></a> object.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-300">0x80880901</span><span class="sxs-lookup"><span data-stu-id="c1cf5-300">0x80880901</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-301"><strong>CAPICOM_E_CANCELLED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-301"><strong>CAPICOM_E_CANCELLED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-302">L'operazione è stata annullata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-302">The operation has been canceled by the user.</span></span> <br/> <span data-ttu-id="c1cf5-303">Ciò si verifica quando all'utente viene richiesta l'autorizzazione per eseguire una determinata operazione, ad esempio l'accesso alla chiave privata, e l'utente annulla l'operazione.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-303">This happens when the user is prompted for permission to carry out a certain operation, such as accessing the private key, and the user cancels the operation.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-304">0x80880902</span><span class="sxs-lookup"><span data-stu-id="c1cf5-304">0x80880902</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-305"><strong>CAPICOM_E_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-305"><strong>CAPICOM_E_NOT_ALLOWED</strong></span></span></td>
<td><span data-ttu-id="c1cf5-306">Operazione tentata non consentita.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-306">The attempted operation is not allowed.</span></span><br/> <span data-ttu-id="c1cf5-307">La modifica della proprietà <a href="extendedproperty-propid.md"><strong>propid</strong></a> di un oggetto <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> , ad esempio, non è consentita se l'oggetto è associato a un certificato.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-307">For example, changing the <a href="extendedproperty-propid.md"><strong>PropID</strong></a> property of an <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> object is not allowed if the object is attached to a certificate.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-308">0x80880903//v 2.0</span><span class="sxs-lookup"><span data-stu-id="c1cf5-308">0x80880903 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-309"><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-309"><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></span></span></td>
<td><span data-ttu-id="c1cf5-310">Il capicot ha esaurito una risorsa.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-310">CAPICOM has run out of a resource.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-311">0x80880904//v 2.0</span><span class="sxs-lookup"><span data-stu-id="c1cf5-311">0x80880904 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1cf5-312"><strong>CAPICOM_E_INTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-312"><strong>CAPICOM_E_INTERNAL</strong></span></span></td>
<td><span data-ttu-id="c1cf5-313">Si è verificato un errore interno.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-313">An internal error has occurred.</span></span> <br/> <span data-ttu-id="c1cf5-314">Per assistenza, contattare il supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-314">Contact Microsoft Technical Support for assistance.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-315">0x80880911</span><span class="sxs-lookup"><span data-stu-id="c1cf5-315">0x80880911</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1cf5-316"><strong>CAPICOM_E_UNKNOWN</strong></span><span class="sxs-lookup"><span data-stu-id="c1cf5-316"><strong>CAPICOM_E_UNKNOWN</strong></span></span></td>
<td><span data-ttu-id="c1cf5-317">Si è verificato un errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-317">An unknown error has occurred.</span></span> <br/> <span data-ttu-id="c1cf5-318">Raccogliere quante più informazioni possibile e contattare il fornitore.</span><span class="sxs-lookup"><span data-stu-id="c1cf5-318">Collect as much information as possible, and contact your vendor.</span></span><br/></td>
<td><span data-ttu-id="c1cf5-319">0x80880999</span><span class="sxs-lookup"><span data-stu-id="c1cf5-319">0x80880999</span></span></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="c1cf5-320">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1cf5-320">Requirements</span></span>



| <span data-ttu-id="c1cf5-321">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1cf5-321">Requirement</span></span> | <span data-ttu-id="c1cf5-322">Valore</span><span class="sxs-lookup"><span data-stu-id="c1cf5-322">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c1cf5-323">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="c1cf5-323">Redistributable</span></span><br/> | <span data-ttu-id="c1cf5-324">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="c1cf5-324">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="c1cf5-325">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1cf5-325">Header</span></span><br/>          | <dl> <span data-ttu-id="c1cf5-326"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1cf5-326"><dt>Capicom.h</dt></span></span> </dl> |



 

 




