---
description: Definisce un singolo oggetto di un filtro di visualizzazione.
ms.assetid: 865b55f3-9294-43c5-b4dc-eb5128ce3a38
title: Struttura FILTEROBJECT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILTEROBJECT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7649ab294f2ecad90946926dcc68d6937b357666
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305934"
---
# <a name="filterobject-structure"></a><span data-ttu-id="c0b79-103">Struttura FILTEROBJECT</span><span class="sxs-lookup"><span data-stu-id="c0b79-103">FILTEROBJECT structure</span></span>

<span data-ttu-id="c0b79-104">La struttura **FILTEROBJECT** definisce un singolo oggetto di un filtro di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c0b79-104">The **FILTEROBJECT** structure defines a single object of a display filter.</span></span> <span data-ttu-id="c0b79-105">La funzione [**FilterAddObject**](filteraddobject.md) USA **FILTEROBJECT** per creare un filtro di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="c0b79-105">The [**FilterAddObject**](filteraddobject.md) function uses **FILTEROBJECT** to build a display filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0b79-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0b79-106">Syntax</span></span>


```C++
typedef struct _FILTEROBJECT {
  FILTERACTIONTYPE     Action;
  HPROPERTY            hProperty;
  union {
    VALUETYPE           Value;
    HPROTOCOL           hProtocol;
    LPVOID              lpArray;
    LPPROTOCOLTABLETYPE lpProtocolTable;
    LPADDRESS           lpAddress;
    ULPLARGEINT         lpLargeInt;
    ULPTIME             lpTime;
    LPOBJECT_IDENTIFIER lpOID;
  };
  union {
    WORD ByteCount;
    WORD ByteOffset;
  };
  struct _FILTEROBJECT  *pNext;
} FILTEROBJECT, *LPFILTEROBJECT;
```



## <a name="members"></a><span data-ttu-id="c0b79-107">Members</span><span class="sxs-lookup"><span data-stu-id="c0b79-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c0b79-108">**Azione**</span><span class="sxs-lookup"><span data-stu-id="c0b79-108">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="c0b79-109">Flag che specifica l'azione **FILTEROBJECT** .</span><span class="sxs-lookup"><span data-stu-id="c0b79-109">Flag that specifies the **FILTEROBJECT** action.</span></span> <span data-ttu-id="c0b79-110">Un flag può specificare una proprietà, un valore o un operatore.</span><span class="sxs-lookup"><span data-stu-id="c0b79-110">A flag can specify a property, value, or operator.</span></span>

<span data-ttu-id="c0b79-111">Nella tabella seguente sono elencati i flag delle proprietà dei membri di azione.</span><span class="sxs-lookup"><span data-stu-id="c0b79-111">The following table lists Action member property flags.</span></span>



| <span data-ttu-id="c0b79-112">Valore</span><span class="sxs-lookup"><span data-stu-id="c0b79-112">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="c0b79-113">Significato</span><span class="sxs-lookup"><span data-stu-id="c0b79-113">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="FILTERACTION_PROPERTY"></span><span id="filteraction_property"></span><dl> <span data-ttu-id="c0b79-114"><dt>**\_Proprietà FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-114"><dt>**FILTERACTION\_PROPERTY**</dt></span></span> </dl>                | <span data-ttu-id="c0b79-115">Contiene questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="c0b79-115">Contains this property.</span></span><br/>                                     |
| <span id="FILTERACTION_PROPERTYEXIST"></span><span id="filteraction_propertyexist"></span><dl> <span data-ttu-id="c0b79-116"><dt>**\_PROPERTYEXIST FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-116"><dt>**FILTERACTION\_PROPERTYEXIST**</dt></span></span> </dl> | <span data-ttu-id="c0b79-117">Indica che una proprietà di azione filtro è già definita.</span><span class="sxs-lookup"><span data-stu-id="c0b79-117">Indicates that a filter action property is already defined.</span></span><br/> |



 

<span data-ttu-id="c0b79-118">Nella tabella seguente sono elencati i flag dei valori dei membri di azione.</span><span class="sxs-lookup"><span data-stu-id="c0b79-118">The following table lists Action member value flags.</span></span>



