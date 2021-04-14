---
title: Unione SoHAttributeValue (NapProtocol. h)
description: Definisce il contenuto del membro del tipo in una struttura SoHAttribute.
ms.assetid: 53b30455-33a5-4cf5-8d4e-f0fa8e4e1a12
keywords:
- NAP Unione SoHAttributeValue
topic_type:
- apiref
api_name:
- SoHAttributeValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36660e4e360ff0df31bb3a76d06c50e5d366c894
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478442"
---
# <a name="sohattributevalue-union"></a><span data-ttu-id="b9c49-104">Unione SoHAttributeValue</span><span class="sxs-lookup"><span data-stu-id="b9c49-104">SoHAttributeValue union</span></span>

> [!Note]  
> <span data-ttu-id="b9c49-105">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="b9c49-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b9c49-106">L'Unione **SoHAttributeValue** definisce il contenuto del membro del **tipo** in una struttura [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) .</span><span class="sxs-lookup"><span data-stu-id="b9c49-106">The **SoHAttributeValue** union defines the contents of the **type** member in a [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) structure.</span></span> <span data-ttu-id="b9c49-107">La struttura dell'Unione **SoHAttributeValue** è determinata dall'oggetto [**SoHAttributeType**](sohattributetype-enum.md) specificato nel membro del **tipo** della struttura [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) .</span><span class="sxs-lookup"><span data-stu-id="b9c49-107">The structure of the **SoHAttributeValue** union is determined by the [**SoHAttributeType**](sohattributetype-enum.md) specified in the **type** member of the [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9c49-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9c49-108">Syntax</span></span>


```C++
typedef union tagSoHAttributeValue {
  SystemHealthEntityId     idVal;
  struct tagIpv4Addresses {
    UINT16      count;
    Ipv4Address *addresses;
  } v4AddressesVal;
  struct tagIpv6Addresses {
    UINT16      count;
    Ipv6Address *addresses;
  } v6AddressesVal;
  ResultCodes              codesVal;
  FILETIME                 dateTimeVal;
  struct tagVendorSpecific {
    UINT32 vendorId;
    UINT16 size;
    BYTE   *vendorSpecificData;
  } vendorSpecificVal;
  UINT8                    uint8Val;
  struct tagOctetString {
    UINT16 size;
    BYTE   *data;
  } octetStringVal;
} SoHAttributeValue;
```



## <a name="members"></a><span data-ttu-id="b9c49-109">Members</span><span class="sxs-lookup"><span data-stu-id="b9c49-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="b9c49-110">**idVal**</span><span class="sxs-lookup"><span data-stu-id="b9c49-110">**idVal**</span></span>
</dt> <dd>

<span data-ttu-id="b9c49-111">**caso (sohAttributeTypeSystemHealthId)**</span><span class="sxs-lookup"><span data-stu-id="b9c49-111">**case(sohAttributeTypeSystemHealthId)**</span></span>

<span data-ttu-id="b9c49-112">[SystemHealthEntityId](nap-datatypes.md) univoco che contiene l'ID dell'agente integrità sistema (SHA) o del servizio di convalida dell'integrità di sistema che ha costruito questo pacchetto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="b9c49-112">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the System Health Agent (SHA) or System Health Validator (SHV) that constructed this [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="b9c49-113">**v4AddressesVal**</span><span class="sxs-lookup"><span data-stu-id="b9c49-113">**v4AddressesVal**</span></span>
</dt> <dd>

<span data-ttu-id="b9c49-114">**caso (sohAttributeTypeIpv4FixupServers)**</span><span class="sxs-lookup"><span data-stu-id="b9c49-114">**case(sohAttributeTypeIpv4FixupServers)**</span></span>

<span data-ttu-id="b9c49-115">Indirizzi IPv4 dei server di correzione utilizzati dal sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="b9c49-115">The IPv4 addresses of the fix-up servers in use by the NAP system.</span></span>

<dl> <dt>

<span data-ttu-id="b9c49-116">**count**</span><span class="sxs-lookup"><span data-stu-id="b9c49-116">**count**</span></span>
</dt> <dd>

