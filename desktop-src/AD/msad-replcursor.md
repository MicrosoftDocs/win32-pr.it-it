---
title: Classe MSAD_ReplCursor
description: Fornisce informazioni sullo stato di replica in ingresso su tutte le repliche di un determinato contesto dei nomi (NC).
ms.assetid: 5746cfe9-b113-4be3-b609-15cb937c271b
ms.tgt_platform: multiple
keywords:
- Classe MSAD_ReplCursor Active Directory
- Classe MSAD_ReplCursor Active Directory, descritta
topic_type:
- apiref
api_name:
- MSAD_ReplCursor
- MSAD_ReplCursor.NamingContextDN
- MSAD_ReplCursor.SourceDsaInvocationID
- MSAD_ReplCursor.USNAttributeFilter
- MSAD_ReplCursor.SourceDsaDN
- MSAD_ReplCursor.TimeOfLastSuccessfulSync
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725ac8e9eee9f921ce4109e0b0e42ed85e75ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476846"
---
# <a name="msad_replcursor-class"></a><span data-ttu-id="c923e-105">\_Classe MSAD ReplCursor</span><span class="sxs-lookup"><span data-stu-id="c923e-105">MSAD\_ReplCursor class</span></span>

<span data-ttu-id="c923e-106">Fornisce informazioni sullo stato di replica in ingresso su tutte le repliche di un determinato contesto dei nomi (NC).</span><span class="sxs-lookup"><span data-stu-id="c923e-106">Provides inbound replication state information about all replicas of a given naming context (NC).</span></span>

## <a name="syntax"></a><span data-ttu-id="c923e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c923e-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplCursor
{
  String   NamingContextDN;
  String   SourceDsaInvocationID;
  uint64   USNAttributeFilter;
  String   SourceDsaDN;
  datetime TimeOfLastSuccessfulSync;
};
```

## <a name="members"></a><span data-ttu-id="c923e-108">Members</span><span class="sxs-lookup"><span data-stu-id="c923e-108">Members</span></span>

<span data-ttu-id="c923e-109">La **classe \_ ReplCursor di MSAD** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c923e-109">The **MSAD\_ReplCursor** class has these types of members:</span></span>

-   [<span data-ttu-id="c923e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c923e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c923e-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c923e-111">Properties</span></span>

<span data-ttu-id="c923e-112">La **classe \_ ReplCursor di MSAD** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c923e-112">The **MSAD\_ReplCursor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c923e-113">**NamingContextDN**</span><span class="sxs-lookup"><span data-stu-id="c923e-113">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c923e-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c923e-114">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="c923e-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c923e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c923e-116">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c923e-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c923e-117">Ottiene il percorso X. 500 per il contesto dei nomi (NC) che include il cursore.</span><span class="sxs-lookup"><span data-stu-id="c923e-117">Gets the X.500 path for the naming context (NC) that holds this cursor.</span></span>

</dd> <dt>

<span data-ttu-id="c923e-118">**SourceDsaDN**</span><span class="sxs-lookup"><span data-stu-id="c923e-118">**SourceDsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c923e-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c923e-119">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="c923e-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c923e-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c923e-121">Ottiene il percorso X. 500 per il Directory System Agent (DSA) che rappresenta il controller di dominio di origine (DC).</span><span class="sxs-lookup"><span data-stu-id="c923e-121">Gets the X.500 path for the directory system agent (DSA) that represents the source domain controller (DC).</span></span>

</dd> <dt>

<span data-ttu-id="c923e-122">**SourceDsaInvocationID**</span><span class="sxs-lookup"><span data-stu-id="c923e-122">**SourceDsaInvocationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c923e-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c923e-123">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="c923e-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c923e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c923e-125">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c923e-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c923e-126">Ottiene l'identificatore di chiamata del server di origine a cui corrisponde l'oggetto **USNAttributeFilter** .</span><span class="sxs-lookup"><span data-stu-id="c923e-126">Gets the invocation identifier of the originating server to which the **USNAttributeFilter** corresponds.</span></span>

</dd> <dt>

<span data-ttu-id="c923e-127">**TimeOfLastSuccessfulSync**</span><span class="sxs-lookup"><span data-stu-id="c923e-127">**TimeOfLastSuccessfulSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c923e-128">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c923e-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c923e-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c923e-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c923e-130">Ottiene il timestamp dell'ultima sincronizzazione corretta della replica con il DSA di origine.</span><span class="sxs-lookup"><span data-stu-id="c923e-130">Gets the timestamp of the last successful replication sync with the source DSA.</span></span> <span data-ttu-id="c923e-131">Indica l'ora in cui il controller di dominio ha rilevato le modifiche apportate nell'origine DSA per questo NC.</span><span class="sxs-lookup"><span data-stu-id="c923e-131">Indicates the time when this DC last saw changes made on the source DSA for this NC.</span></span>

</dd> <dt>

<span data-ttu-id="c923e-132">**USNAttributeFilter**</span><span class="sxs-lookup"><span data-stu-id="c923e-132">**USNAttributeFilter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c923e-133">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c923e-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c923e-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c923e-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c923e-135">Ottiene il numero di sequenza di aggiornamento massimo a cui il server di destinazione può indicare che ha registrato tutte le modifiche originate dal server specificato in corrispondenza dei numeri di sequenza di aggiornamento minori o uguali a questo numero di sequenza dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="c923e-135">Gets the maximum update sequence number to which the destination server can indicate that it has recorded all changes originated by the given server at update sequence numbers less than, or equal to, this update sequence number.</span></span> <span data-ttu-id="c923e-136">Questa proprietà viene utilizzata per filtrare le modifiche che il server di destinazione ha già applicato ai server di origine della replica.</span><span class="sxs-lookup"><span data-stu-id="c923e-136">This property is used to filter changes that the destination server has already applied at replication source servers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c923e-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c923e-137">Requirements</span></span>



| <span data-ttu-id="c923e-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="c923e-138">Requirement</span></span> | <span data-ttu-id="c923e-139">Valore</span><span class="sxs-lookup"><span data-stu-id="c923e-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c923e-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c923e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c923e-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c923e-141">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c923e-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c923e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c923e-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c923e-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c923e-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c923e-144">Namespace</span></span><br/>                | <span data-ttu-id="c923e-145">\\MicrosoftActiveDirectory radice</span><span class="sxs-lookup"><span data-stu-id="c923e-145">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="c923e-146">MOF</span><span class="sxs-lookup"><span data-stu-id="c923e-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c923e-147"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c923e-147"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="c923e-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c923e-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c923e-149"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c923e-149"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c923e-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c923e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c923e-151">**\_cursore REPL \_ DS**</span><span class="sxs-lookup"><span data-stu-id="c923e-151">**DS\_REPL\_CURSOR**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
</dt> </dl>

 

