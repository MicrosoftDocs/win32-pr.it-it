---
description: Indica le lunghezze di NALUs nell'esempio. Si tratta di un BLOB MF impostato su esempi di input compressi per il decodificatore H. 264.
ms.assetid: 09F54504-A6CF-4385-BDD7-8D23B1D0125C
title: Attributo MF_NALU_LENGTH_INFORMATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46d9a0b7cbec92c4cde40548b8d3baecf955b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310824"
---
# <a name="mf_nalu_length_information-attribute"></a><span data-ttu-id="3b8bf-104">\_ \_ \_ Attributo delle informazioni sulla lunghezza di MF Nalu</span><span class="sxs-lookup"><span data-stu-id="3b8bf-104">MF\_NALU\_LENGTH\_INFORMATION attribute</span></span>

<span data-ttu-id="3b8bf-105">Indica le lunghezze di NALUs nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="3b8bf-105">Indicates the lengths of NALUs in the sample.</span></span> <span data-ttu-id="3b8bf-106">Si tratta di un **BLOB** MF impostato su esempi di input compressi per il decodificatore H. 264.</span><span class="sxs-lookup"><span data-stu-id="3b8bf-106">This is a MF **BLOB** that is set on compressed input samples to the H.264 decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="3b8bf-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3b8bf-107">Data type</span></span>

<span data-ttu-id="3b8bf-108">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="3b8bf-108">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="3b8bf-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b8bf-109">Remarks</span></span>

<span data-ttu-id="3b8bf-110">Per impostare questo attributo, è necessario che il supporto sia di tipo MEDIASUBTYPE \_ H264 e che l'attributo [ \_ set di \_ lunghezza \_ MF Nalu](mf-nalu-length-set.md) sia impostato sul tipo di supporto di input di MEDIASUBTYPE \_ H264.</span><span class="sxs-lookup"><span data-stu-id="3b8bf-110">In order for this attribute to be set, the media must be of type MEDIASUBTYPE\_H264 and the [MF\_NALU\_LENGTH\_SET](mf-nalu-length-set.md) attribute must be set on the input media type of MEDIASUBTYPE\_H264.</span></span>

<span data-ttu-id="3b8bf-111">Impostare MF \_ Nalu \_ length \_ Information come **BLOB** nell'esempio di input, con un valore DWORD per ogni Nalu nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="3b8bf-111">Set MF\_NALU\_LENGTH\_INFORMATION as a **BLOB** on the input sample, with one DWORD for each NALU in the sample.</span></span> <span data-ttu-id="3b8bf-112">Se ad esempio sono presenti AUD (9 byte), SPS (25 byte), PPS (10 byte), IDR slice1 (50 k), IDR Slice 2 (60 k), dovrebbero essere presenti 5 DWORD con valori 9, 25, 10, 50 k, 60 k nel **BLOB**.</span><span class="sxs-lookup"><span data-stu-id="3b8bf-112">For example, if there are AUD (9 bytes), SPS (25 bytes), PPS (10 bytes), IDR slice1 (50 k), IDR slice 2 (60 k), then there should be 5 DWORDs with values 9, 25, 10, 50 k, 60 k in the **BLOB**.</span></span>

<span data-ttu-id="3b8bf-113">Di seguito è riportato il codice che imposta il **BLOB**, dove **rgdwNALULengthInfo** è una matrice di tipo DWORD e **uiNaluLengthIdx** è la lunghezza Nalu valida impostata sul **BLOB**.</span><span class="sxs-lookup"><span data-stu-id="3b8bf-113">Here some code that sets the **BLOB**, where **rgdwNALULengthInfo** is an array of type DWORD and **uiNaluLengthIdx** is the valid NALU lengths set to the **BLOB**.</span></span>


```C++
m_spSample->SetBlob( MF_NALU_LENGTH_INFORMATION, 
                    (UINT8*) m_wpParent->m_pdwNALULengthInfo, 
                    sizeof(DWORD)*uiNaluLengthIdx ), 
                    done );
```



## <a name="requirements"></a><span data-ttu-id="3b8bf-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b8bf-114">Requirements</span></span>



| <span data-ttu-id="3b8bf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b8bf-115">Requirement</span></span> | <span data-ttu-id="3b8bf-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3b8bf-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3b8bf-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b8bf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3b8bf-118">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3b8bf-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="3b8bf-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b8bf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3b8bf-120">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="3b8bf-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="3b8bf-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b8bf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b8bf-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b8bf-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b8bf-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b8bf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b8bf-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3b8bf-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3b8bf-125">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="3b8bf-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