<span data-ttu-id="b9c49-117">Numero di indirizzi IPv4 nel membro degli **indirizzi** compresi nell'intervallo da 1 a [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b9c49-117">The number of IPv4 addresses in the **addresses** member in the range 1 to [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9c49-118">**indirizzi**</span><span class="sxs-lookup"><span data-stu-id="b9c49-118">**addresses**</span></span>
</dt> <dd>

<span data-ttu-id="b9c49-119">Matrice di strutture [**IndirizzoIPv4**](/windows/win32/api/naptypes/ns-naptypes-ipv4address) che contengono gli indirizzi IPv4.</span><span class="sxs-lookup"><span data-stu-id="b9c49-119">An array of [**Ipv4Address**](/windows/win32/api/naptypes/ns-naptypes-ipv4address) structures that contain the IPv4 addresses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b9c49-120">**v6AddressesVal**</span><span class="sxs-lookup"><span data-stu-id="b9c49-120">**v6AddressesVal**</span></span>
</dt> <dd>

<span data-ttu-id="b9c49-121">**caso (sohAttributeTypeIpv6FixupServers)**</span><span class="sxs-lookup"><span data-stu-id="b9c49-121">**case(sohAttributeTypeIpv6FixupServers)**</span></span>

<span data-ttu-id="b9c49-122">Indirizzi IPv6 dei server di correzione utilizzati dal sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="b9c49-122">The IPv6 addresses of the fix-up servers in use by the NAP system.</span></span>

<dl> <dt>

<span data-ttu-id="b9c49-123">**count**</span><span class="sxs-lookup"><span data-stu-id="b9c49-123">**count**</span></span>
</dt> <dd>

<span data-ttu-id="b9c49-124">Numero di indirizzi IPv4 nel membro degli **indirizzi** compresi nell'intervallo da 1 a [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b9c49-124">The number of IPv4 addresses in the **addresses** member in the range 1 to [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9c49-125">**indirizzi**</span><span class="sxs-lookup"><span data-stu-id="b9c49-125">**addresses**</span></span>
</dt> <dd>

<span data-ttu-id="b9c49-126">Matrice di strutture [**Ipv6Address**](/windows/win32/api/naptypes/ns-naptypes-ipv6address) che contengono gli indirizzi IPv4.</span><span class="sxs-lookup"><span data-stu-id="b9c49-126">An array of [**Ipv6Address**](/windows/win32/api/naptypes/ns-naptypes-ipv6address) structures that contain the IPv4 addresses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b9c49-127">**codesVal**</span><span class="sxs-lookup"><span data-stu-id="b9c49-127">**codesVal**</span></span>
</dt> <dd>

<span data-ttu-id="b9c49-128">**Case (sohAttributeTypeComplianceResultCodes, sohAttributeTypeErrorCodes)**</span><span class="sxs-lookup"><span data-stu-id="b9c49-128">**case(sohAttributeTypeComplianceResultCodes, sohAttributeTypeErrorCodes)**</span></span>

<span data-ttu-id="b9c49-129">Struttura [**ResultCodes**](/windows/win32/api/naptypes/ns-naptypes-resultcodes) che contiene i codici di risultato della conformità definiti dall'applicazione delle costanti di [**errore**](nap-error-constants.md)client o NAP.</span><span class="sxs-lookup"><span data-stu-id="b9c49-129">A [**ResultCodes**](/windows/win32/api/naptypes/ns-naptypes-resultcodes) structure that contains either the application defined compliance result codes of the client or [**NAP error constants**](nap-error-constants.md).</span></span> <span data-ttu-id="b9c49-130">Un pacchetto di rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) deve contenere questo TLV o il **sohAttributeTypeFailureCategory** TLV.</span><span class="sxs-lookup"><span data-stu-id="b9c49-130">An [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet must contain this TLV or the **sohAttributeTypeFailureCategory** TLV.</span></span>

</dd> <dt>

<span data-ttu-id="b9c49-131">**dateTimeVal**</span><span class="sxs-lookup"><span data-stu-id="b9c49-131">**dateTimeVal**</span></span>
</dt> <dd>

<span data-ttu-id="b9c49-132">**Case (sohAttributeTypeTimeOfLastUpdate, sohAttributeTypeSoHGenerationTime)**</span><span class="sxs-lookup"><span data-stu-id="b9c49-132">**case(sohAttributeTypeTimeOfLastUpdate, sohAttributeTypeSoHGenerationTime)**</span></span>

