---
title: WM/EncodingTime
description: L'attributo WM/EncodingTime contiene un timestamp del momento in cui è stato codificato il contenuto.
ms.assetid: 63da9392-264d-40bb-99fd-56db93801941
keywords:
- Formato di Windows Media WM/EncodingTime
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d27119a9b54e3de22fe620f556c672bd4fe1a17
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045929"
---
# <a name="wmencodingtime"></a><span data-ttu-id="770e4-104">WM/EncodingTime</span><span class="sxs-lookup"><span data-stu-id="770e4-104">WM/EncodingTime</span></span>

<span data-ttu-id="770e4-105">L'attributo **WM/EncodingTime** contiene un timestamp del momento in cui è stato codificato il contenuto.</span><span class="sxs-lookup"><span data-stu-id="770e4-105">The **WM/EncodingTime** attribute contains a time stamp of the time at which the content was encoded.</span></span>

## <a name="global-constant"></a><span data-ttu-id="770e4-106">Costante globale</span><span class="sxs-lookup"><span data-stu-id="770e4-106">Global Constant</span></span>

<span data-ttu-id="770e4-107">g \_ wszWMEncodingTime</span><span class="sxs-lookup"><span data-stu-id="770e4-107">g\_wszWMEncodingTime</span></span>

## <a name="data-type"></a><span data-ttu-id="770e4-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="770e4-108">Data Type</span></span>

<span data-ttu-id="770e4-109">**FILETIME** (**\_ tipo WMT \_ QWORD**)</span><span class="sxs-lookup"><span data-stu-id="770e4-109">**FILETIME** (**WMT\_TYPE\_QWORD**)</span></span>

## <a name="remarks"></a><span data-ttu-id="770e4-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="770e4-110">Remarks</span></span>

<span data-ttu-id="770e4-111">Questo attributo utilizza un valore FILETIME, ovvero un valore a 64 bit che rappresenta il numero di unità di tempo 100-nanosecondi trascorsi dal 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="770e4-111">This attribute uses a FILETIME value, which is a 64-bit value representing the number of 100-nanosecond time units elapsed since January 1, 1601.</span></span> <span data-ttu-id="770e4-112">Per ulteriori informazioni su FILETIME, vedere la sezione informazioni di sistema Windows di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="770e4-112">For more information about the FILETIME, see the Windows System Information section of the Platform SDK.</span></span>

<span data-ttu-id="770e4-113">Non si tratta di un attributo codificato.</span><span class="sxs-lookup"><span data-stu-id="770e4-113">This is not a coded attribute.</span></span> <span data-ttu-id="770e4-114">È necessario impostarla manualmente se si vuole includerla nei file.</span><span class="sxs-lookup"><span data-stu-id="770e4-114">You must set it manually if you want to include it in your files.</span></span>

## <a name="see-also"></a><span data-ttu-id="770e4-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="770e4-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="770e4-116">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="770e4-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




