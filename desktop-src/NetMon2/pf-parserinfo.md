---
description: La \_ struttura PF PARSERINFO definisce un parser alla volta. Nella struttura PF \_ PARSERINFO un parser viene definito dalle informazioni sul protocollo rilevato dal parser.
ms.assetid: e1180952-9560-4386-9320-919dfb8171b3
title: Struttura PF_PARSERINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 28ebeaad31e6f40ceb961d8c303a22590966947f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314750"
---
# <a name="pf_parserinfo-structure"></a><span data-ttu-id="04969-104">\_Struttura PF PARSERINFO</span><span class="sxs-lookup"><span data-stu-id="04969-104">PF\_PARSERINFO structure</span></span>

<span data-ttu-id="04969-105">La struttura **PF \_ PARSERINFO** definisce un parser alla volta.</span><span class="sxs-lookup"><span data-stu-id="04969-105">The **PF\_PARSERINFO** structure defines one parser at a time.</span></span> <span data-ttu-id="04969-106">Nella struttura **PF \_ PARSERINFO** un parser viene definito dalle informazioni sul protocollo rilevato dal parser.</span><span class="sxs-lookup"><span data-stu-id="04969-106">In the **PF\_PARSERINFO** structure, a parser is defined by the information about the protocol that the parser detects.</span></span>

## <a name="syntax"></a><span data-ttu-id="04969-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04969-107">Syntax</span></span>


```C++
typedef struct _PF_PARSERINFO {
  char           szProtocolName[MAX_PROTOCOL_NAME_LEN];
  char           szComment[MAX_PROTOCOL_COMMENT_LEN];
  char           szHelpFile[MAX_PATH];
  PPF_FOLLOWSET  pWhoCanPrecedeMe;
  PPF_FOLLOWSET  pWhoCanFollowMe;
  PPF_HANDOFFSET pWhoHandsOffToMe;
  PPF_HANDOFFSET pWhoDoIHandOffTo;
} PF_PARSERINFO, *PPF_PARSERINFO;
```



## <a name="members"></a><span data-ttu-id="04969-108">Members</span><span class="sxs-lookup"><span data-stu-id="04969-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="04969-109">**szProtocolName**</span><span class="sxs-lookup"><span data-stu-id="04969-109">**szProtocolName**</span></span>
</dt> <dd>

<span data-ttu-id="04969-110">Nome del protocollo rilevato dal parser.</span><span class="sxs-lookup"><span data-stu-id="04969-110">Name of the protocol that the parser detects.</span></span>

</dd> <dt>

<span data-ttu-id="04969-111">**szComment**</span><span class="sxs-lookup"><span data-stu-id="04969-111">**szComment**</span></span>
</dt> <dd>

<span data-ttu-id="04969-112">Breve descrizione del protocollo.</span><span class="sxs-lookup"><span data-stu-id="04969-112">Brief description of the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="04969-113">**szHelpFile**</span><span class="sxs-lookup"><span data-stu-id="04969-113">**szHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="04969-114">Nome del file della guida del protocollo, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="04969-114">Name of the protocol Help file, if any.</span></span>

</dd> <dt>

<span data-ttu-id="04969-115">**pWhoCanPrecedeMe**</span><span class="sxs-lookup"><span data-stu-id="04969-115">**pWhoCanPrecedeMe**</span></span>
</dt> <dd>

<span data-ttu-id="04969-116">Puntatore a una struttura [PF \_ follower](pf-followset.md) che elenca i protocolli che possono precedere il protocollo descritto dalla struttura **PF \_ PARSERINFO** .</span><span class="sxs-lookup"><span data-stu-id="04969-116">Pointer to a [PF\_FOLLOWSET](pf-followset.md) structure that lists the protocols that can precede the protocol the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="04969-117">Network Monitor aggiunge il protocollo del parser al [*set seguente*](f.md) di tutti i protocolli nel set.</span><span class="sxs-lookup"><span data-stu-id="04969-117">Network Monitor adds the parser protocol to the [*follow set*](f.md) of all the protocols in the set.</span></span>

</dd> <dt>

<span data-ttu-id="04969-118">**pWhoCanFollowMe**</span><span class="sxs-lookup"><span data-stu-id="04969-118">**pWhoCanFollowMe**</span></span>
</dt> <dd>

