---
title: Struttura WINBIO_BIR ( \_ tipi WINBIO. h)
description: Rappresenta un record di informazioni biometriche (BIR).
ms.assetid: 39cfab34-0416-4897-bf95-a1b3c3a6a7a1
keywords:
- Struttura di WINBIO_BIR Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_BIR
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e422bbe59414d75541127b41e5e2cc1829adaaa7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302622"
---
# <a name="winbio_bir-structure"></a><span data-ttu-id="de9ea-104">\_Struttura WINBIO Bir</span><span class="sxs-lookup"><span data-stu-id="de9ea-104">WINBIO\_BIR structure</span></span>

<span data-ttu-id="de9ea-105">La struttura **WINBIO \_ Bir** rappresenta un record di informazioni biometriche (Bir).</span><span class="sxs-lookup"><span data-stu-id="de9ea-105">The **WINBIO\_BIR** structure represents a biometric information record (BIR).</span></span> <span data-ttu-id="de9ea-106">Il record di informazioni contiene i blocchi di intestazione, dati e firma.</span><span class="sxs-lookup"><span data-stu-id="de9ea-106">The information record contains header, data, and signature blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="de9ea-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de9ea-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR {
  WINBIO_BIR_DATA HeaderBlock;
  WINBIO_BIR_DATA StandardDataBlock;
  WINBIO_BIR_DATA VendorDataBlock;
  WINBIO_BIR_DATA SignatureBlock;
} WINBIO_BIR;
```



## <a name="members"></a><span data-ttu-id="de9ea-108">Members</span><span class="sxs-lookup"><span data-stu-id="de9ea-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="de9ea-109">**HeaderBlock**</span><span class="sxs-lookup"><span data-stu-id="de9ea-109">**HeaderBlock**</span></span>
</dt> <dd>

<span data-ttu-id="de9ea-110">Struttura [**di \_ \_ dati WINBIO bir**](winbio-bir-data.md) che contiene le dimensioni, in byte, e l'offset dell'intestazione Bir.</span><span class="sxs-lookup"><span data-stu-id="de9ea-110">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of the BIR header.</span></span> <span data-ttu-id="de9ea-111">L'intestazione contiene informazioni che descrivono il contenuto del record di informazioni.</span><span class="sxs-lookup"><span data-stu-id="de9ea-111">The header contains information that describes the contents of the information record.</span></span>

</dd> <dt>

<span data-ttu-id="de9ea-112">**StandardDataBlock**</span><span class="sxs-lookup"><span data-stu-id="de9ea-112">**StandardDataBlock**</span></span>
</dt> <dd>

<span data-ttu-id="de9ea-113">Struttura [**di \_ \_ dati WINBIO bir**](winbio-bir-data.md) che contiene le dimensioni, in byte, e l'offset delle informazioni biometriche elaborate o non elaborate create dal Windows Biometric Framework (WBF).</span><span class="sxs-lookup"><span data-stu-id="de9ea-113">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of processed or unprocessed biometric information created by the Windows Biometric Framework (WBF).</span></span>

</dd> <dt>

<span data-ttu-id="de9ea-114">**VendorDataBlock**</span><span class="sxs-lookup"><span data-stu-id="de9ea-114">**VendorDataBlock**</span></span>
</dt> <dd>

<span data-ttu-id="de9ea-115">Una struttura di [**\_ \_ dati WINBIO bir**](winbio-bir-data.md) che contiene le dimensioni, in byte e l'offset delle informazioni biometriche elaborate o non elaborate fornite dai sensori e dal software del fornitore.</span><span class="sxs-lookup"><span data-stu-id="de9ea-115">A [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of processed or unprocessed biometric information provided by vendor sensors and software.</span></span>

</dd> <dt>

<span data-ttu-id="de9ea-116">**SignatureBlock**</span><span class="sxs-lookup"><span data-stu-id="de9ea-116">**SignatureBlock**</span></span>
</dt> <dd>

<span data-ttu-id="de9ea-117">Struttura di [**\_ \_ dati WINBIO bir**](winbio-bir-data.md) facoltativa che contiene la dimensione, in byte, e l'offset del codice Mac (Digital Signature Message Authentication Code) che può essere usato per verificare l'integrità di Bir.</span><span class="sxs-lookup"><span data-stu-id="de9ea-117">An optional [**WINBIO\_BIR\_DATA**](winbio-bir-data.md) structure that contains the size, in bytes, and offset of the digital signature message authentication code (MAC) that can be used to verify the integrity of the BIR.</span></span> <span data-ttu-id="de9ea-118">Se presente, la firma o il MAC deve coprire l'intestazione e i blocchi di dati.</span><span class="sxs-lookup"><span data-stu-id="de9ea-118">If present, the signature or MAC must cover the header and data blocks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de9ea-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="de9ea-119">Remarks</span></span>

<span data-ttu-id="de9ea-120">L'uso degli offset anziché dei puntatori consente una semplice serializzazione di BIR e per una conversione meno complessa tra gli ambienti 32 e 64 bit o tra l'utente e la modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="de9ea-120">The use of offsets rather than pointers allows for easy serialization of the BIR and for less complicated translation between 32 and 64-bit environments or between user and kernel mode.</span></span>

<span data-ttu-id="de9ea-121">BIR è compatibile con il comune CBEFF (Biometric Exchange Format Framework) definito da NIST 6529-A.</span><span class="sxs-lookup"><span data-stu-id="de9ea-121">The BIR is compatible with the Common Biometric Exchange Format Framework (CBEFF) defined by NIST 6529-A.</span></span>

<span data-ttu-id="de9ea-122">Se questa struttura contiene un valore *StandardDataBlock* , il parametro di *tipo* dell'intestazione specificata dal parametro *HeaderBlock* deve essere impostato sul **\_ \_ \_ \_ tipo di formato WINBIO ANSI 381**.</span><span class="sxs-lookup"><span data-stu-id="de9ea-122">If this structure contains a *StandardDataBlock* value, the *Type* parameter of the header specified by the *HeaderBlock* parameter must be set to **WINBIO\_ANSI\_381\_FORMAT\_TYPE**.</span></span> <span data-ttu-id="de9ea-123">Questo è l'unico formato dati standard supportato dalla versione corrente del Windows Biometric Framework.</span><span class="sxs-lookup"><span data-stu-id="de9ea-123">This is the only standard data format supported by the current version of the Windows Biometric Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="de9ea-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de9ea-124">Requirements</span></span>



| <span data-ttu-id="de9ea-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="de9ea-125">Requirement</span></span> | <span data-ttu-id="de9ea-126">Valore</span><span class="sxs-lookup"><span data-stu-id="de9ea-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de9ea-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de9ea-127">Minimum supported client</span></span><br/> | <span data-ttu-id="de9ea-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="de9ea-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="de9ea-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de9ea-129">Minimum supported server</span></span><br/> | <span data-ttu-id="de9ea-130">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="de9ea-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="de9ea-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de9ea-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="de9ea-132"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de9ea-132"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de9ea-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de9ea-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de9ea-134">Strutture delle applicazioni client</span><span class="sxs-lookup"><span data-stu-id="de9ea-134">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="de9ea-135">**\_dati WINBIO bir \_**</span><span class="sxs-lookup"><span data-stu-id="de9ea-135">**WINBIO\_BIR\_DATA**</span></span>](winbio-bir-data.md)
</dt> <dt>

[<span data-ttu-id="de9ea-136">**\_intestazione WINBIO bir \_**</span><span class="sxs-lookup"><span data-stu-id="de9ea-136">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





