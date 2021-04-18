---
description: Rappresenta i dati non elaborati di una struttura EDID (video Electronics Standard Association) migliorata.
ms.assetid: a51b73bb-a5f7-4e01-9c88-780105e9952b
title: Classe WmiMonitorRawEEdidV1Block
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorRawEEdidV1Block
- WmiMonitorRawEEdidV1Block.Active
- WmiMonitorRawEEdidV1Block.InstanceName
- WmiMonitorRawEEdidV1Block.Id
- WmiMonitorRawEEdidV1Block.Type
- WmiMonitorRawEEdidV1Block.Content
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 79566dccceb36281c9b3a94b19fed2ed5679dc8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313690"
---
# <a name="wmimonitorraweedidv1block-class"></a><span data-ttu-id="489b4-103">Classe WmiMonitorRawEEdidV1Block</span><span class="sxs-lookup"><span data-stu-id="489b4-103">WmiMonitorRawEEdidV1Block class</span></span>

<span data-ttu-id="489b4-104">La classe WMI **WmiMonitorRawEEdidV1Block** rappresenta i dati non elaborati da una struttura di EDID (video Electronics Standard Association) migliorata.</span><span class="sxs-lookup"><span data-stu-id="489b4-104">The **WmiMonitorRawEEdidV1Block** WMI class represents the raw data from a Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure.</span></span> <span data-ttu-id="489b4-105">Questa struttura di dati a 128 byte contiene informazioni che descrivono la configurazione ottimale per una visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="489b4-105">This 128-byte data structure contains information that describes the optimal configuration for a display.</span></span>

## <a name="syntax"></a><span data-ttu-id="489b4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="489b4-106">Syntax</span></span>

``` syntax
class WmiMonitorRawEEdidV1Block : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint8   Id;
  uint8   Type;
  uint8   Content[];
};
```

## <a name="members"></a><span data-ttu-id="489b4-107">Members</span><span class="sxs-lookup"><span data-stu-id="489b4-107">Members</span></span>

<span data-ttu-id="489b4-108">La classe **WmiMonitorRawEEdidV1Block** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="489b4-108">The **WmiMonitorRawEEdidV1Block** class has these types of members:</span></span>

-   [<span data-ttu-id="489b4-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="489b4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="489b4-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="489b4-110">Properties</span></span>

<span data-ttu-id="489b4-111">La classe **WmiMonitorRawEEdidV1Block** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="489b4-111">The **WmiMonitorRawEEdidV1Block** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="489b4-112">**Attivo**</span><span class="sxs-lookup"><span data-stu-id="489b4-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="489b4-113">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="489b4-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="489b4-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="489b4-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="489b4-115">Indica il monitoraggio attivo.</span><span class="sxs-lookup"><span data-stu-id="489b4-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="489b4-116">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="489b4-116">**Content**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="489b4-117">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="489b4-117">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="489b4-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="489b4-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="489b4-119">matrice di byte 128 che contiene il contenuto del blocco non elaborato.</span><span class="sxs-lookup"><span data-stu-id="489b4-119">128 byte array that contains the raw block content.</span></span>

</dd> <dt>

<span data-ttu-id="489b4-120">**Id**</span><span class="sxs-lookup"><span data-stu-id="489b4-120">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="489b4-121">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="489b4-121">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="489b4-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="489b4-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="489b4-123">Identità del blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="489b4-123">Identity of the data block.</span></span>

</dd> <dt>

<span data-ttu-id="489b4-124">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="489b4-124">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="489b4-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="489b4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="489b4-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="489b4-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="489b4-127">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="489b4-127">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="489b4-128">Nome dell'istanza di monitoraggio specifica.</span><span class="sxs-lookup"><span data-stu-id="489b4-128">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="489b4-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="489b4-129">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="489b4-130">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="489b4-130">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="489b4-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="489b4-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="489b4-132">Tipo di blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="489b4-132">Type of data block.</span></span> <span data-ttu-id="489b4-133">Nella tabella seguente sono elencati i valori possibili che possono essere restituiti.</span><span class="sxs-lookup"><span data-stu-id="489b4-133">The following table lists possible values that can be returned.</span></span>



| <span data-ttu-id="489b4-134">Valore</span><span class="sxs-lookup"><span data-stu-id="489b4-134">Value</span></span>                                                                                 | <span data-ttu-id="489b4-135">Significato</span><span class="sxs-lookup"><span data-stu-id="489b4-135">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="489b4-136"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="489b4-136"><dt>0 (0x0)</dt></span></span> </dl>    | <span data-ttu-id="489b4-137">Inizializzazione annullata</span><span class="sxs-lookup"><span data-stu-id="489b4-137">Uninitialized</span></span><br/>   |
| <dl> <span data-ttu-id="489b4-138"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="489b4-138"><dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="489b4-139">Blocco base EDID</span><span class="sxs-lookup"><span data-stu-id="489b4-139">EDID base block</span></span><br/> |
| <dl> <span data-ttu-id="489b4-140"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="489b4-140"><dt>2 (0x2)</dt></span></span> </dl>    | <span data-ttu-id="489b4-141">Mappa di blocco EDID</span><span class="sxs-lookup"><span data-stu-id="489b4-141">EDID block map</span></span><br/>  |
| <dl> <span data-ttu-id="489b4-142"><dt>255 (0xFF)</dt></span><span class="sxs-lookup"><span data-stu-id="489b4-142"><dt>255 (0xFF)</dt></span></span> </dl> | <span data-ttu-id="489b4-143">Altro</span><span class="sxs-lookup"><span data-stu-id="489b4-143">Other</span></span><br/>           |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="489b4-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="489b4-144">Requirements</span></span>



| <span data-ttu-id="489b4-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="489b4-145">Requirement</span></span> | <span data-ttu-id="489b4-146">Valore</span><span class="sxs-lookup"><span data-stu-id="489b4-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="489b4-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="489b4-147">Minimum supported client</span></span><br/> | <span data-ttu-id="489b4-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="489b4-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="489b4-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="489b4-149">Minimum supported server</span></span><br/> | <span data-ttu-id="489b4-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="489b4-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="489b4-151">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="489b4-151">Namespace</span></span><br/>                | <span data-ttu-id="489b4-152">\\WMI radice</span><span class="sxs-lookup"><span data-stu-id="489b4-152">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="489b4-153">MOF</span><span class="sxs-lookup"><span data-stu-id="489b4-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="489b4-154"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="489b4-154"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="489b4-155">DLL</span><span class="sxs-lookup"><span data-stu-id="489b4-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="489b4-156"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="489b4-156"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="489b4-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="489b4-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="489b4-158">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="489b4-158">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> <dt>

[<span data-ttu-id="489b4-159">**WmiGetMonitorRawEEdidV1Block**</span><span class="sxs-lookup"><span data-stu-id="489b4-159">**WmiGetMonitorRawEEdidV1Block**</span></span>](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md)
</dt> </dl>

 

 