<span data-ttu-id="b9c49-133">Struttura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) che contiene l'ora dell'ultimo aggiornamento del rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) o del tempo di generazione del rapporto di **integrità** .</span><span class="sxs-lookup"><span data-stu-id="b9c49-133">A [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that contains the time of the last [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) update or the **SoH** generation time.</span></span>

</dd> <dt>

<span data-ttu-id="b9c49-134">**vendorSpecificVal**</span><span class="sxs-lookup"><span data-stu-id="b9c49-134">**vendorSpecificVal**</span></span>
</dt> <dd>

<span data-ttu-id="b9c49-135">**caso (sohAttributeTypeVendorSpecific)**</span><span class="sxs-lookup"><span data-stu-id="b9c49-135">**case(sohAttributeTypeVendorSpecific)**</span></span>

<span data-ttu-id="b9c49-136">Dati specifici dell'applicazione definiti dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="b9c49-136">Application-specific data that is defined by the vendor.</span></span>

<dl> <dt>

<span data-ttu-id="b9c49-137">**vendorId**</span><span class="sxs-lookup"><span data-stu-id="b9c49-137">**vendorId**</span></span>
</dt> <dd>

<span data-ttu-id="b9c49-138">Identificatore a 4 byte che definisce l'ID della coppia SHA/convalida.</span><span class="sxs-lookup"><span data-stu-id="b9c49-138">A 4-byte identifier that defines the SHA/SHV pair ID.</span></span> <span data-ttu-id="b9c49-139">I primi 3 byte sono il codice SMI assegnato dall'IETF del fornitore e l'ultimo byte identifica il componente stesso.</span><span class="sxs-lookup"><span data-stu-id="b9c49-139">The first 3 bytes are the IETF-assigned SMI code of the vendor, and the last byte identifies the component itself.</span></span> <span data-ttu-id="b9c49-140">Quando si implementa un SHA o un servizio di convalida dell'integrità di sistema, non usare i valori ID assegnati ai componenti interni di integrità del sistema Microsoft nelle [**costanti del fornitore NAP**](nap-vendor-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b9c49-140">When implementing a SHA or SHV, do not use the ID values assigned to internal Microsoft system health components on [**NAP vendor constants**](nap-vendor-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9c49-141">**size**</span><span class="sxs-lookup"><span data-stu-id="b9c49-141">**size**</span></span>
</dt> <dd>

<span data-ttu-id="b9c49-142">Dimensione, in byte, dei dati del fornitore nell'intervallo compreso tra 0 e ([**maxSoHAttributeSize**](nap-type-constants.md) -4).</span><span class="sxs-lookup"><span data-stu-id="b9c49-142">The size, in bytes, of the vendor data in the range 0 to ([**maxSoHAttributeSize**](nap-type-constants.md) - 4).</span></span>

</dd> <dt>

<span data-ttu-id="b9c49-143">**vendorSpecificData**</span><span class="sxs-lookup"><span data-stu-id="b9c49-143">**vendorSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="b9c49-144">Puntatore ai dati specifici del fornitore nell'ordine dei byte di rete.</span><span class="sxs-lookup"><span data-stu-id="b9c49-144">A pointer to the vendor specific data in network byte order.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b9c49-145">**uint8Val**</span><span class="sxs-lookup"><span data-stu-id="b9c49-145">**uint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="b9c49-146">**Case (sohAttributeTypeHealthClass, sohAttributeTypeFailureCategory, sohAttributeTypeExtendedIsolationState)**</span><span class="sxs-lookup"><span data-stu-id="b9c49-146">**case(sohAttributeTypeHealthClass, sohAttributeTypeFailureCategory,sohAttributeTypeExtendedIsolationState)**</span></span>

<span data-ttu-id="b9c49-147">La classe di integrità, la categoria di errore o lo stato di isolamento esteso di un componente NAP come valore [**HealthClassValue**](healthclassvalue-enum.md) o [**FailureCategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) o come struttura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) .</span><span class="sxs-lookup"><span data-stu-id="b9c49-147">The health class, failure category, or extended isolation state of a NAP component as either a [**HealthClassValue**](healthclassvalue-enum.md) or [**FailureCategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) value, or a [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b9c49-148">**octetStringVal**</span><span class="sxs-lookup"><span data-stu-id="b9c49-148">**octetStringVal**</span></span>
</dt> <dd>

<span data-ttu-id="b9c49-149">**default**</span><span class="sxs-lookup"><span data-stu-id="b9c49-149">**default**</span></span>

<span data-ttu-id="b9c49-150">I valori degli attributi seguenti sono stringhe ottetto:</span><span class="sxs-lookup"><span data-stu-id="b9c49-150">The following attributes' values are octet strings:</span></span>

-   <span data-ttu-id="b9c49-151">sohAttributeTypeSoftwareVersion</span><span class="sxs-lookup"><span data-stu-id="b9c49-151">sohAttributeTypeSoftwareVersion</span></span>
-   <span data-ttu-id="b9c49-152">sohAttributeTypeClientId</span><span class="sxs-lookup"><span data-stu-id="b9c49-152">sohAttributeTypeClientId</span></span>
-   <span data-ttu-id="b9c49-153">sohAttributeTypeProductName</span><span class="sxs-lookup"><span data-stu-id="b9c49-153">sohAttributeTypeProductName</span></span>
-   <span data-ttu-id="b9c49-154">sohAttributeTypeHealthClassStatus</span><span class="sxs-lookup"><span data-stu-id="b9c49-154">sohAttributeTypeHealthClassStatus</span></span>

<span data-ttu-id="b9c49-155">Per la compatibilità con le edizioni, tutti gli attributi non riconosciuti vengono restituiti come stringhe ottetto.</span><span class="sxs-lookup"><span data-stu-id="b9c49-155">For forward compatibility, all unrecognized attributes are returned as octet strings.</span></span> <span data-ttu-id="b9c49-156">**i dati** devono essere in ordine byte di rete.</span><span class="sxs-lookup"><span data-stu-id="b9c49-156">**data** must be in network byte order.</span></span>

<dl> <dt>

<span data-ttu-id="b9c49-157">**size**</span><span class="sxs-lookup"><span data-stu-id="b9c49-157">**size**</span></span>
</dt> <dd>

<span data-ttu-id="b9c49-158">Dimensione, in byte, dei **dati** nell'intervallo compreso tra 0 e [**maxSoHAttributeSize**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b9c49-158">The size, in bytes, of **data** in the range 0 to [**maxSoHAttributeSize**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9c49-159">**data**</span><span class="sxs-lookup"><span data-stu-id="b9c49-159">**data**</span></span>
</dt> <dd>

<span data-ttu-id="b9c49-160">Puntatore al valore della stringa ottetto.</span><span class="sxs-lookup"><span data-stu-id="b9c49-160">A pointer to the octet string value.</span></span>

</dd> </dl> </dd> </dl>

## <a name="actual-data-layout"></a><span data-ttu-id="b9c49-161">Layout dati effettivo</span><span class="sxs-lookup"><span data-stu-id="b9c49-161">Actual data layout</span></span>

<span data-ttu-id="b9c49-162">A causa della natura dell'ambiente di pubblicazione dell'SDK, le unioni non sono chiaramente rappresentate nei blocchi di sintassi.</span><span class="sxs-lookup"><span data-stu-id="b9c49-162">Due to the nature of the SDK publishing environment, unions are not clearly represented in syntax blocks.</span></span> <span data-ttu-id="b9c49-163">Di seguito è illustrata la sintassi effettiva del file di intestazione NapProtocol. h.</span><span class="sxs-lookup"><span data-stu-id="b9c49-163">Here is the actual syntax from the NapProtocol.h header file.</span></span>


```C++
#include <windows.h>

typedef [switch_type(SoHAttributeType)] 
   union tagSoHAttributeValue
   {
      [case(sohAttributeTypeSystemHealthId)]
         SystemHealthEntityId idVal;
   
      [case(sohAttributeTypeIpv4FixupServers)]
         struct tagIpv4Addresses
         {
            [range(1, maxIpv4CountPerSoHAttribute)] 
               UINT16 count;
            [size_is(count)] Ipv4Address* addresses;
         } v4AddressesVal;

      [case(sohAttributeTypeIpv6FixupServers)]
         struct tagIpv6Addresses
         {
            [range(1, maxIpv6CountPerSoHAttribute)]
               UINT16 count;
            [size_is(count)] Ipv6Address* addresses;
         } v6AddressesVal;

      [case(sohAttributeTypeComplianceResultCodes, 
            sohAttributeTypeErrorCodes)]
         ResultCodes codesVal;

      [case(sohAttributeTypeTimeOfLastUpdate, 
            sohAttributeTypeSoHGenerationTime)]
         FILETIME dateTimeVal;

      [case(sohAttributeTypeVendorSpecific)]
         struct tagVendorSpecific
         {
            UINT32 vendorId;
            [range(0, maxSoHAttributeSize - 4)] 
               UINT16 size;
            [size_is(size)] BYTE* vendorSpecificData;
         } vendorSpecificVal;

      [case(sohAttributeTypeHealthClass, 
            sohAttributeTypeFailureCategory,
            sohAttributeTypeExtendedIsolationState)]
         UINT8 uint8Val;

      [default]
         struct tagOctetString
         {
            [range(0, maxSoHAttributeSize)] UINT16 size;
            [size_is(size)] BYTE* data;
         } octetStringVal;

   } SoHAttributeValue;
};
```



## <a name="remarks"></a><span data-ttu-id="b9c49-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="b9c49-164">Remarks</span></span>

<span data-ttu-id="b9c49-165">Questi tipi di attributo vengono utilizzati dal sistema NAP:</span><span class="sxs-lookup"><span data-stu-id="b9c49-165">These attribute types are consumed by the NAP system:</span></span>

-   <span data-ttu-id="b9c49-166">sohAttributeTypeSystemHealthId</span><span class="sxs-lookup"><span data-stu-id="b9c49-166">sohAttributeTypeSystemHealthId</span></span>
-   <span data-ttu-id="b9c49-167">sohAttributeTypeIpv4FixupServers</span><span class="sxs-lookup"><span data-stu-id="b9c49-167">sohAttributeTypeIpv4FixupServers</span></span>
-   <span data-ttu-id="b9c49-168">sohAttributeTypeIpv6FixupServers</span><span class="sxs-lookup"><span data-stu-id="b9c49-168">sohAttributeTypeIpv6FixupServers</span></span>
-   <span data-ttu-id="b9c49-169">sohAttributeTypeComplianceResultCodes</span><span class="sxs-lookup"><span data-stu-id="b9c49-169">sohAttributeTypeComplianceResultCodes</span></span>
-   <span data-ttu-id="b9c49-170">sohAttributeTypeFailureCategory</span><span class="sxs-lookup"><span data-stu-id="b9c49-170">sohAttributeTypeFailureCategory</span></span>

<span data-ttu-id="b9c49-171">Gli altri [**SoHAttributeTypes**](sohattributetype-enum.md) sono intesi esclusivamente come linee guida descrittive per l'utilizzo da parte di Shas e SHV.</span><span class="sxs-lookup"><span data-stu-id="b9c49-171">The rest of the [**SoHAttributeTypes**](sohattributetype-enum.md) are meant purely as prescriptive guidance for usage by SHAs and SHVs.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9c49-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9c49-172">Requirements</span></span>



| <span data-ttu-id="b9c49-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9c49-173">Requirement</span></span> | <span data-ttu-id="b9c49-174">Valore</span><span class="sxs-lookup"><span data-stu-id="b9c49-174">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9c49-175">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9c49-175">Minimum supported client</span></span><br/> | <span data-ttu-id="b9c49-176">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b9c49-176">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b9c49-177">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9c49-177">Minimum supported server</span></span><br/> | <span data-ttu-id="b9c49-178">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b9c49-178">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b9c49-179">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9c49-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9c49-180"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9c49-180"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="b9c49-181">IDL</span><span class="sxs-lookup"><span data-stu-id="b9c49-181">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b9c49-182"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b9c49-182"><dt>NapProtocol.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9c49-183">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9c49-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9c49-184">Riferimento NAP</span><span class="sxs-lookup"><span data-stu-id="b9c49-184">NAP Reference</span></span>](nap-reference.md)
</dt> <dt>

[<span data-ttu-id="b9c49-185">Strutture NAP</span><span class="sxs-lookup"><span data-stu-id="b9c49-185">NAP Structures</span></span>](nap-structures.md)
</dt> </dl>

 

