---
description: La \_ struttura PF HANDOFFENTRY definisce un protocollo che Network Monitor aggiunge al set di continuità di un parser.
ms.assetid: c26bee6e-7dbf-4994-a0a7-a280cf4838be
title: Struttura PF_HANDOFFENTRY (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5ad431e936265be96831778f9949ae67ef737beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314752"
---
# <a name="pf_handoffentry-structure"></a><span data-ttu-id="3e77c-103">\_Struttura PF HANDOFFENTRY</span><span class="sxs-lookup"><span data-stu-id="3e77c-103">PF\_HANDOFFENTRY structure</span></span>

<span data-ttu-id="3e77c-104">La struttura **PF \_ HANDOFFENTRY** definisce un protocollo che Network Monitor aggiunge al set di continuità di un parser.</span><span class="sxs-lookup"><span data-stu-id="3e77c-104">The **PF\_HANDOFFENTRY** structure defines a protocol that Network Monitor adds to the handoff set of a parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e77c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e77c-105">Syntax</span></span>


```C++
typedef struct _PF_HANDOFFENTRY {
  char                      szIniFile[MAX_PATH];
  char                      szIniSection[MAX_PATH];
  char                      szProtocol[MAX_PROTOCOL_NAME_LEN];
  DWORD                     dwHandOffValue;
  PF_HANDOFFVALUEFORMATBASE ValueFormatBase;
} PF_HANDOFFENTRY, *PPF_HANDOFFENTRY;
```



## <a name="members"></a><span data-ttu-id="3e77c-106">Members</span><span class="sxs-lookup"><span data-stu-id="3e77c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3e77c-107">**szIniFile**</span><span class="sxs-lookup"><span data-stu-id="3e77c-107">**szIniFile**</span></span>
</dt> <dd>

<span data-ttu-id="3e77c-108">Nome del file INI associato al protocollo.</span><span class="sxs-lookup"><span data-stu-id="3e77c-108">Name of the INI file associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="3e77c-109">**szIniSection**</span><span class="sxs-lookup"><span data-stu-id="3e77c-109">**szIniSection**</span></span>
</dt> <dd>

<span data-ttu-id="3e77c-110">Etichetta della sezione all'interno del file INI.</span><span class="sxs-lookup"><span data-stu-id="3e77c-110">Section label within the INI file.</span></span>

</dd> <dt>

<span data-ttu-id="3e77c-111">**szProtocol**</span><span class="sxs-lookup"><span data-stu-id="3e77c-111">**szProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="3e77c-112">Nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="3e77c-112">Name of the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="3e77c-113">**dwHandOffValue**</span><span class="sxs-lookup"><span data-stu-id="3e77c-113">**dwHandOffValue**</span></span>
</dt> <dd>

<span data-ttu-id="3e77c-114">Valore associato al protocollo.</span><span class="sxs-lookup"><span data-stu-id="3e77c-114">Value associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="3e77c-115">**ValueFormatBase**</span><span class="sxs-lookup"><span data-stu-id="3e77c-115">**ValueFormatBase**</span></span>
</dt> <dd>

<span data-ttu-id="3e77c-116">Base numerica del valore del protocollo specificato in **dwHandOffValue**.</span><span class="sxs-lookup"><span data-stu-id="3e77c-116">Numeric base of the protocol value that is specified in **dwHandOffValue**.</span></span> <span data-ttu-id="3e77c-117">La funzione **ValueFormatBase** deve essere impostata su uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="3e77c-117">The **ValueFormatBase** function must be set to one of the following:</span></span>



| <span data-ttu-id="3e77c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3e77c-118">Value</span></span>                                                                                                                                                                                                                        | <span data-ttu-id="3e77c-119">Significato</span><span class="sxs-lookup"><span data-stu-id="3e77c-119">Meaning</span></span>                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="HANDOFF_VALUE_FORMAT_BASE_UNKNOWN"></span><span id="handoff_value_format_base_unknown"></span><dl> <span data-ttu-id="3e77c-120"><dt>**\_ \_ base formato valore \_ uniforme \_ sconosciuto**</dt></span><span class="sxs-lookup"><span data-stu-id="3e77c-120"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="3e77c-121">Base sconosciuta</span><span class="sxs-lookup"><span data-stu-id="3e77c-121">Unknown base</span></span><br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_DECIMAL"></span><span id="handoff_value_format_base_decimal"></span><dl> <span data-ttu-id="3e77c-122"><dt>**\_ \_ \_ decimale base \_ formato valore uniforme**</dt></span><span class="sxs-lookup"><span data-stu-id="3e77c-122"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_DECIMAL**</dt></span></span> </dl> | <span data-ttu-id="3e77c-123">Base decimale</span><span class="sxs-lookup"><span data-stu-id="3e77c-123">Decimal base</span></span><br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_HEX"></span><span id="handoff_value_format_base_hex"></span><dl> <span data-ttu-id="3e77c-124"><dt>**\_ \_ \_ Hex base formato valore \_ uniforme**</dt></span><span class="sxs-lookup"><span data-stu-id="3e77c-124"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_HEX**</dt></span></span> </dl>             | <span data-ttu-id="3e77c-125">Base esadecimale</span><span class="sxs-lookup"><span data-stu-id="3e77c-125">Hexadecimal base</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e77c-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e77c-126">Remarks</span></span>

<span data-ttu-id="3e77c-127">Una matrice di strutture **PF \_ HANDOFFENTRY** viene usata nella struttura [PF \_ HANDOFFSET](pf-handoffset.md) .</span><span class="sxs-lookup"><span data-stu-id="3e77c-127">An array of the **PF\_HANDOFFENTRY** structures is used in the [PF\_HANDOFFSET](pf-handoffset.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e77c-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e77c-128">Requirements</span></span>



| <span data-ttu-id="3e77c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e77c-129">Requirement</span></span> | <span data-ttu-id="3e77c-130">Valore</span><span class="sxs-lookup"><span data-stu-id="3e77c-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3e77c-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e77c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3e77c-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3e77c-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3e77c-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e77c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3e77c-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3e77c-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3e77c-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e77c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e77c-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e77c-136"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e77c-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e77c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e77c-138">PF \_ HANDOFFSET</span><span class="sxs-lookup"><span data-stu-id="3e77c-138">PF\_HANDOFFSET</span></span>](pf-handoffset.md)
</dt> </dl>

 

 