| <span data-ttu-id="c0b79-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c0b79-119">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="c0b79-120">Significato</span><span class="sxs-lookup"><span data-stu-id="c0b79-120">Meaning</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="FILTERACTION_VALUE"></span><span id="filteraction_value"></span><dl> <span data-ttu-id="c0b79-121"><dt>**\_valore FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-121"><dt>**FILTERACTION\_VALUE**</dt></span></span> </dl>                 | <span data-ttu-id="c0b79-122">Contiene questo valore.</span><span class="sxs-lookup"><span data-stu-id="c0b79-122">Contains this value.</span></span><br/>                                             |
| <span id="FILTERACTION_STRING"></span><span id="filteraction_string"></span><dl> <span data-ttu-id="c0b79-123"><dt>**\_stringa FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-123"><dt>**FILTERACTION\_STRING**</dt></span></span> </dl>              | <span data-ttu-id="c0b79-124">Contiene questa stringa.</span><span class="sxs-lookup"><span data-stu-id="c0b79-124">Contains this string.</span></span><br/>                                            |
| <span id="FILTERACTION_ARRAY"></span><span id="filteraction_array"></span><dl> <span data-ttu-id="c0b79-125"><dt>**\_matrice FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-125"><dt>**FILTERACTION\_ARRAY**</dt></span></span> </dl>                 | <span data-ttu-id="c0b79-126">Contiene questa matrice.</span><span class="sxs-lookup"><span data-stu-id="c0b79-126">Contains this array.</span></span><br/>                                             |
| <span id="FILTERACTION_CONTAINSNC"></span><span id="filteraction_containsnc"></span><dl> <span data-ttu-id="c0b79-127"><dt>**\_CONTAINSNC FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-127"><dt>**FILTERACTION\_CONTAINSNC**</dt></span></span> </dl>  | <span data-ttu-id="c0b79-128">Indica che una proprietà contiene una sottostringa senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c0b79-128">Indicates that a property contains a case-insensitive substring.</span></span><br/> |
| <span id="FILTERACTION_CONTAINS"></span><span id="filteraction_contains"></span><dl> <span data-ttu-id="c0b79-129"><dt>**FILTERACTION \_ contiene**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-129"><dt>**FILTERACTION\_CONTAINS**</dt></span></span> </dl>        | <span data-ttu-id="c0b79-130">Indica che una proprietà contiene una sottostringa con distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c0b79-130">Indicates that a property contains a case sensitive substring.</span></span><br/>   |
| <span id="FILTERACTION_ADDRESS"></span><span id="filteraction_address"></span><dl> <span data-ttu-id="c0b79-131"><dt>**\_Indirizzo FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-131"><dt>**FILTERACTION\_ADDRESS**</dt></span></span> </dl>           | <span data-ttu-id="c0b79-132">Contiene l'indirizzo MAC.</span><span class="sxs-lookup"><span data-stu-id="c0b79-132">Contains the MAC address.</span></span><br/>                                        |
| <span id="FILTERACTION_ADDRESSANY"></span><span id="filteraction_addressany"></span><dl> <span data-ttu-id="c0b79-133"><dt>**\_ADDRESSANY FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-133"><dt>**FILTERACTION\_ADDRESSANY**</dt></span></span> </dl>  | <span data-ttu-id="c0b79-134">Corrisponde a qualsiasi indirizzo MAC.</span><span class="sxs-lookup"><span data-stu-id="c0b79-134">Matches any MAC address.</span></span><br/>                                         |
| <span id="FILTERACTION_FROM"></span><span id="filteraction_from"></span><dl> <span data-ttu-id="c0b79-135"><dt>**FILTERACTION \_ da**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-135"><dt>**FILTERACTION\_FROM**</dt></span></span> </dl>                    | <span data-ttu-id="c0b79-136">Indica l'indirizzo **Mac da** .</span><span class="sxs-lookup"><span data-stu-id="c0b79-136">Indicates the **From MAC** address.</span></span><br/>                              |
| <span id="FILTERACTION_TO"></span><span id="filteraction_to"></span><dl> <span data-ttu-id="c0b79-137"><dt>**FILTERACTION \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-137"><dt>**FILTERACTION\_TO**</dt></span></span> </dl>                          | <span data-ttu-id="c0b79-138">Indica l'indirizzo **Mac** .</span><span class="sxs-lookup"><span data-stu-id="c0b79-138">Indicates the **To MAC** address.</span></span><br/>                                |
| <span id="FILTERACTION_FROMTO"></span><span id="filteraction_fromto"></span><dl> <span data-ttu-id="c0b79-139"><dt>**\_FROMTO FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-139"><dt>**FILTERACTION\_FROMTO**</dt></span></span> </dl>              | <span data-ttu-id="c0b79-140">Indica un'associazione **tra/** e di indirizzi Mac.</span><span class="sxs-lookup"><span data-stu-id="c0b79-140">Indicates a **From/To** pairing of MAC addresses.</span></span><br/>                |
| <span id="FILTERACTION_LARGEINT"></span><span id="filteraction_largeint"></span><dl> <span data-ttu-id="c0b79-141"><dt>**\_largeInt FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-141"><dt>**FILTERACTION\_LARGEINT**</dt></span></span> </dl>        | <span data-ttu-id="c0b79-142">Contiene un numero intero grande.</span><span class="sxs-lookup"><span data-stu-id="c0b79-142">Contains a large integer.</span></span><br/>                                        |
| <span id="FILTERACTION_TIME"></span><span id="filteraction_time"></span><dl> <span data-ttu-id="c0b79-143"><dt>**FILTERACTION \_ tempo**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-143"><dt>**FILTERACTION\_TIME**</dt></span></span> </dl>                    | <span data-ttu-id="c0b79-144">Contiene una struttura **SYSTEMTIME** .</span><span class="sxs-lookup"><span data-stu-id="c0b79-144">Contains a **SYSTEMTIME** structure.</span></span><br/>                             |
| <span id="FILTERACTION_ADDR_ETHER"></span><span id="filteraction_addr_ether"></span><dl> <span data-ttu-id="c0b79-145"><dt>**FILTERACTION \_ addr \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-145"><dt>**FILTERACTION\_ADDR\_ETHER**</dt></span></span> </dl> | <span data-ttu-id="c0b79-146">Contiene un indirizzo MAC Ethernet.</span><span class="sxs-lookup"><span data-stu-id="c0b79-146">Contains an Ethernet MAC address.</span></span><br/>                                |
| <span id="FILTERACTION_ADDR_TOKEN"></span><span id="filteraction_addr_token"></span><dl> <span data-ttu-id="c0b79-147"><dt>**\_token addr \_ FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-147"><dt>**FILTERACTION\_ADDR\_TOKEN**</dt></span></span> </dl> | <span data-ttu-id="c0b79-148">Contiene un indirizzo MAC dell'anello di token.</span><span class="sxs-lookup"><span data-stu-id="c0b79-148">Contains a token ring MAC address.</span></span><br/>                               |
| <span id="FILTERACTION_ADDR_FDDI"></span><span id="filteraction_addr_fddi"></span><dl> <span data-ttu-id="c0b79-149"><dt>**FILTERACTION \_ addr \_ FDDI**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-149"><dt>**FILTERACTION\_ADDR\_FDDI**</dt></span></span> </dl>    | <span data-ttu-id="c0b79-150">Contiene un indirizzo MAC di FDDI.</span><span class="sxs-lookup"><span data-stu-id="c0b79-150">Contains a FDDI MAC address.</span></span><br/>                                     |
| <span id="FILTERACTION_ADDR_IPX"></span><span id="filteraction_addr_ipx"></span><dl> <span data-ttu-id="c0b79-151"><dt>**FILTERACTION \_ addr \_ IPX**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-151"><dt>**FILTERACTION\_ADDR\_IPX**</dt></span></span> </dl>       | <span data-ttu-id="c0b79-152">Contiene un indirizzo MAC IPX.</span><span class="sxs-lookup"><span data-stu-id="c0b79-152">Contains an IPX MAC address.</span></span><br/>                                     |
| <span id="FILTERACTION_ADDR_IP"></span><span id="filteraction_addr_ip"></span><dl> <span data-ttu-id="c0b79-153"><dt>**\_IP addr \_ FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-153"><dt>**FILTERACTION\_ADDR\_IP**</dt></span></span> </dl>          | <span data-ttu-id="c0b79-154">Contiene un indirizzo MAC IP.</span><span class="sxs-lookup"><span data-stu-id="c0b79-154">Contains an IP MAC address.</span></span><br/>                                      |
| <span id="FILTERACTION_OID"></span><span id="filteraction_oid"></span><dl> <span data-ttu-id="c0b79-155"><dt>**\_OID FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-155"><dt>**FILTERACTION\_OID**</dt></span></span> </dl>                       | <span data-ttu-id="c0b79-156">Contiene un identificatore di oggetto (OID).</span><span class="sxs-lookup"><span data-stu-id="c0b79-156">Contains an Object Identifier (OID).</span></span><br/>                             |



 

