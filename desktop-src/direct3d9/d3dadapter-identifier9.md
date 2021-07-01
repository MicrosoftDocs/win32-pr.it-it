---
description: Contiene informazioni che identificano l'adapter.
ms.assetid: d0d59df9-c512-4d69-b0a0-7d87d7a380f6
title: D3DADAPTER_IDENTIFIER9 struttura (D3D9Types.h)
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
ms.openlocfilehash: 85401573956d29386b5ddabbd48711a7be140463
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129970"
---
# <a name="d3dadapter_identifier9-structure"></a><span data-ttu-id="dd477-103">Struttura D3DADAPTER \_ IDENTIFIER9</span><span class="sxs-lookup"><span data-stu-id="dd477-103">D3DADAPTER\_IDENTIFIER9 structure</span></span>

<span data-ttu-id="dd477-104">Contiene informazioni che identificano l'adapter.</span><span class="sxs-lookup"><span data-stu-id="dd477-104">Contains information identifying the adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd477-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd477-105">Syntax</span></span>


```C++
typedef struct D3DADAPTER_IDENTIFIER9 {
  char          Driver[MAX_DEVICE_IDENTIFIER_STRING];
  char          Description[MAX_DEVICE_IDENTIFIER_STRING];
  char          DeviceName[32];
#ifdef _WIN32
  LARGE_INTEGER DriverVersion;
#else
  DWORD         DriverVersionLowPart;
  DWORD         DriverVersionHighPart;
#endif
  DWORD         VendorId;
  DWORD         DeviceId;
  DWORD         SubSysId;
  DWORD         Revision;
  GUID          DeviceIdentifier;
  DWORD         WHQLLevel;
} D3DADAPTER_IDENTIFIER9, *LPD3DADAPTER_IDENTIFIER9;
```



## <a name="members"></a><span data-ttu-id="dd477-106">Members</span><span class="sxs-lookup"><span data-stu-id="dd477-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dd477-107">**Driver**</span><span class="sxs-lookup"><span data-stu-id="dd477-107">**Driver**</span></span>
</dt> <dd>

<span data-ttu-id="dd477-108">Tipo: **char**</span><span class="sxs-lookup"><span data-stu-id="dd477-108">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="dd477-109">Usato per la presentazione all'utente.</span><span class="sxs-lookup"><span data-stu-id="dd477-109">Used for presentation to the user.</span></span> <span data-ttu-id="dd477-110">Questo non deve essere usato per identificare driver specifici, perché molte stringhe diverse potrebbero essere associate allo stesso dispositivo e driver di fornitori diversi.</span><span class="sxs-lookup"><span data-stu-id="dd477-110">This should not be used to identify particular drivers, because many different strings might be associated with the same device and driver from different vendors.</span></span>

</dd> <dt>

<span data-ttu-id="dd477-111">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="dd477-111">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="dd477-112">Tipo: **char**</span><span class="sxs-lookup"><span data-stu-id="dd477-112">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="dd477-113">Usato per la presentazione all'utente.</span><span class="sxs-lookup"><span data-stu-id="dd477-113">Used for presentation to the user.</span></span>

</dd> <dt>

<span data-ttu-id="dd477-114">**DeviceName**</span><span class="sxs-lookup"><span data-stu-id="dd477-114">**DeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="dd477-115">Tipo: **char**</span><span class="sxs-lookup"><span data-stu-id="dd477-115">Type: **char**</span></span>

</dd> <dd>

<span data-ttu-id="dd477-116">Nome del dispositivo per GDI.</span><span class="sxs-lookup"><span data-stu-id="dd477-116">Device name for GDI.</span></span>

</dd> <dt>

