---
description: Contiene informazioni che identificano l'adapter.
ms.assetid: d0d59df9-c512-4d69-b0a0-7d87d7a380f6
title: Struttura D3DADAPTER_IDENTIFIER9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DADAPTER_IDENTIFIER9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 33aba75cafff5f9e69a74d5570f98455a9853289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322381"
---
# <a name="d3dadapter_identifier9-structure"></a><span data-ttu-id="19933-103">\_Struttura D3DADAPTER IDENTIFIER9</span><span class="sxs-lookup"><span data-stu-id="19933-103">D3DADAPTER\_IDENTIFIER9 structure</span></span>

<span data-ttu-id="19933-104">Contiene informazioni che identificano l'adapter.</span><span class="sxs-lookup"><span data-stu-id="19933-104">Contains information identifying the adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="19933-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19933-105">Syntax</span></span>


```C++
typedef struct D3DADAPTER_IDENTIFIER9 {
  char          Driver[MAX_DEVICE_IDENTIFIER_STRING];
  char          Description[MAX_DEVICE_IDENTIFIER_STRING];
  char          DeviceName[32];
  LARGE_INTEGER DriverVersion;
  DWORD         DriverVersionLowPart;
  DWORD         DriverVersionHighPart;
  DWORD         VendorId;
  DWORD         DeviceId;
  DWORD         SubSysId;
  DWORD         Revision;
  GUID          DeviceIdentifier;
  DWORD         WHQLLevel;
} D3DADAPTER_IDENTIFIER9, *LPD3DADAPTER_IDENTIFIER9;
```



## <a name="members"></a><span data-ttu-id="19933-106">Members</span><span class="sxs-lookup"><span data-stu-id="19933-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="19933-107">**Driver**</span><span class="sxs-lookup"><span data-stu-id="19933-107">**Driver**</span></span>
</dt> <dd>

<span data-ttu-id="19933-108">Tipo: **char**</span><span class="sxs-lookup"><span data-stu-id="19933-108">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="19933-109">Utilizzato per la presentazione all'utente.</span><span class="sxs-lookup"><span data-stu-id="19933-109">Used for presentation to the user.</span></span> <span data-ttu-id="19933-110">Questa operazione non deve essere utilizzata per identificare driver specifici, perché molte stringhe diverse possono essere associate allo stesso dispositivo e driver di fornitori diversi.</span><span class="sxs-lookup"><span data-stu-id="19933-110">This should not be used to identify particular drivers, because many different strings might be associated with the same device and driver from different vendors.</span></span>

</dd> <dt>

<span data-ttu-id="19933-111">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="19933-111">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="19933-112">Tipo: **char**</span><span class="sxs-lookup"><span data-stu-id="19933-112">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="19933-113">Utilizzato per la presentazione all'utente.</span><span class="sxs-lookup"><span data-stu-id="19933-113">Used for presentation to the user.</span></span>

</dd> <dt>

<span data-ttu-id="19933-114">**DeviceName**</span><span class="sxs-lookup"><span data-stu-id="19933-114">**DeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="19933-115">Tipo: **char**</span><span class="sxs-lookup"><span data-stu-id="19933-115">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="19933-116">Nome del dispositivo per GDI.</span><span class="sxs-lookup"><span data-stu-id="19933-116">Device name for GDI.</span></span>

</dd> <dt>