<span data-ttu-id="c0b79-157">Nella tabella seguente sono elencati i flag dell'operatore membro di azione.</span><span class="sxs-lookup"><span data-stu-id="c0b79-157">The following table lists Action member operator flags.</span></span>



| <span data-ttu-id="c0b79-158">Valore</span><span class="sxs-lookup"><span data-stu-id="c0b79-158">Value</span></span>                                                                                                                                                                                                        | <span data-ttu-id="c0b79-159">Significato</span><span class="sxs-lookup"><span data-stu-id="c0b79-159">Meaning</span></span>                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILTERACTION_INVALID"></span><span id="filteraction_invalid"></span><dl> <span data-ttu-id="c0b79-160"><dt>**FILTERACTION \_ non valido**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-160"><dt>**FILTERACTION\_INVALID**</dt></span></span> </dl>                           | <span data-ttu-id="c0b79-161">Indica un'azione di filtro non valida.</span><span class="sxs-lookup"><span data-stu-id="c0b79-161">Indicates an invalid filter action.</span></span><br/>                                                                                  |
| <span id="FILTERACTION_AND"></span><span id="filteraction_and"></span><dl> <span data-ttu-id="c0b79-162"><dt>**FILTERACTION \_ e**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-162"><dt>**FILTERACTION\_AND**</dt></span></span> </dl>                                       | <span data-ttu-id="c0b79-163">Indica un'istruzione **and** logica.</span><span class="sxs-lookup"><span data-stu-id="c0b79-163">Indicates a logical **AND** statement.</span></span><br/>                                                                               |
| <span id="FILTERACTION_OR"></span><span id="filteraction_or"></span><dl> <span data-ttu-id="c0b79-164"><dt>**FILTERACTION \_ o**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-164"><dt>**FILTERACTION\_OR**</dt></span></span> </dl>                                          | <span data-ttu-id="c0b79-165">Indica un'istruzione **or** logica.</span><span class="sxs-lookup"><span data-stu-id="c0b79-165">Indicates a logical **OR** statement.</span></span><br/>                                                                                |
| <span id="FILTERACTION_XOR"></span><span id="filteraction_xor"></span><dl> <span data-ttu-id="c0b79-166"><dt>**\_Xor FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-166"><dt>**FILTERACTION\_XOR**</dt></span></span> </dl>                                       | <span data-ttu-id="c0b79-167">Indica un'istruzione **or** esclusivo logica (XOR).</span><span class="sxs-lookup"><span data-stu-id="c0b79-167">Indicates a logical exclusive **OR** (XOR) statement.</span></span><br/>                                                                |
| <span id="FILTERACTION_NOT"></span><span id="filteraction_not"></span><dl> <span data-ttu-id="c0b79-168"><dt>**FILTERACTION \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-168"><dt>**FILTERACTION\_NOT**</dt></span></span> </dl>                                       | <span data-ttu-id="c0b79-169">Indica un'istruzione **not** logica.</span><span class="sxs-lookup"><span data-stu-id="c0b79-169">Indicates a logical **NOT** statement.</span></span><br/>                                                                               |
| <span id="FILTERACTION_EQUALNC"></span><span id="filteraction_equalnc"></span><dl> <span data-ttu-id="c0b79-170"><dt>**\_EQUALNC FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-170"><dt>**FILTERACTION\_EQUALNC**</dt></span></span> </dl>                           | <span data-ttu-id="c0b79-171">L'azione filtro è uguale e senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c0b79-171">Filter action is equal and case insensitive.</span></span><br/>                                                                         |
| <span id="FILTERACTION_EQUAL"></span><span id="filteraction_equal"></span><dl> <span data-ttu-id="c0b79-172"><dt>**FILTERACTION \_ uguale a**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-172"><dt>**FILTERACTION\_EQUAL**</dt></span></span> </dl>                                 | <span data-ttu-id="c0b79-173">L'azione filtro è uguale e maiuscole/minuscole.</span><span class="sxs-lookup"><span data-stu-id="c0b79-173">Filter action is equal and case sensitive.</span></span><br/>                                                                           |
| <span id="FILTERACTION_NOTEQUALNC"></span><span id="filteraction_notequalnc"></span><dl> <span data-ttu-id="c0b79-174"><dt>**\_NOTEQUALNC FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-174"><dt>**FILTERACTION\_NOTEQUALNC**</dt></span></span> </dl>                  | <span data-ttu-id="c0b79-175">L'istruzione NOT logica è uguale e **senza** distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c0b79-175">Logical **NOT** statement is equal and case insensitive.</span></span><br/>                                                             |
| <span id="FILTERACTION_NOTEQUAL"></span><span id="filteraction_notequal"></span><dl> <span data-ttu-id="c0b79-176"><dt>**\_NOTEQUAL FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-176"><dt>**FILTERACTION\_NOTEQUAL**</dt></span></span> </dl>                        | <span data-ttu-id="c0b79-177">L'istruzione **not** logica è uguale e fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c0b79-177">Logical **NOT** statement is equal and is case sensitive.</span></span><br/>                                                            |
| <span id="FILTERACTION_GREATERNC"></span><span id="filteraction_greaternc"></span><dl> <span data-ttu-id="c0b79-178"><dt>**\_GREATERNC FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-178"><dt>**FILTERACTION\_GREATERNC**</dt></span></span> </dl>                     | <span data-ttu-id="c0b79-179">L'azione di filtro è maggiore di (>) e senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c0b79-179">Filter action is greater than (>) and case insensitive.</span></span><br/>                                                           |
| <span id="FILTERACTION_GREATER"></span><span id="filteraction_greater"></span><dl> <span data-ttu-id="c0b79-180"><dt>**FILTERACTION \_ maggiore**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-180"><dt>**FILTERACTION\_GREATER**</dt></span></span> </dl>                           | <span data-ttu-id="c0b79-181">L'azione di filtro è maggiore di (>) e distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c0b79-181">Filter action is greater than (>) and case sensitive.</span></span><br/>                                                             |
| <span id="FILTERACTION_LESSNC"></span><span id="filteraction_lessnc"></span><dl> <span data-ttu-id="c0b79-182"><dt>**\_LESSNC FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-182"><dt>**FILTERACTION\_LESSNC**</dt></span></span> </dl>                              | <span data-ttu-id="c0b79-183">L'azione di filtro è minore di (<) e senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c0b79-183">Filter action is less than (<) and case insensitive.</span></span><br/>                                                              |
| <span id="FILTERACTION_LESS"></span><span id="filteraction_less"></span><dl> <span data-ttu-id="c0b79-184"><dt>**FILTERACTION \_ less**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-184"><dt>**FILTERACTION\_LESS**</dt></span></span> </dl>                                    | <span data-ttu-id="c0b79-185">L'azione di filtro è minore di (<) e distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c0b79-185">Filter action is less than (<) and case sensitive.</span></span><br/>                                                                |
| <span id="FILTERACTION_GREATEREQUALNC"></span><span id="filteraction_greaterequalnc"></span><dl> <span data-ttu-id="c0b79-186"><dt>**\_GREATEREQUALNC FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-186"><dt>**FILTERACTION\_GREATEREQUALNC**</dt></span></span> </dl>      | <span data-ttu-id="c0b79-187">L'azione di filtro è maggiore o uguale a (>=) e senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c0b79-187">Filter action is greater than or equal to (>=) and case insensitive.</span></span><br/>                                              |
| <span id="FILTERACTION_GREATEREQUAL"></span><span id="filteraction_greaterequal"></span><dl> <span data-ttu-id="c0b79-188"><dt>**\_GREATEREQUAL FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-188"><dt>**FILTERACTION\_GREATEREQUAL**</dt></span></span> </dl>            | <span data-ttu-id="c0b79-189">L'azione di filtro è maggiore o uguale a (>=) e con distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c0b79-189">Filter action is greater than or equal to (>=) and case sensitive.</span></span><br/>                                                |
| <span id="FILTERACTION_LESSEQUALNC"></span><span id="filteraction_lessequalnc"></span><dl> <span data-ttu-id="c0b79-190"><dt>**\_LESSEQUALNC FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-190"><dt>**FILTERACTION\_LESSEQUALNC**</dt></span></span> </dl>               | <span data-ttu-id="c0b79-191">L'azione di filtro è minore o uguale a (<=) e senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c0b79-191">Filter action is less than or equal to (<=) and case insensitive.</span></span><br/>                                                 |
| <span id="FILTERACTION_LESSEQUAL"></span><span id="filteraction_lessequal"></span><dl> <span data-ttu-id="c0b79-192"><dt>**\_LESSEQUAL FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-192"><dt>**FILTERACTION\_LESSEQUAL**</dt></span></span> </dl>                     | <span data-ttu-id="c0b79-193">L'azione di filtro è minore o uguale a (<=) e fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c0b79-193">Filter action is less than or equal to (<=) and is case sensitive.</span></span><br/>                                                |
| <span id="FILTERACTION_PLUS"></span><span id="filteraction_plus"></span><dl> <span data-ttu-id="c0b79-194"><dt>**FILTERACTION \_ Plus**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-194"><dt>**FILTERACTION\_PLUS**</dt></span></span> </dl>                                    | <span data-ttu-id="c0b79-195">Operatore Add (+).</span><span class="sxs-lookup"><span data-stu-id="c0b79-195">Add operator (+).</span></span><br/>                                                                                                    |
| <span id="FILTERACTION_MINUS"></span><span id="filteraction_minus"></span><dl> <span data-ttu-id="c0b79-196"><dt>**FILTERACTION \_ meno**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-196"><dt>**FILTERACTION\_MINUS**</dt></span></span> </dl>                                 | <span data-ttu-id="c0b79-197">Operatore di sottrazione (-).</span><span class="sxs-lookup"><span data-stu-id="c0b79-197">Subtract operator (-).</span></span><br/>                                                                                               |
| <span id="FILTERACTION_AREBITSON"></span><span id="filteraction_arebitson"></span><dl> <span data-ttu-id="c0b79-198"><dt>**\_AREBITSON FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-198"><dt>**FILTERACTION\_AREBITSON**</dt></span></span> </dl>                     | <span data-ttu-id="c0b79-199">Indica un'operazione bit per bit.</span><span class="sxs-lookup"><span data-stu-id="c0b79-199">Indicates a bitwise operation.</span></span><br/>                                                                                       |
| <span id="FILTERACTION_AREBITSOFF"></span><span id="filteraction_arebitsoff"></span><dl> <span data-ttu-id="c0b79-200"><dt>**\_AREBITSOFF FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-200"><dt>**FILTERACTION\_AREBITSOFF**</dt></span></span> </dl>                  | <span data-ttu-id="c0b79-201">Indica un'operazione non bit per bit.</span><span class="sxs-lookup"><span data-stu-id="c0b79-201">Indicates a non-bitwise operation.</span></span><br/>                                                                                   |
| <span id="FILTERACTION_PROTOCOLSEXIST"></span><span id="filteraction_protocolsexist"></span><dl> <span data-ttu-id="c0b79-202"><dt>**\_PROTOCOLSEXIST FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-202"><dt>**FILTERACTION\_PROTOCOLSEXIST**</dt></span></span> </dl>      | <span data-ttu-id="c0b79-203">Indica che i protocolli selezionati sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="c0b79-203">Indicates that the selected protocols exist.</span></span><br/>                                                                         |
| <span id="FILTERACTION_PROTOCOLEXIST"></span><span id="filteraction_protocolexist"></span><dl> <span data-ttu-id="c0b79-204"><dt>**\_PROTOCOLEXIST FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-204"><dt>**FILTERACTION\_PROTOCOLEXIST**</dt></span></span> </dl>         | <span data-ttu-id="c0b79-205">Indica che il protocollo selezionato esiste.</span><span class="sxs-lookup"><span data-stu-id="c0b79-205">Indicates that the selected protocol exists.</span></span><br/>                                                                         |
| <span id="FILTERACTION_ARRAYEQUAL"></span><span id="filteraction_arrayequal"></span><dl> <span data-ttu-id="c0b79-206"><dt>**\_ARRAYEQUAL FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-206"><dt>**FILTERACTION\_ARRAYEQUAL**</dt></span></span> </dl>                  | <span data-ttu-id="c0b79-207">Indica che il contenuto della matrice è uguale.</span><span class="sxs-lookup"><span data-stu-id="c0b79-207">Indicates that array contents are equal.</span></span> <span data-ttu-id="c0b79-208">Il flag deve essere usato con una struttura di **\_ matrice FILTERACTION** .</span><span class="sxs-lookup"><span data-stu-id="c0b79-208">The flag must be used with a **FILTERACTION\_ARRAY** structure.</span></span><br/>             |
| <span id="FILTERACTION_DEREFPROPERTY"></span><span id="filteraction_derefproperty"></span><dl> <span data-ttu-id="c0b79-209"><dt>**\_DEREFPROPERTY FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-209"><dt>**FILTERACTION\_DEREFPROPERTY**</dt></span></span> </dl>         | <span data-ttu-id="c0b79-210">Descrive un criterio di corrispondenza in un offset (in byte) dal protocollo.</span><span class="sxs-lookup"><span data-stu-id="c0b79-210">Describes a pattern match at an offset (in bytes), from the protocol.</span></span><br/>                                                |
| <span id="FILTERACTION_OID_CONTAINS"></span><span id="filteraction_oid_contains"></span><dl> <span data-ttu-id="c0b79-211"><dt>**FILTERACTION \_ OID \_ contiene**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-211"><dt>**FILTERACTION\_OID\_CONTAINS**</dt></span></span> </dl>           | <span data-ttu-id="c0b79-212">Valuta una sottostringa all'interno di un identificatore di oggetto.</span><span class="sxs-lookup"><span data-stu-id="c0b79-212">Evaluates a substring within an object identifier.</span></span> <span data-ttu-id="c0b79-213">L'azione deve essere utilizzata con la **struttura \_ OID FILTERACTION** .</span><span class="sxs-lookup"><span data-stu-id="c0b79-213">The action must be used with the **FILTERACTION\_OID** structure.</span></span><br/> |
| <span id="FILTERACTION_OID_BEGINS_WITH"></span><span id="filteraction_oid_begins_with"></span><dl> <span data-ttu-id="c0b79-214"><dt>**l' \_ OID FILTERACTION \_ inizia \_ con**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-214"><dt>**FILTERACTION\_OID\_BEGINS\_WITH**</dt></span></span> </dl> | <span data-ttu-id="c0b79-215">Valuta una sottostringa che inizia un identificatore di oggetto.</span><span class="sxs-lookup"><span data-stu-id="c0b79-215">Evaluates a substring that begins an object identifier.</span></span> <span data-ttu-id="c0b79-216">Il flag deve essere utilizzato con **\_ OID FILTERACTION**.</span><span class="sxs-lookup"><span data-stu-id="c0b79-216">The flag must be used with **FILTERACTION\_OID**.</span></span><br/>            |
| <span id="FILTERACTION_OID_ENDS_WITH"></span><span id="filteraction_oid_ends_with"></span><dl> <span data-ttu-id="c0b79-217"><dt>**l' \_ OID FILTERACTION \_ Termina \_ con**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-217"><dt>**FILTERACTION\_OID\_ENDS\_WITH**</dt></span></span> </dl>       | <span data-ttu-id="c0b79-218">Valuta una sottostringa che termina un identificatore di oggetto.</span><span class="sxs-lookup"><span data-stu-id="c0b79-218">Evaluates a substring that ends an object identifier.</span></span> <span data-ttu-id="c0b79-219">Il flag deve essere utilizzato con **\_ OID FILTERACTION**.</span><span class="sxs-lookup"><span data-stu-id="c0b79-219">The flag must be used with **FILTERACTION\_OID**.</span></span><br/>              |
| <span id="FILTERACTION_ADDR_VINES"></span><span id="filteraction_addr_vines"></span><dl> <span data-ttu-id="c0b79-220"><dt>**\_viti FILTERACTION addr \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-220"><dt>**FILTERACTION\_ADDR\_VINES**</dt></span></span> </dl>                 | <span data-ttu-id="c0b79-221">Contiene un indirizzo MAC Vine.</span><span class="sxs-lookup"><span data-stu-id="c0b79-221">Contains a Vines MAC address.</span></span><br/>                                                                                        |
| <span id="FILTERACTION_EXPRESSION"></span><span id="filteraction_expression"></span><dl> <span data-ttu-id="c0b79-222"><dt>**\_espressione FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-222"><dt>**FILTERACTION\_EXPRESSION**</dt></span></span> </dl>                  | <span data-ttu-id="c0b79-223">Contiene un'espressione di azione.</span><span class="sxs-lookup"><span data-stu-id="c0b79-223">Contains an action expression.</span></span><br/>                                                                                       |
| <span id="FILTERACTION_BOOL"></span><span id="filteraction_bool"></span><dl> <span data-ttu-id="c0b79-224"><dt>**\_bool FILTERACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-224"><dt>**FILTERACTION\_BOOL**</dt></span></span> </dl>                                    | <span data-ttu-id="c0b79-225">Contiene un tipo di dati **bool** .</span><span class="sxs-lookup"><span data-stu-id="c0b79-225">Contains a **BOOL** data type.</span></span><br/>                                                                                       |
| <span id="FILTER_DIRECTION_NEXT"></span><span id="filter_direction_next"></span><dl> <span data-ttu-id="c0b79-226"><dt>**\_direzione filtro \_ Avanti**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-226"><dt>**FILTER\_DIRECTION\_NEXT**</dt></span></span> </dl>                       | <span data-ttu-id="c0b79-227">Controlla la direzione sequenziale (frame successivo) all'interno di un file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="c0b79-227">Controls sequential direction (Next frame) within a capture file.</span></span><br/>                                                    |
| <span id="FILTER_DIRECTION_PREV"></span><span id="filter_direction_prev"></span><dl> <span data-ttu-id="c0b79-228"><dt>**\_direzione filtro \_ precedente**</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-228"><dt>**FILTER\_DIRECTION\_PREV**</dt></span></span> </dl>                       | <span data-ttu-id="c0b79-229">Controlla la direzione sequenziale (frame precedente) all'interno di un file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="c0b79-229">Controls sequential direction (Previous frame) within a capture file.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="c0b79-230">**hProperty**</span><span class="sxs-lookup"><span data-stu-id="c0b79-230">**hProperty**</span></span>
</dt> <dd>

