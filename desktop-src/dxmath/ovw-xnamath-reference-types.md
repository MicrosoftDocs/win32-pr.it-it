---
description: La libreria DirectXMath fornisce una serie di strutture e tipi definiti per incapsulare i dati per supportare semplicità di utilizzo, ottimizzazione e portabilità.
ms.assetid: 4b9ffc17-3917-551c-7cb5-19de505dfd21
title: Tipi di libreria DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32ac888e451fe1e1ba5cfc66184bf2eb7b6feffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880129"
---
# <a name="directxmath-library-types"></a><span data-ttu-id="0d453-103">Tipi di libreria DirectXMath</span><span class="sxs-lookup"><span data-stu-id="0d453-103">DirectXMath Library types</span></span>

<span data-ttu-id="0d453-104">La libreria DirectXMath fornisce una serie di strutture e tipi definiti per incapsulare i dati per supportare semplicità di utilizzo, ottimizzazione e portabilità.</span><span class="sxs-lookup"><span data-stu-id="0d453-104">The DirectXMath Library provides a number of structures and defined types to encapsulate data to support ease of use, optimization, and portability.</span></span>

<span data-ttu-id="0d453-105">L'elenco seguente include le strutture che fanno attualmente parte della libreria DirectXMath e sono disponibili tramite l'intestazione DirectXMath. h.</span><span class="sxs-lookup"><span data-stu-id="0d453-105">The list below includes structures currently part of the DirectXMath Library, and available through the DirectXMath.h header.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0d453-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="0d453-106">In this section</span></span>



| <span data-ttu-id="0d453-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="0d453-107">Topic</span></span>                                                             | <span data-ttu-id="0d453-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d453-108">Description</span></span>                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d453-109">**Tipo di dati HALF**</span><span class="sxs-lookup"><span data-stu-id="0d453-109">**HALF Data Type**</span></span>](half-data-type.md)<br/>               | <span data-ttu-id="0d453-110">Alias per **UInt16 \_ t** compresso con un numero a virgola mobile a 16 bit costituito da un bit di segno, un esponente distorta a 5 bit e un mantissa a 10 bit.</span><span class="sxs-lookup"><span data-stu-id="0d453-110">An alias to **uint16\_t** packed with a 16-bit floating-point number consisting of a sign bit, a 5-bit biased exponent, and a 10-bit mantissa.</span></span><br/>                         |
| [<span data-ttu-id="0d453-111">**Tipo di dati XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="0d453-111">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)<br/>       | <span data-ttu-id="0d453-112">Tipo portabile usato per rappresentare un vettore di componenti a virgola mobile o Integer a 4 32 bit, ognuno allineato in modo ottimale e mappato a un registro di vettori hardware.</span><span class="sxs-lookup"><span data-stu-id="0d453-112">A portable type used to represent a vector of four 32-bit floating-point or integer components, each aligned optimally and mapped to a hardware vector register.</span></span><br/>       |
| [<span data-ttu-id="0d453-113">**Tipo di dati XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="0d453-113">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)<br/> | <span data-ttu-id="0d453-114">Tipo opaco e portabile per supportare l'utilizzo della sintassi dell'inizializzatore C/C++ per caricare valori a virgola mobile in un'istanza di tipo [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="0d453-114">An opaque, portable type to support the use of C/C++ initializer syntax to load floating-point values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span><br/> |
| [<span data-ttu-id="0d453-115">**Tipo di dati XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="0d453-115">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)<br/> | <span data-ttu-id="0d453-116">Tipo opaco e portabile per supportare l'utilizzo della sintassi dell'inizializzatore C/C++ per caricare valori integer in un'istanza di tipo [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="0d453-116">An opaque, portable type to support the use of C/C++ initializer syntax to load integer values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span><br/>        |
| [<span data-ttu-id="0d453-117">**Tipo di dati XMVECTORU32**</span><span class="sxs-lookup"><span data-stu-id="0d453-117">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)<br/> | <span data-ttu-id="0d453-118">Tipo opaco e portabile per supportare l'utilizzo della sintassi dell'inizializzatore C/C++ per caricare \_ i valori UInt32 t in un'istanza di tipo XMVECTOR.</span><span class="sxs-lookup"><span data-stu-id="0d453-118">An opaque, portable type to support the use of C/C++ initializer syntax to load uint32\_t values into an instance of XMVECTOR type.</span></span><br/>                                    |
| [<span data-ttu-id="0d453-119">**Tipo di dati XMVECTORU8**</span><span class="sxs-lookup"><span data-stu-id="0d453-119">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)<br/>   | <span data-ttu-id="0d453-120">Tipo opaco e portabile per supportare l'uso della sintassi dell'inizializzatore C/C++ per caricare \_ i valori Uint8 in un'istanza di tipo XMVECTOR.</span><span class="sxs-lookup"><span data-stu-id="0d453-120">An opaque, portable type to support the use of C/C++ initializer syntax to load uint8\_t values into an instance of XMVECTOR type.</span></span><br/>                                     |



 

## <a name="related-topics"></a><span data-ttu-id="0d453-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0d453-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d453-122">Guida di riferimento alla programmazione DirectXMath</span><span class="sxs-lookup"><span data-stu-id="0d453-122">DirectXMath Programming Reference</span></span>](ovw-xnamath-reference.md)
</dt> </dl>

 

 