<span data-ttu-id="19933-117">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="19933-117">**DriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="19933-118">Tipo: **[ **\_ Integer grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="19933-118">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="19933-119">Identificare la versione del driver Direct3D.</span><span class="sxs-lookup"><span data-stu-id="19933-119">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="19933-120">È possibile eseguire confronti minori di e superiori rispetto al valore Signed Integer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="19933-120">It is legal to do less than and greater than comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="19933-121">Tuttavia, prestare attenzione se si utilizza questo elemento per identificare i driver problematici.</span><span class="sxs-lookup"><span data-stu-id="19933-121">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="19933-122">È invece consigliabile usare DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="19933-122">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="19933-123">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="19933-123">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="19933-124">**DriverVersionLowPart**</span><span class="sxs-lookup"><span data-stu-id="19933-124">**DriverVersionLowPart**</span></span>
</dt> <dd>

<span data-ttu-id="19933-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19933-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="19933-126">Identificare la versione del driver Direct3D.</span><span class="sxs-lookup"><span data-stu-id="19933-126">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="19933-127">È lecito eseguire confronti < e > sul valore intero con segno a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="19933-127">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="19933-128">Tuttavia, prestare attenzione se si utilizza questo elemento per identificare i driver problematici.</span><span class="sxs-lookup"><span data-stu-id="19933-128">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="19933-129">È invece consigliabile usare DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="19933-129">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="19933-130">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="19933-130">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="19933-131">**DriverVersionHighPart**</span><span class="sxs-lookup"><span data-stu-id="19933-131">**DriverVersionHighPart**</span></span>
</dt> <dd>

<span data-ttu-id="19933-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19933-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="19933-133">Identificare la versione del driver Direct3D.</span><span class="sxs-lookup"><span data-stu-id="19933-133">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="19933-134">È lecito eseguire confronti < e > sul valore intero con segno a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="19933-134">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="19933-135">Tuttavia, prestare attenzione se si utilizza questo elemento per identificare i driver problematici.</span><span class="sxs-lookup"><span data-stu-id="19933-135">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="19933-136">È invece consigliabile usare DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="19933-136">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="19933-137">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="19933-137">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="19933-138">**VendorId**</span><span class="sxs-lookup"><span data-stu-id="19933-138">**VendorId**</span></span>
</dt> <dd>

<span data-ttu-id="19933-139">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19933-139">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="19933-140">Può essere utilizzato per identificare un particolare set di chip.</span><span class="sxs-lookup"><span data-stu-id="19933-140">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="19933-141">Eseguire una query su questo membro per identificare il produttore.</span><span class="sxs-lookup"><span data-stu-id="19933-141">Query this member to identify the manufacturer.</span></span> <span data-ttu-id="19933-142">Il valore può essere zero se sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="19933-142">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="19933-143">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="19933-143">**DeviceId**</span></span>
</dt> <dd>

<span data-ttu-id="19933-144">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19933-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="19933-145">Può essere utilizzato per identificare un particolare set di chip.</span><span class="sxs-lookup"><span data-stu-id="19933-145">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="19933-146">Eseguire una query su questo membro per identificare il tipo di set di chip.</span><span class="sxs-lookup"><span data-stu-id="19933-146">Query this member to identify the type of chip set.</span></span> <span data-ttu-id="19933-147">Il valore può essere zero se sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="19933-147">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="19933-148">**SubSysId**</span><span class="sxs-lookup"><span data-stu-id="19933-148">**SubSysId**</span></span>
</dt> <dd>

<span data-ttu-id="19933-149">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19933-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="19933-150">Può essere utilizzato per identificare un particolare set di chip.</span><span class="sxs-lookup"><span data-stu-id="19933-150">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="19933-151">Eseguire una query su questo membro per identificare il sottosistema, in genere la bacheca particolare.</span><span class="sxs-lookup"><span data-stu-id="19933-151">Query this member to identify the subsystem, typically the particular board.</span></span> <span data-ttu-id="19933-152">Il valore può essere zero se sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="19933-152">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="19933-153">**Revisione**</span><span class="sxs-lookup"><span data-stu-id="19933-153">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="19933-154">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19933-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="19933-155">Può essere utilizzato per identificare un particolare set di chip.</span><span class="sxs-lookup"><span data-stu-id="19933-155">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="19933-156">Eseguire una query su questo membro per identificare il livello di revisione del set di chip.</span><span class="sxs-lookup"><span data-stu-id="19933-156">Query this member to identify the revision level of the chip set.</span></span> <span data-ttu-id="19933-157">Il valore può essere zero se sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="19933-157">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="19933-158">**DeviceIdentifier**</span><span class="sxs-lookup"><span data-stu-id="19933-158">**DeviceIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="19933-159">Tipo: **[ **GUID**](guid.md)**</span><span class="sxs-lookup"><span data-stu-id="19933-159">Type: **[**GUID**](guid.md)**</span></span>

</dd> <dd>

<span data-ttu-id="19933-160">È possibile eseguire una query per verificare le modifiche apportate al driver e al set di chip.</span><span class="sxs-lookup"><span data-stu-id="19933-160">Can be queried to check changes in the driver and chip set.</span></span> <span data-ttu-id="19933-161">Questo GUID è un identificatore univoco per la coppia di driver e set di chip.</span><span class="sxs-lookup"><span data-stu-id="19933-161">This GUID is a unique identifier for the driver and chip set pair.</span></span> <span data-ttu-id="19933-162">Eseguire una query su questo membro per tenere traccia delle modifiche al driver e al set di chip per generare un nuovo profilo per il sottosistema grafico.</span><span class="sxs-lookup"><span data-stu-id="19933-162">Query this member to track changes to the driver and chip set in order to generate a new profile for the graphics subsystem.</span></span> <span data-ttu-id="19933-163">DeviceIdentifier può essere usato anche per identificare driver problematici particolari.</span><span class="sxs-lookup"><span data-stu-id="19933-163">DeviceIdentifier can also be used to identify particular problematic drivers.</span></span>

</dd> <dt>

<span data-ttu-id="19933-164">**WHQLLevel**</span><span class="sxs-lookup"><span data-stu-id="19933-164">**WHQLLevel**</span></span>
</dt> <dd>

<span data-ttu-id="19933-165">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19933-165">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="19933-166">Utilizzato per determinare il livello di convalida di Windows Hardware Quality Labs (WHQL) per questa coppia di driver e dispositivi.</span><span class="sxs-lookup"><span data-stu-id="19933-166">Used to determine the Windows Hardware Quality Labs (WHQL) validation level for this driver and device pair.</span></span> <span data-ttu-id="19933-167">DWORD è una struttura di data compressa che definisce la data di rilascio del test WHQL più recente passato dal driver.</span><span class="sxs-lookup"><span data-stu-id="19933-167">The DWORD is a packed date structure defining the date of the release of the most recent WHQL test passed by the driver.</span></span> <span data-ttu-id="19933-168">È consentito eseguire operazioni di < e > su questo valore.</span><span class="sxs-lookup"><span data-stu-id="19933-168">It is legal to perform < and > operations on this value.</span></span> <span data-ttu-id="19933-169">Di seguito viene illustrato il formato della data.</span><span class="sxs-lookup"><span data-stu-id="19933-169">The following illustrates the date format.</span></span>



|       |                                               |
|-------|-----------------------------------------------|
| <span data-ttu-id="19933-170">BITS</span><span class="sxs-lookup"><span data-stu-id="19933-170">Bits</span></span>  |                                               |
| <span data-ttu-id="19933-171">31-16</span><span class="sxs-lookup"><span data-stu-id="19933-171">31-16</span></span> | <span data-ttu-id="19933-172">Anno, un numero decimale compreso tra 1999 e verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="19933-172">The year, a decimal number from 1999 upwards.</span></span> |
| <span data-ttu-id="19933-173">15-8</span><span class="sxs-lookup"><span data-stu-id="19933-173">15-8</span></span>  | <span data-ttu-id="19933-174">Il mese, un numero decimale compreso tra 1 e 12.</span><span class="sxs-lookup"><span data-stu-id="19933-174">The month, a decimal number from 1 to 12.</span></span>     |
| <span data-ttu-id="19933-175">7-0</span><span class="sxs-lookup"><span data-stu-id="19933-175">7-0</span></span>   | <span data-ttu-id="19933-176">Il giorno, un numero decimale compreso tra 1 e 31.</span><span class="sxs-lookup"><span data-stu-id="19933-176">The day, a decimal number from 1 to 31.</span></span>       |



 

<span data-ttu-id="19933-177">Vengono inoltre utilizzati i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="19933-177">The following values are also used.</span></span>



|     |                                                       |
|-----|-------------------------------------------------------|
| <span data-ttu-id="19933-178">0</span><span class="sxs-lookup"><span data-stu-id="19933-178">0</span></span>   | <span data-ttu-id="19933-179">Non certificata.</span><span class="sxs-lookup"><span data-stu-id="19933-179">Not certified.</span></span>                                        |
| <span data-ttu-id="19933-180">1</span><span class="sxs-lookup"><span data-stu-id="19933-180">1</span></span>   | <span data-ttu-id="19933-181">WHQL convalidato, ma non sono disponibili informazioni sulla data.</span><span class="sxs-lookup"><span data-stu-id="19933-181">WHQL validated, but no date information is available.</span></span> |



 

<span data-ttu-id="19933-182">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="19933-182">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

<span data-ttu-id="19933-183">Per Direct3D9Ex in esecuzione in Windows Vista, Windows Server 2008, Windows 7 e Windows Server 2008 R2 (o più sistemi operativi correnti), [**IDirect3D9:: GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) restituisce 1 per il livello WHQL senza controllare lo stato del driver.</span><span class="sxs-lookup"><span data-stu-id="19933-183">For Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system), [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) returns 1 for the WHQL level without checking the status of the driver.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19933-184">Commenti</span><span class="sxs-lookup"><span data-stu-id="19933-184">Remarks</span></span>