<span data-ttu-id="c0b79-231">Handle per una chiave della proprietà.</span><span class="sxs-lookup"><span data-stu-id="c0b79-231">Handle to a property key.</span></span>

</dd> <dt>

<span data-ttu-id="c0b79-232">**Valore**</span><span class="sxs-lookup"><span data-stu-id="c0b79-232">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="c0b79-233">Valore di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="c0b79-233">Value of an object.</span></span>

</dd> <dt>

<span data-ttu-id="c0b79-234">**hProtocol**</span><span class="sxs-lookup"><span data-stu-id="c0b79-234">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="c0b79-235">Handle per visualizzare il protocollo di filtro.</span><span class="sxs-lookup"><span data-stu-id="c0b79-235">Handle to display filter protocol.</span></span>

</dd> <dt>

<span data-ttu-id="c0b79-236">**lpArray**</span><span class="sxs-lookup"><span data-stu-id="c0b79-236">**lpArray**</span></span>
</dt> <dd>

<span data-ttu-id="c0b79-237">Puntatore a una matrice.</span><span class="sxs-lookup"><span data-stu-id="c0b79-237">Pointer to an array.</span></span>

</dd> <dt>

<span data-ttu-id="c0b79-238">**lpProtocolTable**</span><span class="sxs-lookup"><span data-stu-id="c0b79-238">**lpProtocolTable**</span></span>
</dt> <dd>

