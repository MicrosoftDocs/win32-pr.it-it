---
description: Copia un certificato in una stringa codificata.
ms.assetid: bae7fb57-6b44-4aac-a635-b5b82de1f68d
title: 'Metodo ICertificate2:: Export'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Export
- ICertificate2.Export
- ICertificate.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aee48fe3d9ba56cba90c9645a3fb9752e3367a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332156"
---
# <a name="icertificate2export-method"></a><span data-ttu-id="baeaa-103">Metodo ICertificate2:: Export</span><span class="sxs-lookup"><span data-stu-id="baeaa-103">ICertificate2::Export method</span></span>

<span data-ttu-id="baeaa-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="baeaa-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="baeaa-105">Usare invece la [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="baeaa-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="baeaa-106">Il metodo **Export** copia un certificato in una stringa codificata.</span><span class="sxs-lookup"><span data-stu-id="baeaa-106">The **Export** method copies a certificate to an encoded string.</span></span> <span data-ttu-id="baeaa-107">La stringa codificata può essere scritta in un file o importata in un nuovo oggetto [**certificato**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="baeaa-107">The encoded string can be written to a file or imported into a new [**Certificate**](certificate.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="baeaa-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="baeaa-108">Syntax</span></span>


```VB
Certificate.Export( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="baeaa-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="baeaa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baeaa-110">*EncodingType* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="baeaa-110">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="baeaa-111">Valore dell'enumerazione del [**\_ \_ tipo di codifica CAPICOM**](capicom-encoding-type.md) che specifica il tipo di codifica per l'operazione di esportazione.</span><span class="sxs-lookup"><span data-stu-id="baeaa-111">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that specifies the encoding type for the export operation.</span></span> <span data-ttu-id="baeaa-112">Il valore predefinito è **CAPICOM \_ Encode \_ base64**.</span><span class="sxs-lookup"><span data-stu-id="baeaa-112">The default value is **CAPICOM\_ENCODE\_BASE64**.</span></span> <span data-ttu-id="baeaa-113">Nella tabella seguente sono illustrati i possibili valori.</span><span class="sxs-lookup"><span data-stu-id="baeaa-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="baeaa-114">Valore</span><span class="sxs-lookup"><span data-stu-id="baeaa-114">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="baeaa-115">Significato</span><span class="sxs-lookup"><span data-stu-id="baeaa-115">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="baeaa-116"><dt>**CAPICOM \_ Encode \_ any**</dt></span><span class="sxs-lookup"><span data-stu-id="baeaa-116"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="baeaa-117">Questo tipo di codifica viene utilizzato solo quando i dati di input hanno un tipo di codifica sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="baeaa-117">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="baeaa-118">Se questo valore viene usato per specificare il tipo di codifica dell'output, \_ \_ verrà invece usato CAPICOM Encode Base64.</span><span class="sxs-lookup"><span data-stu-id="baeaa-118">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="baeaa-119">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="baeaa-119">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="baeaa-120"><dt>**\_Codifica Base64 per CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="baeaa-120"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="baeaa-121">I dati vengono salvati come stringa con codifica Base64.</span><span class="sxs-lookup"><span data-stu-id="baeaa-121">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="baeaa-122"><dt>**\_codificare il \_ file binario di CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="baeaa-122"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="baeaa-123">I dati vengono salvati come una sequenza binaria pura.</span><span class="sxs-lookup"><span data-stu-id="baeaa-123">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baeaa-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="baeaa-124">Return value</span></span>

<span data-ttu-id="baeaa-125">Stringa che contiene il certificato esportato nel formato di codifica specificato.</span><span class="sxs-lookup"><span data-stu-id="baeaa-125">A string that contains the exported certificate in the specified encoding form.</span></span>

## <a name="requirements"></a><span data-ttu-id="baeaa-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="baeaa-126">Requirements</span></span>



| <span data-ttu-id="baeaa-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="baeaa-127">Requirement</span></span> | <span data-ttu-id="baeaa-128">Valore</span><span class="sxs-lookup"><span data-stu-id="baeaa-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="baeaa-129">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="baeaa-129">End of client support</span></span><br/> | <span data-ttu-id="baeaa-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="baeaa-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="baeaa-131">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="baeaa-131">End of server support</span></span><br/> | <span data-ttu-id="baeaa-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="baeaa-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="baeaa-133">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="baeaa-133">Redistributable</span></span><br/>       | <span data-ttu-id="baeaa-134">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="baeaa-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="baeaa-135">DLL</span><span class="sxs-lookup"><span data-stu-id="baeaa-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="baeaa-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="baeaa-136"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baeaa-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="baeaa-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baeaa-138">Oggetti Cryptography</span><span class="sxs-lookup"><span data-stu-id="baeaa-138">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="baeaa-139">**Certificato**</span><span class="sxs-lookup"><span data-stu-id="baeaa-139">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
