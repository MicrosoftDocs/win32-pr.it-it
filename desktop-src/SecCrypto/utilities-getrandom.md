---
description: Genera un numero casuale sicuro utilizzando il provider del servizio di crittografia (CSP) predefinito.
ms.assetid: 52c49f73-58b8-455f-9368-54f38de55776
title: Utilities. GetRandom, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.GetRandom
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b7e02c7df61c1a2d710189fb2e5e0a21cc0b504
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327884"
---
# <a name="utilitiesgetrandom-method"></a><span data-ttu-id="b086b-103">Utilities. GetRandom, metodo</span><span class="sxs-lookup"><span data-stu-id="b086b-103">Utilities.GetRandom method</span></span>

<span data-ttu-id="b086b-104">\[Il metodo **GetRandom** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.\]</span><span class="sxs-lookup"><span data-stu-id="b086b-104">\[The **GetRandom** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="b086b-105">Il metodo **GetRandom** genera un numero casuale sicuro usando il [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) predefinito.</span><span class="sxs-lookup"><span data-stu-id="b086b-105">The **GetRandom** method generates a secure random number using the default [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

## <a name="syntax"></a><span data-ttu-id="b086b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b086b-106">Syntax</span></span>


```VB
Utilities.GetRandom( _
  [ ByVal Length ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b086b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b086b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b086b-108">*Lunghezza* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b086b-108">*Length* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b086b-109">Lunghezza, in byte, del numero casuale da creare.</span><span class="sxs-lookup"><span data-stu-id="b086b-109">The length, in bytes, of the random number to create.</span></span> <span data-ttu-id="b086b-110">Il valore predefinito è 8 byte.</span><span class="sxs-lookup"><span data-stu-id="b086b-110">The default value is 8 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b086b-111">*EncodingType* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="b086b-111">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b086b-112">Valore dell'enumerazione del [**\_ \_ tipo di codifica CAPICOM**](capicom-encoding-type.md) che indica il tipo di codifica da utilizzare per il numero casuale generato.</span><span class="sxs-lookup"><span data-stu-id="b086b-112">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that indicates the type of encoding to use for the generated random number.</span></span> <span data-ttu-id="b086b-113">Il valore predefinito è CAPICOM \_ Encode \_ Binary.</span><span class="sxs-lookup"><span data-stu-id="b086b-113">The default value is CAPICOM\_ENCODE\_BINARY.</span></span> <span data-ttu-id="b086b-114">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b086b-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="b086b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b086b-115">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="b086b-116">Significato</span><span class="sxs-lookup"><span data-stu-id="b086b-116">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="b086b-117"><dt>**CAPICOM \_ Encode \_ any**</dt></span><span class="sxs-lookup"><span data-stu-id="b086b-117"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="b086b-118">Questo tipo di codifica viene utilizzato solo quando i dati di input hanno un tipo di codifica sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b086b-118">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="b086b-119">Se questo valore viene usato per specificare il tipo di codifica dell'output, \_ \_ verrà invece usato CAPICOM Encode Base64.</span><span class="sxs-lookup"><span data-stu-id="b086b-119">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="b086b-120">Introdotta in capicol 2,0.</span><span class="sxs-lookup"><span data-stu-id="b086b-120">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="b086b-121"><dt>**\_Codifica Base64 per CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b086b-121"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="b086b-122">I dati vengono salvati come stringa con codifica Base64.</span><span class="sxs-lookup"><span data-stu-id="b086b-122">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="b086b-123"><dt>**\_codificare il \_ file binario di CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="b086b-123"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="b086b-124">I dati vengono salvati come una sequenza binaria pura.</span><span class="sxs-lookup"><span data-stu-id="b086b-124">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b086b-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b086b-125">Return value</span></span>

<span data-ttu-id="b086b-126">*Lunghezza* in byte del numero generato casualmente, con la codifica specificata.</span><span class="sxs-lookup"><span data-stu-id="b086b-126">A randomly generated number *Length* bytes long, with the specified encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="b086b-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b086b-127">Requirements</span></span>



| <span data-ttu-id="b086b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b086b-128">Requirement</span></span> | <span data-ttu-id="b086b-129">Valore</span><span class="sxs-lookup"><span data-stu-id="b086b-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b086b-130">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="b086b-130">Redistributable</span></span><br/> | <span data-ttu-id="b086b-131">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="b086b-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b086b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b086b-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="b086b-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b086b-133"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b086b-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b086b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b086b-135">**Utilità**</span><span class="sxs-lookup"><span data-stu-id="b086b-135">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 