<span data-ttu-id="c0b79-239">Puntatore a un elenco di protocolli progettato per verificare l'esistenza del protocollo in un frame.</span><span class="sxs-lookup"><span data-stu-id="c0b79-239">Pointer to a protocol list designed to test the existence of protocol in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="c0b79-240">**lpAddress**</span><span class="sxs-lookup"><span data-stu-id="c0b79-240">**lpAddress**</span></span>
</dt> <dd>

<span data-ttu-id="c0b79-241">Puntatore all'indirizzo del tipo di kernel.</span><span class="sxs-lookup"><span data-stu-id="c0b79-241">Pointer to the kernel type address.</span></span> <span data-ttu-id="c0b79-242">Ad esempio, MAC o IP.</span><span class="sxs-lookup"><span data-stu-id="c0b79-242">For example, MAC or IP.</span></span>

</dd> <dt>

<span data-ttu-id="c0b79-243">**lpLargeInt**</span><span class="sxs-lookup"><span data-stu-id="c0b79-243">**lpLargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="c0b79-244">Double **DWORD** usato in un'applicazione Windows NT o Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c0b79-244">Double **DWORD** used in a Windows NT or Windows 2000 application.</span></span>

</dd> <dt>

<span data-ttu-id="c0b79-245">**lpTime**</span><span class="sxs-lookup"><span data-stu-id="c0b79-245">**lpTime**</span></span>
</dt> <dd>