<span data-ttu-id="19933-185">Nell'esempio di pseudocodice seguente viene illustrato il formato della versione codificato nei membri DriverVersion, DriverVersionLowPart e DriverVersionHighPart.</span><span class="sxs-lookup"><span data-stu-id="19933-185">The following pseudocode example illustrates the version format encoded in the DriverVersion, DriverVersionLowPart, and DriverVersionHighPart members.</span></span>


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



<span data-ttu-id="19933-186">Per ulteriori informazioni sulla macro HIWORD, sulla macro LOWORD e sulla struttura di tipo Integer grande, vedere Platform SDK \_ .</span><span class="sxs-lookup"><span data-stu-id="19933-186">See the Platform SDK for more information about the HIWORD macro, the LOWORD macro, and the LARGE\_INTEGER structure.</span></span>

<span data-ttu-id="19933-187">\_ \_ \_ La stringa dell'identificatore di dispositivo Max è una costante con la definizione seguente.</span><span class="sxs-lookup"><span data-stu-id="19933-187">MAX\_DEVICE\_IDENTIFIER\_STRING is a constant with the following definition.</span></span>


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



<span data-ttu-id="19933-188">I membri VendorId, DeviceId, SubSysId e Revision possono essere utilizzati in combinazione per identificare determinati set di chip.</span><span class="sxs-lookup"><span data-stu-id="19933-188">The VendorId, DeviceId, SubSysId, and Revision members can be used in tandem to identify particular chip sets.</span></span> <span data-ttu-id="19933-189">Tuttavia, usare questi membri con cautela.</span><span class="sxs-lookup"><span data-stu-id="19933-189">However, use these members with caution.</span></span>

## <a name="requirements"></a><span data-ttu-id="19933-190">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19933-190">Requirements</span></span>



| <span data-ttu-id="19933-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="19933-191">Requirement</span></span> | <span data-ttu-id="19933-192">Valore</span><span class="sxs-lookup"><span data-stu-id="19933-192">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19933-193">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19933-193">Header</span></span><br/> | <dl> <span data-ttu-id="19933-194"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="19933-194"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19933-195">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19933-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19933-196">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="19933-196">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
