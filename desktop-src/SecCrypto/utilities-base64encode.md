---
description: Codifica una stringa come Base64.
ms.assetid: 73a279e3-40b0-4db8-89d3-95627f0878dd
title: Utilities. Base64Encode, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.Base64Encode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0536097e3e46fcc09702c1e4000d2fbd9856c205
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326887"
---
# <a name="utilitiesbase64encode-method"></a><span data-ttu-id="b2581-103">Utilities. Base64Encode, metodo</span><span class="sxs-lookup"><span data-stu-id="b2581-103">Utilities.Base64Encode method</span></span>

<span data-ttu-id="b2581-104">\[Il metodo **Base64Encode** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.\]</span><span class="sxs-lookup"><span data-stu-id="b2581-104">\[The **Base64Encode** method is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="b2581-105">Il metodo **Base64Encode** codifica una stringa come Base64.</span><span class="sxs-lookup"><span data-stu-id="b2581-105">The **Base64Encode** method encodes a string as base64.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2581-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2581-106">Syntax</span></span>


```VB
Utilities.Base64Encode( _
  ByVal SrcString _
)
```



## <a name="parameters"></a><span data-ttu-id="b2581-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2581-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2581-108">*SrcString* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2581-108">*SrcString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2581-109">Stringa da codificare come Base64.</span><span class="sxs-lookup"><span data-stu-id="b2581-109">The string to encode as base64.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2581-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2581-110">Return value</span></span>

<span data-ttu-id="b2581-111">Stringa con codifica Base64.</span><span class="sxs-lookup"><span data-stu-id="b2581-111">The base64-encoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2581-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2581-112">Remarks</span></span>

<span data-ttu-id="b2581-113">La codifica Base64 è lo schema utilizzato per la trasmissione di dati binari.</span><span class="sxs-lookup"><span data-stu-id="b2581-113">Base64 encoding is the scheme used to transmit binary data.</span></span> <span data-ttu-id="b2581-114">Base64 elabora i dati come gruppi a 24 bit, eseguendo il mapping di questi dati a quattro caratteri codificati.</span><span class="sxs-lookup"><span data-stu-id="b2581-114">Base64 processes data as 24-bit groups, mapping this data to four encoded characters.</span></span> <span data-ttu-id="b2581-115">La codifica Base64 viene a volte definita codifica da 3 a 4.</span><span class="sxs-lookup"><span data-stu-id="b2581-115">Base64 encoding is sometimes referred to as 3-to-4 encoding.</span></span> <span data-ttu-id="b2581-116">Ogni 6 bit del gruppo a 24 bit viene utilizzato come indice in una tabella di mapping (alfabeto Base64) per ottenere un carattere per i dati codificati.</span><span class="sxs-lookup"><span data-stu-id="b2581-116">Each 6 bits of the 24-bit group is used as an index into a mapping table (the base64 alphabet) to obtain a character for the encoded data.</span></span> <span data-ttu-id="b2581-117">I dati codificati hanno lunghezze di riga limitate a 76 caratteri.</span><span class="sxs-lookup"><span data-stu-id="b2581-117">The encoded data has line lengths that are limited to 76 characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2581-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2581-118">Requirements</span></span>



| <span data-ttu-id="b2581-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2581-119">Requirement</span></span> | <span data-ttu-id="b2581-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b2581-120">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2581-121">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="b2581-121">Redistributable</span></span><br/> | <span data-ttu-id="b2581-122">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="b2581-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b2581-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b2581-123">DLL</span></span><br/>             | <dl> <span data-ttu-id="b2581-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2581-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2581-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2581-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2581-126">**Utilità**</span><span class="sxs-lookup"><span data-stu-id="b2581-126">**Utilities**</span></span>](utilities.md)
</dt> </dl>

 

 




