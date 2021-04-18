---
description: Copia il contenuto di un archivio certificati aperto in una stringa codificata.
ms.assetid: 00697579-f929-42ed-8e8e-5c970fe4465b
title: Store. Export (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dbf4a2912cb62935447daa1589b6829c5a96488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331266"
---
# <a name="storeexport-method"></a><span data-ttu-id="ceafb-103">Store. Export (metodo)</span><span class="sxs-lookup"><span data-stu-id="ceafb-103">Store.Export method</span></span>

<span data-ttu-id="ceafb-104">\[Il metodo di **esportazione** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="ceafb-104">\[The **Export** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ceafb-105">Usare invece la [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="ceafb-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ceafb-106">Il metodo **Export** copia il contenuto di un [*archivio certificati*](../secgloss/c-gly.md) aperto in una stringa codificata.</span><span class="sxs-lookup"><span data-stu-id="ceafb-106">The **Export** method copies the contents of an open [*certificate store*](../secgloss/c-gly.md) to an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceafb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ceafb-107">Syntax</span></span>


```VB
Store.Export( _
  [ ByVal SaveAs ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ceafb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ceafb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceafb-109">*SaveAs* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ceafb-109">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ceafb-110">Valore dell'enumerazione [ \_ \_ Salva \_ come \_ tipo di archivio CAPICOM](capicom-store-save-as-type.md) che indica il formato per l'operazione di esportazione.</span><span class="sxs-lookup"><span data-stu-id="ceafb-110">A value of the [CAPICOM\_STORE\_SAVE\_AS\_TYPE](capicom-store-save-as-type.md) enumeration that indicates the format for the export operation.</span></span> <span data-ttu-id="ceafb-111">Il valore predefinito è capicot \_ Store \_ Salva \_ come \_ serializzato.</span><span class="sxs-lookup"><span data-stu-id="ceafb-111">The default value is CAPICOM\_STORE\_SAVE\_AS\_SERIALIZED.</span></span> <span data-ttu-id="ceafb-112">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ceafb-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="ceafb-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ceafb-113">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="ceafb-114">Significato</span><span class="sxs-lookup"><span data-stu-id="ceafb-114">Meaning</span></span>                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPICOM_STORE_SAVE_AS_SERIALIZED"></span><span id="capicom_store_save_as_serialized"></span><dl> <span data-ttu-id="ceafb-115"><dt>**\_Archivio CAPICOM \_ Salva \_ come \_ serializzato**</dt></span><span class="sxs-lookup"><span data-stu-id="ceafb-115"><dt>**CAPICOM\_STORE\_SAVE\_AS\_SERIALIZED**</dt></span></span> </dl> | <span data-ttu-id="ceafb-116">L'archivio viene salvato in formato serializzato.</span><span class="sxs-lookup"><span data-stu-id="ceafb-116">The store is saved in serialized format.</span></span><br/> |
| <span id="CAPICOM_STORE_SAVE_AS_PKCS7"></span><span id="capicom_store_save_as_pkcs7"></span><dl> <span data-ttu-id="ceafb-117"><dt>**\_Archivio CAPICOM \_ Salva \_ come \_ PKCS7**</dt></span><span class="sxs-lookup"><span data-stu-id="ceafb-117"><dt>**CAPICOM\_STORE\_SAVE\_AS\_PKCS7**</dt></span></span> </dl>                | <span data-ttu-id="ceafb-118">L'archivio viene salvato in \# formato PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="ceafb-118">The store is saved in PKCS \#7 format.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="ceafb-119">*EncodingType* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="ceafb-119">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ceafb-120">Valore dell'enumerazione del [ \_ \_ tipo di codifica CAPICOM](capicom-encoding-type.md) che indica il tipo di codifica dell'archivio esportato.</span><span class="sxs-lookup"><span data-stu-id="ceafb-120">A value of the [CAPICOM\_ENCODING\_TYPE](capicom-encoding-type.md) enumeration that indicates the encoding type of the exported store.</span></span> <span data-ttu-id="ceafb-121">Il valore predefinito è CAPICOM \_ Encode \_ base64.</span><span class="sxs-lookup"><span data-stu-id="ceafb-121">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="ceafb-122">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ceafb-122">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="ceafb-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ceafb-123">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="ceafb-124">Significato</span><span class="sxs-lookup"><span data-stu-id="ceafb-124">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="ceafb-125"><dt>**CAPICOM \_ Encode \_ any**</dt></span><span class="sxs-lookup"><span data-stu-id="ceafb-125"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="ceafb-126">Questo tipo di codifica viene utilizzato solo quando i dati di input hanno un tipo di codifica sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="ceafb-126">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="ceafb-127">Se questo valore viene usato per specificare il tipo di codifica dell'output, \_ \_ verrà invece usato CAPICOM Encode Base64.</span><span class="sxs-lookup"><span data-stu-id="ceafb-127">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="ceafb-128">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="ceafb-128">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="ceafb-129"><dt>**\_Codifica Base64 per CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ceafb-129"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="ceafb-130">I dati vengono salvati come stringa con codifica Base64.</span><span class="sxs-lookup"><span data-stu-id="ceafb-130">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="ceafb-131"><dt>**\_codificare il \_ file binario di CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="ceafb-131"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="ceafb-132">I dati vengono salvati come una sequenza binaria pura.</span><span class="sxs-lookup"><span data-stu-id="ceafb-132">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceafb-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ceafb-133">Return value</span></span>

<span data-ttu-id="ceafb-134">Questo metodo restituisce una stringa che contiene i certificati nell'archivio nel formato di codifica specificato.</span><span class="sxs-lookup"><span data-stu-id="ceafb-134">This method returns a string that contains the certificates in the store in the specified encoding form.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceafb-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ceafb-135">Requirements</span></span>



| <span data-ttu-id="ceafb-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="ceafb-136">Requirement</span></span> | <span data-ttu-id="ceafb-137">Valore</span><span class="sxs-lookup"><span data-stu-id="ceafb-137">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ceafb-138">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="ceafb-138">Redistributable</span></span><br/> | <span data-ttu-id="ceafb-139">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="ceafb-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ceafb-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ceafb-140">DLL</span></span><br/>             | <dl> <span data-ttu-id="ceafb-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ceafb-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ceafb-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ceafb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceafb-143">**Store**</span><span class="sxs-lookup"><span data-stu-id="ceafb-143">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="ceafb-144">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="ceafb-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