<span data-ttu-id="c0b79-246">Puntatore a una struttura **SYSTEMTIME** .</span><span class="sxs-lookup"><span data-stu-id="c0b79-246">A pointer to a **SYSTEMTIME** structure.</span></span>

</dd> <dt>

<span data-ttu-id="c0b79-247">**lpOID**</span><span class="sxs-lookup"><span data-stu-id="c0b79-247">**lpOID**</span></span>
</dt> <dd>

<span data-ttu-id="c0b79-248">Puntatore alla struttura dell' **\_ identificatore di oggetto** (OID).</span><span class="sxs-lookup"><span data-stu-id="c0b79-248">A pointer to the **OBJECT\_IDENTIFIER** (OID) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c0b79-249">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="c0b79-249">**ByteCount**</span></span>
</dt> <dd>

<span data-ttu-id="c0b79-250">Numero, in byte, nel frame.</span><span class="sxs-lookup"><span data-stu-id="c0b79-250">The number, in bytes, in the frame.</span></span>

</dd> <dt>

<span data-ttu-id="c0b79-251">**ByteOffset**</span><span class="sxs-lookup"><span data-stu-id="c0b79-251">**ByteOffset**</span></span>
</dt> <dd>

<span data-ttu-id="c0b79-252">Valore byte di offset della struttura FILTEROBJECT utilizzata per confrontare le matrici.</span><span class="sxs-lookup"><span data-stu-id="c0b79-252">The offset byte value of the FILTEROBJECT structure used to compare arrays.</span></span>

</dd> <dt>

<span data-ttu-id="c0b79-253">**pNext**</span><span class="sxs-lookup"><span data-stu-id="c0b79-253">**pNext**</span></span>
</dt> <dd>

<span data-ttu-id="c0b79-254">Riservato.</span><span class="sxs-lookup"><span data-stu-id="c0b79-254">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0b79-255">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0b79-255">Requirements</span></span>



| <span data-ttu-id="c0b79-256">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0b79-256">Requirement</span></span> | <span data-ttu-id="c0b79-257">Valore</span><span class="sxs-lookup"><span data-stu-id="c0b79-257">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b79-258">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0b79-258">Minimum supported client</span></span><br/> | <span data-ttu-id="c0b79-259">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c0b79-259">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c0b79-260">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0b79-260">Minimum supported server</span></span><br/> | <span data-ttu-id="c0b79-261">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c0b79-261">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c0b79-262">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0b79-262">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0b79-263"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0b79-263"><dt>Netmon.h</dt></span></span> </dl> |



 

 