<span data-ttu-id="dd477-117">**DriverVersion**</span><span class="sxs-lookup"><span data-stu-id="dd477-117">**DriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="dd477-118">Tipo: **[ **LARGE \_ INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="dd477-118">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="dd477-119">Identificare la versione del driver Direct3D.</span><span class="sxs-lookup"><span data-stu-id="dd477-119">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="dd477-120">È legale eseguire confronti minori e maggiori di sul valore intero con segno a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="dd477-120">It is legal to do less than and greater than comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="dd477-121">Prestare tuttavia attenzione se si usa questo elemento per identificare i driver problematici.</span><span class="sxs-lookup"><span data-stu-id="dd477-121">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="dd477-122">È invece consigliabile usare DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="dd477-122">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="dd477-123">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="dd477-123">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="dd477-124">**DriverVersionLowPart**</span><span class="sxs-lookup"><span data-stu-id="dd477-124">**DriverVersionLowPart**</span></span>
</dt> <dd>

<span data-ttu-id="dd477-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd477-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dd477-126">Identificare la versione del driver Direct3D.</span><span class="sxs-lookup"><span data-stu-id="dd477-126">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="dd477-127">È legale eseguire confronti < e > sul valore intero con segno a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="dd477-127">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="dd477-128">Prestare tuttavia attenzione se si usa questo elemento per identificare i driver problematici.</span><span class="sxs-lookup"><span data-stu-id="dd477-128">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="dd477-129">È invece consigliabile usare DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="dd477-129">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="dd477-130">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="dd477-130">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="dd477-131">**DriverVersionHighPart**</span><span class="sxs-lookup"><span data-stu-id="dd477-131">**DriverVersionHighPart**</span></span>
</dt> <dd>

<span data-ttu-id="dd477-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd477-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dd477-133">Identificare la versione del driver Direct3D.</span><span class="sxs-lookup"><span data-stu-id="dd477-133">Identify the version of the Direct3D driver.</span></span> <span data-ttu-id="dd477-134">È legale eseguire confronti < e > sul valore intero con segno a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="dd477-134">It is legal to do < and > comparisons on the 64-bit signed integer value.</span></span> <span data-ttu-id="dd477-135">Prestare tuttavia attenzione se si usa questo elemento per identificare i driver problematici.</span><span class="sxs-lookup"><span data-stu-id="dd477-135">However, exercise caution if you use this element to identify problematic drivers.</span></span> <span data-ttu-id="dd477-136">È invece consigliabile usare DeviceIdentifier.</span><span class="sxs-lookup"><span data-stu-id="dd477-136">Instead, you should use DeviceIdentifier.</span></span> <span data-ttu-id="dd477-137">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="dd477-137">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="dd477-138">**VendorId**</span><span class="sxs-lookup"><span data-stu-id="dd477-138">**VendorId**</span></span>
</dt> <dd>

<span data-ttu-id="dd477-139">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd477-139">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dd477-140">Può essere usato per identificare un determinato chip set.</span><span class="sxs-lookup"><span data-stu-id="dd477-140">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="dd477-141">Eseguire una query su questo membro per identificare il produttore.</span><span class="sxs-lookup"><span data-stu-id="dd477-141">Query this member to identify the manufacturer.</span></span> <span data-ttu-id="dd477-142">Il valore può essere zero se sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="dd477-142">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="dd477-143">**DeviceId**</span><span class="sxs-lookup"><span data-stu-id="dd477-143">**DeviceId**</span></span>
</dt> <dd>

<span data-ttu-id="dd477-144">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd477-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dd477-145">Può essere usato per identificare un determinato chip set.</span><span class="sxs-lookup"><span data-stu-id="dd477-145">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="dd477-146">Eseguire una query su questo membro per identificare il tipo di chip set.</span><span class="sxs-lookup"><span data-stu-id="dd477-146">Query this member to identify the type of chip set.</span></span> <span data-ttu-id="dd477-147">Il valore può essere zero se sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="dd477-147">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="dd477-148">**SubSysId**</span><span class="sxs-lookup"><span data-stu-id="dd477-148">**SubSysId**</span></span>
</dt> <dd>

<span data-ttu-id="dd477-149">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd477-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dd477-150">Può essere usato per identificare un determinato chip set.</span><span class="sxs-lookup"><span data-stu-id="dd477-150">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="dd477-151">Eseguire una query su questo membro per identificare il sottosistema, in genere la scheda specifica.</span><span class="sxs-lookup"><span data-stu-id="dd477-151">Query this member to identify the subsystem, typically the particular board.</span></span> <span data-ttu-id="dd477-152">Il valore può essere zero se sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="dd477-152">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="dd477-153">**Revisione**</span><span class="sxs-lookup"><span data-stu-id="dd477-153">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="dd477-154">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd477-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dd477-155">Può essere usato per identificare un determinato chip set.</span><span class="sxs-lookup"><span data-stu-id="dd477-155">Can be used to help identify a particular chip set.</span></span> <span data-ttu-id="dd477-156">Eseguire una query su questo membro per identificare il livello di revisione del chip set.</span><span class="sxs-lookup"><span data-stu-id="dd477-156">Query this member to identify the revision level of the chip set.</span></span> <span data-ttu-id="dd477-157">Il valore può essere zero se sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="dd477-157">The value can be zero if unknown.</span></span>

</dd> <dt>

<span data-ttu-id="dd477-158">**DeviceIdentifier**</span><span class="sxs-lookup"><span data-stu-id="dd477-158">**DeviceIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="dd477-159">Tipo: **[ **GUID**](guid.md)**</span><span class="sxs-lookup"><span data-stu-id="dd477-159">Type: **[**GUID**](guid.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dd477-160">È possibile eseguire query per controllare le modifiche nel driver e nel chip set.</span><span class="sxs-lookup"><span data-stu-id="dd477-160">Can be queried to check changes in the driver and chip set.</span></span> <span data-ttu-id="dd477-161">Questo GUID è un identificatore univoco per la coppia di driver e chip set.</span><span class="sxs-lookup"><span data-stu-id="dd477-161">This GUID is a unique identifier for the driver and chip set pair.</span></span> <span data-ttu-id="dd477-162">Eseguire una query su questo membro per tenere traccia delle modifiche apportate al driver e al chip set per generare un nuovo profilo per il sottosistema grafico.</span><span class="sxs-lookup"><span data-stu-id="dd477-162">Query this member to track changes to the driver and chip set in order to generate a new profile for the graphics subsystem.</span></span> <span data-ttu-id="dd477-163">DeviceIdentifier può essere usato anche per identificare driver problematici specifici.</span><span class="sxs-lookup"><span data-stu-id="dd477-163">DeviceIdentifier can also be used to identify particular problematic drivers.</span></span>

</dd> <dt>

<span data-ttu-id="dd477-164">**WHQLLevel**</span><span class="sxs-lookup"><span data-stu-id="dd477-164">**WHQLLevel**</span></span>
</dt> <dd>

<span data-ttu-id="dd477-165">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dd477-165">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dd477-166">Usato per determinare il Windows Hardware Quality Labs di convalida (WHQL) per questa coppia di driver e dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dd477-166">Used to determine the Windows Hardware Quality Labs (WHQL) validation level for this driver and device pair.</span></span> <span data-ttu-id="dd477-167">Il valore DWORD è una struttura di data di tipo pack che definisce la data di rilascio del test WHQL più recente superato dal driver.</span><span class="sxs-lookup"><span data-stu-id="dd477-167">The DWORD is a packed date structure defining the date of the release of the most recent WHQL test passed by the driver.</span></span> <span data-ttu-id="dd477-168">È legale eseguire operazioni < e > su questo valore.</span><span class="sxs-lookup"><span data-stu-id="dd477-168">It is legal to perform < and > operations on this value.</span></span> <span data-ttu-id="dd477-169">Di seguito viene illustrato il formato della data.</span><span class="sxs-lookup"><span data-stu-id="dd477-169">The following illustrates the date format.</span></span>



| <span data-ttu-id="dd477-170">BITS</span><span class="sxs-lookup"><span data-stu-id="dd477-170">Bits</span></span>  |  <span data-ttu-id="dd477-171">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd477-171">Description</span></span>                                             |
|-------|-----------------------------------------------|
| <span data-ttu-id="dd477-172">31-16</span><span class="sxs-lookup"><span data-stu-id="dd477-172">31-16</span></span> | <span data-ttu-id="dd477-173">Anno, un numero decimale dal 1999 verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="dd477-173">The year, a decimal number from 1999 upwards.</span></span> |
| <span data-ttu-id="dd477-174">15-8</span><span class="sxs-lookup"><span data-stu-id="dd477-174">15-8</span></span>  | <span data-ttu-id="dd477-175">Mese, numero decimale da 1 a 12.</span><span class="sxs-lookup"><span data-stu-id="dd477-175">The month, a decimal number from 1 to 12.</span></span>     |
| <span data-ttu-id="dd477-176">7-0</span><span class="sxs-lookup"><span data-stu-id="dd477-176">7-0</span></span>   | <span data-ttu-id="dd477-177">Giorno, numero decimale da 1 a 31.</span><span class="sxs-lookup"><span data-stu-id="dd477-177">The day, a decimal number from 1 to 31.</span></span>       |



 

<span data-ttu-id="dd477-178">Vengono usati anche i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="dd477-178">The following values are also used.</span></span>



| <span data-ttu-id="dd477-179">Valore</span><span class="sxs-lookup"><span data-stu-id="dd477-179">Value</span></span>    |  <span data-ttu-id="dd477-180">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd477-180">Description</span></span>                                                     |
|-----|-------------------------------------------------------|
| <span data-ttu-id="dd477-181">0</span><span class="sxs-lookup"><span data-stu-id="dd477-181">0</span></span>   | <span data-ttu-id="dd477-182">Non certificata.</span><span class="sxs-lookup"><span data-stu-id="dd477-182">Not certified.</span></span>                                        |
| <span data-ttu-id="dd477-183">1</span><span class="sxs-lookup"><span data-stu-id="dd477-183">1</span></span>   | <span data-ttu-id="dd477-184">WHQL convalidato, ma non sono disponibili informazioni sulla data.</span><span class="sxs-lookup"><span data-stu-id="dd477-184">WHQL validated, but no date information is available.</span></span> |



 

<span data-ttu-id="dd477-185">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="dd477-185">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

<span data-ttu-id="dd477-186">Per Direct3D9Ex in esecuzione in Windows Vista, Windows Server 2008, Windows 7 e Windows Server 2008 R2 (o un sistema operativo più recente), [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) restituisce 1 per il livello WHQL senza controllare lo stato del driver.</span><span class="sxs-lookup"><span data-stu-id="dd477-186">For Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system), [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) returns 1 for the WHQL level without checking the status of the driver.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd477-187">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd477-187">Remarks</span></span>

<span data-ttu-id="dd477-188">L'esempio di pseudocodice seguente illustra il formato della versione codificato nei membri DriverVersion, DriverVersionLowPart e DriverVersionHighPart.</span><span class="sxs-lookup"><span data-stu-id="dd477-188">The following pseudocode example illustrates the version format encoded in the DriverVersion, DriverVersionLowPart, and DriverVersionHighPart members.</span></span>


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



<span data-ttu-id="dd477-189">Per altre informazioni sulla macro HIWORD, sulla macro LOWORD e sulla struttura LARGE INTEGER, vedere Platform \_ SDK.</span><span class="sxs-lookup"><span data-stu-id="dd477-189">See the Platform SDK for more information about the HIWORD macro, the LOWORD macro, and the LARGE\_INTEGER structure.</span></span>

<span data-ttu-id="dd477-190">MAX \_ DEVICE IDENTIFIER STRING è una costante con la definizione \_ \_ seguente.</span><span class="sxs-lookup"><span data-stu-id="dd477-190">MAX\_DEVICE\_IDENTIFIER\_STRING is a constant with the following definition.</span></span>


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



<span data-ttu-id="dd477-191">I membri VendorId, DeviceId, SubSysId e Revision possono essere usati in tandem per identificare determinati chip set.</span><span class="sxs-lookup"><span data-stu-id="dd477-191">The VendorId, DeviceId, SubSysId, and Revision members can be used in tandem to identify particular chip sets.</span></span> <span data-ttu-id="dd477-192">Tuttavia, usare questi membri con cautela.</span><span class="sxs-lookup"><span data-stu-id="dd477-192">However, use these members with caution.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd477-193">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd477-193">Requirements</span></span>



| <span data-ttu-id="dd477-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd477-194">Requirement</span></span> | <span data-ttu-id="dd477-195">Valore</span><span class="sxs-lookup"><span data-stu-id="dd477-195">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd477-196">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd477-196">Header</span></span><br/> | <dl> <span data-ttu-id="dd477-197"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="dd477-197"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd477-198">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="dd477-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd477-199">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="dd477-199">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
