---
description: Ottiene o imposta la velocità di decodifica dei video.
ms.assetid: 76F7013D-C172-4D31-93BC-EA3D186EB14C
title: Proprietà AVDecVideoFastDecodeMode (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355c085731befedbcb9245a67870d9d609a92c6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125265"
---
# <a name="avdecvideofastdecodemode-property"></a><span data-ttu-id="fa3c8-103">Proprietà AVDecVideoFastDecodeMode</span><span class="sxs-lookup"><span data-stu-id="fa3c8-103">AVDecVideoFastDecodeMode property</span></span>

<span data-ttu-id="fa3c8-104">Ottiene o imposta la velocità di decodifica dei video.</span><span class="sxs-lookup"><span data-stu-id="fa3c8-104">Gets or sets the video decoding speed.</span></span>

## <a name="data-type"></a><span data-ttu-id="fa3c8-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="fa3c8-105">Data type</span></span>

<span data-ttu-id="fa3c8-106">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="fa3c8-106">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="fa3c8-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="fa3c8-107">Property GUID</span></span>

<span data-ttu-id="fa3c8-108">**Codecapis \_ AVDecVideoFastDecodeMode**</span><span class="sxs-lookup"><span data-stu-id="fa3c8-108">**CODECAPI\_AVDecVideoFastDecodeMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="fa3c8-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fa3c8-109">Property value</span></span>

<span data-ttu-id="fa3c8-110">Il valore di questa proprietà può variare da 0 a 32, dove 0 indica la decodifica normale e 32 è la modalità di decodifica più veloce.</span><span class="sxs-lookup"><span data-stu-id="fa3c8-110">The value of this property can range from 0 to 32, where 0 indicates normal decoding and 32 is the fastest decoding mode.</span></span> <span data-ttu-id="fa3c8-111">Il comportamento esatto dipende dall'implementazione del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="fa3c8-111">The exact behavior depends on the decoder implementation.</span></span> <span data-ttu-id="fa3c8-112">Non tutti gli incrementi compresi tra 1 e 32 definiscono necessariamente una modalità distinta.</span><span class="sxs-lookup"><span data-stu-id="fa3c8-112">Not every increment between 1 and 32 necessarily defines is a distinct mode.</span></span>

<span data-ttu-id="fa3c8-113">L'enumerazione [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) contiene alcune modalità predefinite per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="fa3c8-113">The [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) enumeration contains some predefined modes for this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa3c8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa3c8-114">Requirements</span></span>



| <span data-ttu-id="fa3c8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa3c8-115">Requirement</span></span> | <span data-ttu-id="fa3c8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="fa3c8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa3c8-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa3c8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fa3c8-118">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="fa3c8-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="fa3c8-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa3c8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fa3c8-120">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fa3c8-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="fa3c8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa3c8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa3c8-122"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa3c8-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa3c8-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa3c8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa3c8-124">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="fa3c8-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="fa3c8-125">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="fa3c8-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




