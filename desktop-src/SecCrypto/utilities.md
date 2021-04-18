---
description: Fornisce funzionalità per la generazione di numeri casuali, le conversioni e la codifica e la decodifica da Base64.
ms.assetid: c0073361-5d0d-4915-8110-02f6e1e0714e
title: Utilità (oggetto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2f6000179b1752630f02d03aa5c87dea11364d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331261"
---
# <a name="utilities-object"></a><span data-ttu-id="6a103-103">Utilità (oggetto)</span><span class="sxs-lookup"><span data-stu-id="6a103-103">Utilities object</span></span>

<span data-ttu-id="6a103-104">\[L'oggetto **Utilities** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.\]</span><span class="sxs-lookup"><span data-stu-id="6a103-104">\[The **Utilities** object is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="6a103-105">L'oggetto **Utilities** fornisce funzionalità per la generazione di numeri casuali, le conversioni e la codifica e la decodifica da Base64.</span><span class="sxs-lookup"><span data-stu-id="6a103-105">The **Utilities** object provides functionality for random number generation, conversions, and encoding and decoding from base64.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="6a103-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="6a103-106">When to use</span></span>

<span data-ttu-id="6a103-107">L'oggetto **Utilities** viene utilizzato per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="6a103-107">The **Utilities** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="6a103-108">Codificare una stringa come base64 o decodificare una stringa da Base64.</span><span class="sxs-lookup"><span data-stu-id="6a103-108">Encode a string as base64 or decode a string from base64.</span></span>
-   <span data-ttu-id="6a103-109">Converte una stringa con pacchetto binario in una matrice di byte e viceversa.</span><span class="sxs-lookup"><span data-stu-id="6a103-109">Convert a binary-packed string to a byte array and vice versa.</span></span>
-   <span data-ttu-id="6a103-110">Converte una stringa con pacchetto binario in una stringa esadecimale e viceversa.</span><span class="sxs-lookup"><span data-stu-id="6a103-110">Convert a binary-packed string to a hexadecimal string and vice versa.</span></span>
-   <span data-ttu-id="6a103-111">Genera un numero casuale protetto.</span><span class="sxs-lookup"><span data-stu-id="6a103-111">Generate a secure random number.</span></span>
-   <span data-ttu-id="6a103-112">Converte l'ora locale in ora UTC (ora di Greenwich) e viceversa.</span><span class="sxs-lookup"><span data-stu-id="6a103-112">Convert local time to Coordinated Universal Time (Greenwich Mean Time) and vice versa.</span></span>

## <a name="members"></a><span data-ttu-id="6a103-113">Membri</span><span class="sxs-lookup"><span data-stu-id="6a103-113">Members</span></span>

<span data-ttu-id="6a103-114">L'oggetto **Utilities** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6a103-114">The **Utilities** object has these types of members:</span></span>

-   [<span data-ttu-id="6a103-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="6a103-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6a103-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="6a103-116">Methods</span></span>

<span data-ttu-id="6a103-117">L'oggetto **Utilities** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6a103-117">The **Utilities** object has these methods.</span></span>



| <span data-ttu-id="6a103-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="6a103-118">Method</span></span>                                                               | <span data-ttu-id="6a103-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a103-119">Description</span></span>                                                                  |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="6a103-120">**Base64Decode**</span><span class="sxs-lookup"><span data-stu-id="6a103-120">**Base64Decode**</span></span>](utilities-base64decode.md)                       | <span data-ttu-id="6a103-121">Decodifica una stringa da Base64.</span><span class="sxs-lookup"><span data-stu-id="6a103-121">Decodes a string from base64.</span></span><br/>                                     |
| [<span data-ttu-id="6a103-122">**Base64Encode**</span><span class="sxs-lookup"><span data-stu-id="6a103-122">**Base64Encode**</span></span>](utilities-base64encode.md)                       | <span data-ttu-id="6a103-123">Codifica una stringa come Base64.</span><span class="sxs-lookup"><span data-stu-id="6a103-123">Encodes a string as base64.</span></span><br/>                                       |
| [<span data-ttu-id="6a103-124">**BinaryStringToByteArray**</span><span class="sxs-lookup"><span data-stu-id="6a103-124">**BinaryStringToByteArray**</span></span>](utilities-binarystringtobytearray.md) | <span data-ttu-id="6a103-125">Converte una stringa con pacchetto binario in una matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="6a103-125">Converts a binary-packed string to an array of bytes.</span></span><br/>             |
| [<span data-ttu-id="6a103-126">**BinaryToHex**</span><span class="sxs-lookup"><span data-stu-id="6a103-126">**BinaryToHex**</span></span>](utilities-binarytohex.md)                         | <span data-ttu-id="6a103-127">Converte una stringa con pacchetto binario in una stringa esadecimale.</span><span class="sxs-lookup"><span data-stu-id="6a103-127">Converts a binary-packed string to a hexadecimal string.</span></span><br/>          |
| [<span data-ttu-id="6a103-128">**ByteArrayToBinaryString**</span><span class="sxs-lookup"><span data-stu-id="6a103-128">**ByteArrayToBinaryString**</span></span>](utilities-bytearraytobinarystring.md) | <span data-ttu-id="6a103-129">Converte una matrice di byte in una stringa con pacchetto binario.</span><span class="sxs-lookup"><span data-stu-id="6a103-129">Converts an array of bytes to a binary-packed string.</span></span><br/>             |
| [<span data-ttu-id="6a103-130">**GetRandom**</span><span class="sxs-lookup"><span data-stu-id="6a103-130">**GetRandom**</span></span>](utilities-getrandom.md)                             | <span data-ttu-id="6a103-131">Genera un numero casuale protetto.</span><span class="sxs-lookup"><span data-stu-id="6a103-131">Generates a secure random number.</span></span><br/>                                 |
| [<span data-ttu-id="6a103-132">**HexToBinary**</span><span class="sxs-lookup"><span data-stu-id="6a103-132">**HexToBinary**</span></span>](utilities-hextobinary.md)                         | <span data-ttu-id="6a103-133">Converte una stringa esadecimale in una stringa con pacchetto binario.</span><span class="sxs-lookup"><span data-stu-id="6a103-133">Converts a hexadecimal string to a binary-packed string.</span></span><br/>          |
| [<span data-ttu-id="6a103-134">**LocalTimeToUTCTime**</span><span class="sxs-lookup"><span data-stu-id="6a103-134">**LocalTimeToUTCTime**</span></span>](utilities-localtimetoutctime.md)           | <span data-ttu-id="6a103-135">Converte l'ora locale del computer nell'ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="6a103-135">Converts the computer's local time to Coordinated Universal Time.</span></span><br/> |
| [<span data-ttu-id="6a103-136">**UTCTimeToLocalTime**</span><span class="sxs-lookup"><span data-stu-id="6a103-136">**UTCTimeToLocalTime**</span></span>](utilities-utctimetolocaltime.md)           | <span data-ttu-id="6a103-137">Converte l'ora UTC (Coordinated Universal Time) nell'ora locale del computer.</span><span class="sxs-lookup"><span data-stu-id="6a103-137">Converts Coordinated Universal Time to the computer's local time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6a103-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a103-138">Remarks</span></span>

<span data-ttu-id="6a103-139">È possibile creare l'oggetto **Utilities** ed è sicuro per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="6a103-139">The **Utilities** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="6a103-140">Il ProgID per l'oggetto **Utilities** è capicom. Utilities. 1.</span><span class="sxs-lookup"><span data-stu-id="6a103-140">The ProgID for the **Utilities** object is CAPICOM.Utilities.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a103-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a103-141">Requirements</span></span>



| <span data-ttu-id="6a103-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a103-142">Requirement</span></span> | <span data-ttu-id="6a103-143">Valore</span><span class="sxs-lookup"><span data-stu-id="6a103-143">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a103-144">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="6a103-144">Redistributable</span></span><br/> | <span data-ttu-id="6a103-145">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="6a103-145">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6a103-146">DLL</span><span class="sxs-lookup"><span data-stu-id="6a103-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="6a103-147"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a103-147"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