<span data-ttu-id="04969-119">Puntatore a una struttura [PF \_ follower](pf-followset.md) che elenca il protocollo che può seguire il protocollo descritto dalla struttura **PF \_ PARSERINFO** .</span><span class="sxs-lookup"><span data-stu-id="04969-119">Pointer to a [PF\_FOLLOWSET](pf-followset.md) structure that lists the protocol that can follow the protocol the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="04969-120">Network Monitor aggiunge i protocolli del set al [*seguente set*](f.md) del protocollo del parser.</span><span class="sxs-lookup"><span data-stu-id="04969-120">Network Monitor adds the protocols of the set to the [*follow set*](f.md) of the parser protocol.</span></span>

</dd> <dt>

<span data-ttu-id="04969-121">**pWhoHandsOffToMe**</span><span class="sxs-lookup"><span data-stu-id="04969-121">**pWhoHandsOffToMe**</span></span>
</dt> <dd>

<span data-ttu-id="04969-122">Puntatore a una struttura [PF \_ HANDOFFSET](pf-handoffset.md) che passa al protocollo descritto dalla struttura **PF \_ PARSERINFO** .</span><span class="sxs-lookup"><span data-stu-id="04969-122">Pointer to a [PF\_HANDOFFSET](pf-handoffset.md) structure that hands-off to the protocol that the **PF\_PARSERINFO** structure describes.</span></span> <span data-ttu-id="04969-123">Network Monitor aggiunge il protocollo del parser ai [*set*](h.md) di tutti i protocolli nel set.</span><span class="sxs-lookup"><span data-stu-id="04969-123">Network Monitor adds the parser protocol to the [*handoff sets*](h.md) of all the protocols in the set.</span></span>

</dd> <dt>

<span data-ttu-id="04969-124">**pWhoDoIHandOffTo**</span><span class="sxs-lookup"><span data-stu-id="04969-124">**pWhoDoIHandOffTo**</span></span>
</dt> <dd>

<span data-ttu-id="04969-125">Puntatore a una struttura [PF \_ HANDOFFSET](pf-handoffset.md) che elenca i protocolli a cui il protocollo del parser passa.</span><span class="sxs-lookup"><span data-stu-id="04969-125">Pointer to a [PF\_HANDOFFSET](pf-handoffset.md) structure that lists the protocols that the parser protocol hands off to.</span></span> <span data-ttu-id="04969-126">Network Monitor aggiunge i protocolli di questo set al [*set di continuità*](h.md) del protocollo del parser.</span><span class="sxs-lookup"><span data-stu-id="04969-126">Network Monitor adds the protocols of this set to the [*handoff set*](h.md) of the parser protocol.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04969-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="04969-127">Remarks</span></span>

<span data-ttu-id="04969-128">La struttura **PF \_ PARSERINFO** viene usata nella struttura **PF \_ PARSERDLLINFO** per fornire una descrizione di un parser.</span><span class="sxs-lookup"><span data-stu-id="04969-128">The **PF\_PARSERINFO** structure is used in the **PF\_PARSERDLLINFO** structure to provide a description of a parser.</span></span> <span data-ttu-id="04969-129">Network Monitor usa la descrizione del parser per aggiornare il file di [*Parser.ini*](p.md) e i file ini dei parser che precedono e seguono il protocollo descritto nella struttura **PF \_ PARSERINFO** .</span><span class="sxs-lookup"><span data-stu-id="04969-129">Network Monitor uses the parser description to update the [*Parser.ini*](p.md) file, and the INI files of the parsers that precede and follow the protocol described in the **PF\_PARSERINFO** structure.</span></span>

<span data-ttu-id="04969-130">Un set di seguito specifica i protocolli che seguono un protocollo.</span><span class="sxs-lookup"><span data-stu-id="04969-130">A follow set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="04969-131">Network Monitor utilizza un set di seguito quando il parser non è in grado di identificare il protocollo successivo tra i dati in un'istanza del protocollo.</span><span class="sxs-lookup"><span data-stu-id="04969-131">Network Monitor uses a follow set when the parser cannot identify the next protocol from the data in a protocol instance.</span></span> <span data-ttu-id="04969-132">Un set di seguito viene archiviato nel file di [*Parser.ini*](p.md) .</span><span class="sxs-lookup"><span data-stu-id="04969-132">A follow set is stored in the [*Parser.ini*](p.md) file.</span></span> <span data-ttu-id="04969-133">Quando il parser viene installato per la prima volta, Network Monitor aggiorna il set seguente di protocolli del parser elencati in **pWhoCanPrecedeMe** e **pWhoCanFollowMe**.</span><span class="sxs-lookup"><span data-stu-id="04969-133">When the parser is installed for the first time, Network Monitor updates the follow set of the parser protocols that are listed in **pWhoCanPrecedeMe** and **pWhoCanFollowMe**.</span></span>

