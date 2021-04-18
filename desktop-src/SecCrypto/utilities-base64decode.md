---
description: Decodifica una stringa da Base64.
ms.assetid: acf2dba6-a0e8-4b77-a5a6-93cfa6afe874
title: Utilities. Base64Decode, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Decode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df0a0e2a0400ef2000ce5e54e1a76a1a4bd8eebd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327995"
---
# <a name="utilitiesbase64decode-method"></a><span data-ttu-id="967fd-103">Utilities. Base64Decode, metodo</span><span class="sxs-lookup"><span data-stu-id="967fd-103">Utilities.Base64Decode method</span></span>

<span data-ttu-id="967fd-104">\[Il metodo **Base64Decode** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.\]</span><span class="sxs-lookup"><span data-stu-id="967fd-104">\[The **Base64Decode** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="967fd-105">Il metodo **Base64Decode** decodifica una stringa da Base64.</span><span class="sxs-lookup"><span data-stu-id="967fd-105">The **Base64Decode** method decodes a string from base64.</span></span>

## <a name="syntax"></a><span data-ttu-id="967fd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="967fd-106">Syntax</span></span>


```VB
Utilities.Base64Decode( _
  ByVal EncodedString _
)
```



## <a name="parameters"></a><span data-ttu-id="967fd-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="967fd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="967fd-108">*EncodedString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="967fd-108">*EncodedString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="967fd-109">Stringa con codifica base64 da decodificare.</span><span class="sxs-lookup"><span data-stu-id="967fd-109">The base64-encoded string to decode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="967fd-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="967fd-110">Return value</span></span>

<span data-ttu-id="967fd-111">Stringa decodificata.</span><span class="sxs-lookup"><span data-stu-id="967fd-111">The decoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="967fd-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="967fd-112">Remarks</span></span>

<span data-ttu-id="967fd-113">La codifica Base64 è lo schema utilizzato per la trasmissione di dati binari.</span><span class="sxs-lookup"><span data-stu-id="967fd-113">Base64 encoding is the scheme used to transmit binary data.</span></span> <span data-ttu-id="967fd-114">Base64 elabora i dati come gruppi a 24 bit, eseguendo il mapping di questi dati a quattro caratteri codificati.</span><span class="sxs-lookup"><span data-stu-id="967fd-114">Base64 processes data as 24-bit groups, mapping this data to four encoded characters.</span></span> <span data-ttu-id="967fd-115">La codifica Base64 viene a volte definita codifica da 3 a 4.</span><span class="sxs-lookup"><span data-stu-id="967fd-115">Base64 encoding is sometimes referred to as 3-to-4 encoding.</span></span> <span data-ttu-id="967fd-116">Ogni 6 bit del gruppo a 24 bit viene utilizzato come indice in una tabella di mapping (alfabeto Base64) per ottenere un carattere per i dati codificati.</span><span class="sxs-lookup"><span data-stu-id="967fd-116">Each 6 bits of the 24-bit group is used as an index into a mapping table (the base64 alphabet) to obtain a character for the encoded data.</span></span> <span data-ttu-id="967fd-117">I dati codificati hanno lunghezze di riga limitate a 76 caratteri.</span><span class="sxs-lookup"><span data-stu-id="967fd-117">The encoded data has line lengths that are limited to 76 characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="967fd-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="967fd-118">Requirements</span></span>



| <span data-ttu-id="967fd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="967fd-119">Requirement</span></span> | <span data-ttu-id="967fd-120">Valore</span><span class="sxs-lookup"><span data-stu-id="967fd-120">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="967fd-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="967fd-121">Redistributable</span></span><br/> | <span data-ttu-id="967fd-122">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="967fd-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="967fd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="967fd-123">DLL</span></span><br/>             | <dl> <span data-ttu-id="967fd-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="967fd-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="967fd-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="967fd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="967fd-126">**Utilità**</span><span class="sxs-lookup"><span data-stu-id="967fd-126">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