<span data-ttu-id="04969-134">Un set di continuità specifica i protocolli che seguono un protocollo.</span><span class="sxs-lookup"><span data-stu-id="04969-134">A handoff set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="04969-135">Il parser utilizza un set di continuità solo quando il parser è in grado di identificare il protocollo successivo tra i dati in un'istanza del protocollo.</span><span class="sxs-lookup"><span data-stu-id="04969-135">The parser uses a handoff set only when the parser can identify the next protocol from the data in a protocol instance.</span></span> <span data-ttu-id="04969-136">Un set di continuità viene archiviato nei file INI di ogni parser.</span><span class="sxs-lookup"><span data-stu-id="04969-136">A handoff set is stored in the INI files of each parser.</span></span> <span data-ttu-id="04969-137">Quando il parser viene installato per la prima volta, Network Monitor aggiorna il set di protocolli di parser elencati in **pWhoHandsOffToMe** e **pWhoDoIHandOffTo**.</span><span class="sxs-lookup"><span data-stu-id="04969-137">When the parser is installed for the first time, Network Monitor updates the handoff set of the parser protocols that are listed in **pWhoHandsOffToMe** and **pWhoDoIHandOffTo**.</span></span>



| <span data-ttu-id="04969-138">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="04969-138">For information on</span></span>                                               | <span data-ttu-id="04969-139">Vedere</span><span class="sxs-lookup"><span data-stu-id="04969-139">See</span></span>                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="04969-140">Quali sono i parser e come funzionano con Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="04969-140">What parsers are, and how they work with Network Monitor.</span></span>        | [<span data-ttu-id="04969-141">Parser</span><span class="sxs-lookup"><span data-stu-id="04969-141">Parsers</span></span>](parsers.md)                                                       |
| <span data-ttu-id="04969-142">Elementi che seguono i set.</span><span class="sxs-lookup"><span data-stu-id="04969-142">What follow sets contain.</span></span>                                        | [<span data-ttu-id="04969-143">Specifica di un set di seguito</span><span class="sxs-lookup"><span data-stu-id="04969-143">Specifying a Follow Set</span></span>](specifying-a-follow-set.md)                       |
| <span data-ttu-id="04969-144">Elementi inclusi nei set di continuità.</span><span class="sxs-lookup"><span data-stu-id="04969-144">What handoff sets contain.</span></span>                                       | [<span data-ttu-id="04969-145">Specifica di un set di continuità</span><span class="sxs-lookup"><span data-stu-id="04969-145">Specifying a Handoff Set</span></span>](specifying-a-handoff-set.md)                     |
| <span data-ttu-id="04969-146">Punti di ingresso inclusi nella DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="04969-146">What entry points are included in the parser DLL.</span></span>                | [<span data-ttu-id="04969-147">Architettura DLL parser</span><span class="sxs-lookup"><span data-stu-id="04969-147">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                       |
| <span data-ttu-id="04969-148">L'implementazione di **ParserAutoInstallInfo**  include un esempio.</span><span class="sxs-lookup"><span data-stu-id="04969-148">How to implement **ParserAutoInstallInfo**  includes an example.</span></span> | [<span data-ttu-id="04969-149">Implementazione di ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="04969-149">Implementing ParserAutoInstallInfo</span></span>](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a><span data-ttu-id="04969-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04969-150">Requirements</span></span>



| <span data-ttu-id="04969-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="04969-151">Requirement</span></span> | <span data-ttu-id="04969-152">Valore</span><span class="sxs-lookup"><span data-stu-id="04969-152">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="04969-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04969-153">Minimum supported client</span></span><br/> | <span data-ttu-id="04969-154">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="04969-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="04969-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04969-155">Minimum supported server</span></span><br/> | <span data-ttu-id="04969-156">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="04969-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="04969-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04969-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="04969-158"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="04969-158"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04969-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04969-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04969-160">ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="04969-160">ParserAutoInstallInfo</span></span>](parserautoinstallinfo.md)
</dt> <dt>

[<span data-ttu-id="04969-161">PF \_</span><span class="sxs-lookup"><span data-stu-id="04969-161">PF\_FOLLOWSET</span></span>](pf-followset.md)
</dt> <dt>

[<span data-ttu-id="04969-162">PF \_ HANDOFFSET</span><span class="sxs-lookup"><span data-stu-id="04969-162">PF\_HANDOFFSET</span></span>](pf-handoffset.md)
</dt> <dt>

[<span data-ttu-id="04969-163">PF \_ PARSERDLLINFO</span><span class="sxs-lookup"><span data-stu-id="04969-163">PF\_PARSERDLLINFO</span></span>](pf-parserdllinfo.md)
</dt> </dl>

 

 




