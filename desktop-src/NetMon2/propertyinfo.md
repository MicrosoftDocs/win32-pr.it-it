---
description: La struttura dei dati PROPERTYINFO definisce una proprietà del protocollo.
ms.assetid: 878777ab-141d-4cc5-b0c1-f2ac8f770bf0
title: Struttura PROPERTYINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 435b08c5dd5e020dce2bde9be03a0d41299836c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967240"
---
# <a name="propertyinfo-structure"></a><span data-ttu-id="38968-103">Struttura PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="38968-103">PROPERTYINFO structure</span></span>

<span data-ttu-id="38968-104">La struttura dei dati **PROPERTYINFO** definisce una proprietà del protocollo.</span><span class="sxs-lookup"><span data-stu-id="38968-104">The **PROPERTYINFO** data structure defines one property of the protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="38968-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38968-105">Syntax</span></span>


```C++
typedef struct _PROPERTYINFO {
  HPROPERTY hProperty;
  DWORD     Version;
  LPSTR     Label;
  LPSTR     Comment;
  BYTE      DataType;
  BYTE      DataQualifier;
  union {
    LPVOID  lpExtendedInfo;
    LPRANGE lpRange;
    LPSET   lpSet;
    DWORD   Bitmask;
    DWORD   Value;
  };
  WORD      FormatStringSize;
  LPVOID    InstanceData;
} PROPERTYINFO, *LPPROPERTYINFO;
```



## <a name="members"></a><span data-ttu-id="38968-106">Members</span><span class="sxs-lookup"><span data-stu-id="38968-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="38968-107">**hProperty**</span><span class="sxs-lookup"><span data-stu-id="38968-107">**hProperty**</span></span>
</dt> <dd>

<span data-ttu-id="38968-108">Impostare questo campo su zero.</span><span class="sxs-lookup"><span data-stu-id="38968-108">Set this field to zero.</span></span> <span data-ttu-id="38968-109">Nell'output Network Monitor restituisce un handle alla proprietà dopo che la proprietà viene aggiunta al database della proprietà.</span><span class="sxs-lookup"><span data-stu-id="38968-109">On output, Network Monitor returns a handle to the property after the property is added to the property database.</span></span>

</dd> <dt>

<span data-ttu-id="38968-110">**Versione**</span><span class="sxs-lookup"><span data-stu-id="38968-110">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="38968-111">Riservato.</span><span class="sxs-lookup"><span data-stu-id="38968-111">Reserved.</span></span> <span data-ttu-id="38968-112">Deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="38968-112">Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="38968-113">**Etichetta**</span><span class="sxs-lookup"><span data-stu-id="38968-113">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="38968-114">Nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="38968-114">Name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="38968-115">**Commento**</span><span class="sxs-lookup"><span data-stu-id="38968-115">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="38968-116">Descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="38968-116">Description of the property.</span></span> <span data-ttu-id="38968-117">La descrizione viene visualizzata sulla barra di stato Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="38968-117">The description appears on the Network Monitor status bar.</span></span>

</dd> <dt>

<span data-ttu-id="38968-118">**DataType**</span><span class="sxs-lookup"><span data-stu-id="38968-118">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="38968-119">Tipo di dati della proprietà.</span><span class="sxs-lookup"><span data-stu-id="38968-119">Data type of the property.</span></span> <span data-ttu-id="38968-120">Questo membro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="38968-120">This member can have one of the following values.</span></span>



| <span data-ttu-id="38968-121">Valore</span><span class="sxs-lookup"><span data-stu-id="38968-121">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="38968-122">Significato</span><span class="sxs-lookup"><span data-stu-id="38968-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_TYPE_VOID"></span><span id="prop_type_void"></span><dl> <span data-ttu-id="38968-123"><dt>**\_tipo Prop \_ void**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-123"><dt>**PROP\_TYPE\_VOID**</dt></span></span> </dl>                                           | <span data-ttu-id="38968-124">Il tipo di proprietà è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="38968-124">Property type is unknown.</span></span> <span data-ttu-id="38968-125">Non esiste alcuna lunghezza o formato implicito.</span><span class="sxs-lookup"><span data-stu-id="38968-125">There is no implied length or format.</span></span><br/>                                                                                                                                                                                                                                  |
| <span id="PROP_TYPE_SUMMARY"></span><span id="prop_type_summary"></span><dl> <span data-ttu-id="38968-126"><dt>**\_Riepilogo del tipo di Prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-126"><dt>**PROP\_TYPE\_SUMMARY**</dt></span></span> </dl>                                  | <span data-ttu-id="38968-127">Riepilogo del tipo di proprietà.</span><span class="sxs-lookup"><span data-stu-id="38968-127">Summarizing property type.</span></span> <span data-ttu-id="38968-128">Indica la prima istanza di proprietà che il parser connette a un frame.</span><span class="sxs-lookup"><span data-stu-id="38968-128">Indicates the first property instance that the parser attaches to a frame.</span></span> <span data-ttu-id="38968-129">Il \_ \_ Riepilogo del tipo prop può fungere da segnaposto per gruppi di proprietà.</span><span class="sxs-lookup"><span data-stu-id="38968-129">PROP\_TYPE\_SUMMARY can serve as a placeholder for groups of properties.</span></span> <span data-ttu-id="38968-130">Questo valore indica che la proprietà non è definita nella *RFC* del protocollo.</span><span class="sxs-lookup"><span data-stu-id="38968-130">This value indicates that the property is not defined in the protocol *RFC*.</span></span><br/> |
| <span id="PROP_TYPE_BYTE"></span><span id="prop_type_byte"></span><dl> <span data-ttu-id="38968-131"><dt>**tipo di PROP \_ \_ byte**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-131"><dt>**PROP\_TYPE\_BYTE**</dt></span></span> </dl>                                           | <span data-ttu-id="38968-132">Dati numerici con una dimensione di un byte (entità a 8 bit).</span><span class="sxs-lookup"><span data-stu-id="38968-132">Numeric data with a size of one byte (8-bit entity).</span></span><br/>                                                                                                                                                                                                                                             |
| <span id="PROP_TYPE_WORD"></span><span id="prop_type_word"></span><dl> <span data-ttu-id="38968-133"><dt>**tipo di PROP \_ \_ Word**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-133"><dt>**PROP\_TYPE\_WORD**</dt></span></span> </dl>                                           | <span data-ttu-id="38968-134">Dati numerici con una dimensione di due byte (entità a 16 bit).</span><span class="sxs-lookup"><span data-stu-id="38968-134">Numeric data with a size of two bytes (16-bit entity).</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_DWORD"></span><span id="prop_type_dword"></span><dl> <span data-ttu-id="38968-135"><dt>**tipo di PROP \_ \_ DWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-135"><dt>**PROP\_TYPE\_DWORD**</dt></span></span> </dl>                                        | <span data-ttu-id="38968-136">Dati numerici con una dimensione di quattro byte (entità a 32 bit).</span><span class="sxs-lookup"><span data-stu-id="38968-136">Numeric data with a size of four bytes (32-bit entity).</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="PROP_TYPE_LARGEINT"></span><span id="prop_type_largeint"></span><dl> <span data-ttu-id="38968-137"><dt>**\_tipo Prop \_ largeInt**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-137"><dt>**PROP\_TYPE\_LARGEINT**</dt></span></span> </dl>                               | <span data-ttu-id="38968-138">Dati numerici con una dimensione di otto byte (entità a 64 bit).</span><span class="sxs-lookup"><span data-stu-id="38968-138">Numeric data with a size of eight bytes (64-bit entity).</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="PROP_TYPE_ADDR"></span><span id="prop_type_addr"></span><dl> <span data-ttu-id="38968-139"><dt>**\_tipo Prop \_ addr**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-139"><dt>**PROP\_TYPE\_ADDR**</dt></span></span> </dl>                                           | <span data-ttu-id="38968-140">Indirizzo MAC (entità a 6 byte).</span><span class="sxs-lookup"><span data-stu-id="38968-140">MAC address (6-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_TIME"></span><span id="prop_type_time"></span><dl> <span data-ttu-id="38968-141"><dt>**\_ora tipo di Prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-141"><dt>**PROP\_TYPE\_TIME**</dt></span></span> </dl>                                           | <span data-ttu-id="38968-142">Struttura **SYSTEMTIME** .</span><span class="sxs-lookup"><span data-stu-id="38968-142">**SYSTEMTIME** structure.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_STRING"></span><span id="prop_type_string"></span><dl> <span data-ttu-id="38968-143"><dt>**\_stringa di tipo Prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-143"><dt>**PROP\_TYPE\_STRING**</dt></span></span> </dl>                                     | <span data-ttu-id="38968-144">Dati di testo ASCII.</span><span class="sxs-lookup"><span data-stu-id="38968-144">ASCII text data.</span></span> <span data-ttu-id="38968-145">Questo tipo di dati non è con terminazione NULL.</span><span class="sxs-lookup"><span data-stu-id="38968-145">This data type is not NULL-terminated.</span></span> <br/> <span data-ttu-id="38968-146">Per i dati Unicode, quando si specificano dati di testo ASCII, è \_ necessario impostare anche il flag Unicode IFLAG quando viene chiamata la funzione di istanza della proprietà di connessione.</span><span class="sxs-lookup"><span data-stu-id="38968-146">For Unicode data, when ASCII text data is specified, the IFLAG\_UNICODE flag must also be set when the attach property instance function is called.</span></span><br/>                                                                          |
| <span id="PROP_TYPE_IP_ADDRESS"></span><span id="prop_type_ip_address"></span><dl> <span data-ttu-id="38968-147"><dt>**\_ \_ indirizzo IP del tipo Prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-147"><dt>**PROP\_TYPE\_IP\_ADDRESS**</dt></span></span> </dl>                        | <span data-ttu-id="38968-148">Indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="38968-148">IP Address.</span></span> <span data-ttu-id="38968-149">(entità a 4 byte).</span><span class="sxs-lookup"><span data-stu-id="38968-149">(4-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                     |
| <span id="PROP_TYPE_IPX_ADDRESS"></span><span id="prop_type_ipx_address"></span><dl> <span data-ttu-id="38968-150"><dt>**\_ \_ indirizzo IPX di tipo Prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-150"><dt>**PROP\_TYPE\_IPX\_ADDRESS**</dt></span></span> </dl>                     | <span data-ttu-id="38968-151">Indirizzo IPX.</span><span class="sxs-lookup"><span data-stu-id="38968-151">IPX Address.</span></span> <span data-ttu-id="38968-152">(entità a 10 byte).</span><span class="sxs-lookup"><span data-stu-id="38968-152">(10-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                   |
| <span id="PROP_TYPE_BYTESWAPPED_WORD"></span><span id="prop_type_byteswapped_word"></span><dl> <span data-ttu-id="38968-153"><dt>**\_tipo Prop \_ BYTESWAPPED \_ Word**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-153"><dt>**PROP\_TYPE\_BYTESWAPPED\_WORD**</dt></span></span> </dl>      | <span data-ttu-id="38968-154">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="38968-154">Obsolete.</span></span> <span data-ttu-id="38968-155">Per i dati di WORD con scambio di byte, impostare **DataType** su Prop \_ digitare \_ Word e impostare il \_ flag IFLAG scambiato quando si chiama una funzione di istanza della proprietà di **connessione** .</span><span class="sxs-lookup"><span data-stu-id="38968-155">For byte-swapped WORD data, set **DataType** to PROP\_TYPE\_WORD and set the IFLAG\_SWAPPED flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                                |
| <span id="PROP_TYPE_BYTESWAPPED_DWORD"></span><span id="prop_type_byteswapped_dword"></span><dl> <span data-ttu-id="38968-156"><dt>**\_tipo Prop \_ BYTESWAPPED \_ DWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-156"><dt>**PROP\_TYPE\_BYTESWAPPED\_DWORD**</dt></span></span> </dl>   | <span data-ttu-id="38968-157">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="38968-157">Obsolete.</span></span> <span data-ttu-id="38968-158">Per i dati DWORD con scambio di byte, impostare **DataType** su Prop \_ tipo \_ DWORD e impostare il \_ flag IFLAG scambiato quando si chiama una funzione di istanza della proprietà di **connessione** .</span><span class="sxs-lookup"><span data-stu-id="38968-158">For byte-swapped DWORD data, set **DataType** to PROP\_TYPE\_DWORD and set the IFLAG\_SWAPPED flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                              |
| <span id="PROP_TYPE_TYPED_STRING"></span><span id="prop_type_typed_string"></span><dl> <span data-ttu-id="38968-159"><dt>**\_ \_ stringa tipizzata di tipo Prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-159"><dt>**PROP\_TYPE\_TYPED\_STRING**</dt></span></span> </dl>                  | <span data-ttu-id="38968-160">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="38968-160">Obsolete.</span></span> <span data-ttu-id="38968-161">Per i dati di tipo stringa variabile, impostare **DataType** su Prop \_ tipo \_ stringa e impostare il \_ flag Unicode IFLAG quando si chiama una funzione di istanza della proprietà di **connessione** .</span><span class="sxs-lookup"><span data-stu-id="38968-161">For variable-type string data, set **DataType** to PROP\_TYPE\_STRING and set the IFLAG\_UNICODE flag when calling an **Attach** property instance function.</span></span><br/>                                                                                                                           |
| <span id="PROP_TYPE_RAW_DATA"></span><span id="prop_type_raw_data"></span><dl> <span data-ttu-id="38968-162"><dt>**tipi di PROP \_ \_ dati non elaborati \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-162"><dt>**PROP\_TYPE\_RAW\_DATA**</dt></span></span> </dl>                              | <span data-ttu-id="38968-163">Dati non elaborati di lunghezza e formato sconosciuti.</span><span class="sxs-lookup"><span data-stu-id="38968-163">Raw data of unknown length and format.</span></span><br/>                                                                                                                                                                                                                                                           |
| <span id="PROP_TYPE_COMMENT"></span><span id="prop_type_comment"></span><dl> <span data-ttu-id="38968-164"><dt>**\_commento tipo \_ prop**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-164"><dt>**PROP\_TYPE\_COMMENT**</dt></span></span> </dl>                                  | <span data-ttu-id="38968-165">Uguale al tipo di PROP \_ \_ void.</span><span class="sxs-lookup"><span data-stu-id="38968-165">Same as PROP\_TYPE\_VOID.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="PROP_TYPE_SRCFRIENDLYNAME"></span><span id="prop_type_srcfriendlyname"></span><dl> <span data-ttu-id="38968-166"><dt>**\_tipo Prop \_ SRCFRIENDLYNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-166"><dt>**PROP\_TYPE\_SRCFRIENDLYNAME**</dt></span></span> </dl>          | <span data-ttu-id="38968-167">Indirizzo del nome descrittivo dell'origine.</span><span class="sxs-lookup"><span data-stu-id="38968-167">Address of source-friendly name.</span></span> <span data-ttu-id="38968-168">Network Monitor non fornisce il supporto predefinito per la formattazione per questo tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="38968-168">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                |
| <span id="PROP_TYPE_DSTFRIENDLYNAME"></span><span id="prop_type_dstfriendlyname"></span><dl> <span data-ttu-id="38968-169"><dt>**\_tipo Prop \_ DSTFRIENDLYNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-169"><dt>**PROP\_TYPE\_DSTFRIENDLYNAME**</dt></span></span> </dl>          | <span data-ttu-id="38968-170">Indirizzo del nome descrittivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="38968-170">Address of destination friendly name.</span></span> <span data-ttu-id="38968-171">Network Monitor non fornisce il supporto predefinito per la formattazione per questo tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="38968-171">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                           |
| <span id="PROP_TYPE_TOKENRING_ADDRESS"></span><span id="prop_type_tokenring_address"></span><dl> <span data-ttu-id="38968-172"><dt>**\_ \_ Indirizzo Tokenring di tipo Prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-172"><dt>**PROP\_TYPE\_TOKENRING\_ADDRESS**</dt></span></span> </dl>   | <span data-ttu-id="38968-173">Indirizzo token-ring.</span><span class="sxs-lookup"><span data-stu-id="38968-173">Token-ring address.</span></span> <span data-ttu-id="38968-174">Network Monitor non fornisce il supporto predefinito per la formattazione per questo tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="38968-174">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                             |
| <span id="PROP_TYPE_FDDI_ADDRESS"></span><span id="prop_type_fddi_address"></span><dl> <span data-ttu-id="38968-175"><dt>**\_ \_ Indirizzo FDDI di tipo Prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-175"><dt>**PROP\_TYPE\_FDDI\_ADDRESS**</dt></span></span> </dl>                  | <span data-ttu-id="38968-176">Indirizzo FDDI.</span><span class="sxs-lookup"><span data-stu-id="38968-176">FDDI address.</span></span> <span data-ttu-id="38968-177">Network Monitor non fornisce il supporto predefinito per la formattazione per questo tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="38968-177">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                                   |
| <span id="PROP_TYPE_ETHERNET_ADDRESS"></span><span id="prop_type_ethernet_address"></span><dl> <span data-ttu-id="38968-178"><dt>**\_ \_ indirizzo Ethernet del tipo Prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-178"><dt>**PROP\_TYPE\_ETHERNET\_ADDRESS**</dt></span></span> </dl>      | <span data-ttu-id="38968-179">Indirizzo Ethernet.</span><span class="sxs-lookup"><span data-stu-id="38968-179">Ethernet address.</span></span> <span data-ttu-id="38968-180">Network Monitor non fornisce il supporto predefinito per la formattazione per questo tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="38968-180">Network Monitor does not provide built-in formatting support for this data type.</span></span><br/>                                                                                                                                                                                               |
| <span id="PROP_TYPE_OBJECT_IDENTIFIER"></span><span id="prop_type_object_identifier"></span><dl> <span data-ttu-id="38968-181"><dt>**\_ \_ identificatore oggetto di tipo Prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-181"><dt>**PROP\_TYPE\_OBJECT\_IDENTIFIER**</dt></span></span> </dl>   | <span data-ttu-id="38968-182">Identificatore di oggetto SNMP con codifica BER.</span><span class="sxs-lookup"><span data-stu-id="38968-182">BER-encoded SNMP object identifier.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="PROP_TYPE_VINES_IP_ADDRESS"></span><span id="prop_type_vines_ip_address"></span><dl> <span data-ttu-id="38968-183"><dt>**\_ \_ indirizzo IP delle viti di tipo \_ prop \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-183"><dt>**PROP\_TYPE\_VINES\_IP\_ADDRESS**</dt></span></span> </dl>     | <span data-ttu-id="38968-184">Indirizzo IP viti (entità a 6 byte).</span><span class="sxs-lookup"><span data-stu-id="38968-184">Vines IP address (6-byte entity).</span></span><br/>                                                                                                                                                                                                                                                                |
| <span id="PROP_TYPE_VAR_LEN_SMALL_INT"></span><span id="prop_type_var_len_small_int"></span><dl> <span data-ttu-id="38968-185"><dt>**\_tipo Prop \_ var \_ Len \_ small \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-185"><dt>**PROP\_TYPE\_VAR\_LEN\_SMALL\_INT**</dt></span></span> </dl> | <span data-ttu-id="38968-186">Valore numerico senza una lunghezza predeterminata, ma non più di 8 byte.</span><span class="sxs-lookup"><span data-stu-id="38968-186">Numeric value without a pre-determined length, but no more than 8 bytes long.</span></span> <span data-ttu-id="38968-187">La lunghezza dei dati associati determina la lunghezza del valore.</span><span class="sxs-lookup"><span data-stu-id="38968-187">The length of the attached data determines the length of the value.</span></span><br/>                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="38968-188">**Qualificatore dataqualifier**</span><span class="sxs-lookup"><span data-stu-id="38968-188">**DataQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="38968-189">Qualificatore dei dati di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="38968-189">The data qualifier of a property.</span></span> <span data-ttu-id="38968-190">Questo membro fornisce informazioni precise sul tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="38968-190">This member provides precise information about the data type.</span></span>

<span data-ttu-id="38968-191">**Dataqualifier** può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="38968-191">**DataQualifier** can have one of the following values.</span></span>



| <span data-ttu-id="38968-192">Valore</span><span class="sxs-lookup"><span data-stu-id="38968-192">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="38968-193">Significato</span><span class="sxs-lookup"><span data-stu-id="38968-193">Meaning</span></span>                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROP_QUAL_NONE"></span><span id="prop_qual_none"></span><dl> <span data-ttu-id="38968-194"><dt>**PROP \_ qual \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-194"><dt>**PROP\_QUAL\_NONE**</dt></span></span> </dl>                                      | <span data-ttu-id="38968-195">Il tipo di dati della proprietà è l'unica specifica della proprietà.</span><span class="sxs-lookup"><span data-stu-id="38968-195">The property data type is the only specification of the property.</span></span> <br/> <span data-ttu-id="38968-196">Quando questo valore è impostato, il membro Union della struttura viene impostato su **null**, quindi viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="38968-196">When this value is set, the union member of the structure is set to **NULL**, and then ignored.</span></span><br/>                                                                                                                                        |
| <span id="PROP_QUAL_RANGE"></span><span id="prop_qual_range"></span><dl> <span data-ttu-id="38968-197"><dt>**intervallo di proprietà PROP \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-197"><dt>**PROP\_QUAL\_RANGE**</dt></span></span> </dl>                                   | <span data-ttu-id="38968-198">Il valore numerico dovrebbe essere compreso in un intervallo specificato.</span><span class="sxs-lookup"><span data-stu-id="38968-198">The numeric value is expected to be within a given range.</span></span> <span data-ttu-id="38968-199">Definire l'intervallo nel membro **lpRange** .</span><span class="sxs-lookup"><span data-stu-id="38968-199">Define the range in the **lpRange** member.</span></span><br/>                                                                                                                                                                                                                |
| <span id="PROP_QUAL_SET"></span><span id="prop_qual_set"></span><dl> <span data-ttu-id="38968-200"><dt>**SET di proprietà PROP \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-200"><dt>**PROP\_QUAL\_SET**</dt></span></span> </dl>                                         | <span data-ttu-id="38968-201">Il valore di una proprietà viene confrontato con un set di valori specificati nel membro **lpSet** dell'Unione della struttura.</span><span class="sxs-lookup"><span data-stu-id="38968-201">The value of a property is compared to a set of values that are specified in the **lpSet** member of the structure's union.</span></span> <span data-ttu-id="38968-202">Il valore di una proprietà può essere un **byte**, una **parola**, un **DWORD**, un **largeInt** o un' **ora**.</span><span class="sxs-lookup"><span data-stu-id="38968-202">The value of a property can be a **BYTE**, **WORD**, **DWORD**, **LARGEINT** or **TIME**.</span></span><br/>                                                                                                |
| <span id="PROP_QUAL_BITFIELD"></span><span id="prop_qual_bitfield"></span><dl> <span data-ttu-id="38968-203"><dt>**PROP \_ qual \_ bit**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-203"><dt>**PROP\_QUAL\_BITFIELD**</dt></span></span> </dl>                          | <span data-ttu-id="38968-204">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="38968-204">Obsolete.</span></span><br/>                                                                                                                                                                                                                                                                                                            |
| <span id="PROP_QUAL_LABELED_SET"></span><span id="prop_qual_labeled_set"></span><dl> <span data-ttu-id="38968-205"><dt>**\_set con \_ etichetta \_ set di prop**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-205"><dt>**PROP\_QUAL\_LABELED\_SET**</dt></span></span> </dl>                | <span data-ttu-id="38968-206">Il valore di una proprietà viene confrontato con un valore in un set di coppie di etichette di valore.</span><span class="sxs-lookup"><span data-stu-id="38968-206">The value of a property is compared to a value in a set of value label pairs.</span></span> <span data-ttu-id="38968-207">Le coppie di etichette di valore vengono specificate nel membro **lpSet** dell'Unione della struttura.</span><span class="sxs-lookup"><span data-stu-id="38968-207">The value label pairs are specified in the **lpSet** member of the structure's union.</span></span> <br/> <span data-ttu-id="38968-208">Al momento della visualizzazione, se il valore della proprietà corrisponde a un valore nel set, verranno visualizzati sia un valore che l'etichetta associata.</span><span class="sxs-lookup"><span data-stu-id="38968-208">At display time, if the value of the property matches a value in the set, then both a value, and the associated label are displayed.</span></span><br/> |
| <span id="PROP_QUAL_LABELED_BITFIELD"></span><span id="prop_qual_labeled_bitfield"></span><dl> <span data-ttu-id="38968-209"><dt>**PROP \_ qual \_ etichettato \_ bit**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-209"><dt>**PROP\_QUAL\_LABELED\_BITFIELD**</dt></span></span> </dl> | <span data-ttu-id="38968-210">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="38968-210">Obsolete.</span></span> <span data-ttu-id="38968-211">Usare invece i flag PROPa \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="38968-211">Use PROP\_QUAL\_FLAGS instead.</span></span><br/>                                                                                                                                                                                                                                                                             |
| <span id="PROP_QUAL_CONST"></span><span id="prop_qual_const"></span><dl> <span data-ttu-id="38968-212"><dt>**PROP \_ qual \_ const**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-212"><dt>**PROP\_QUAL\_CONST**</dt></span></span> </dl>                                   | <span data-ttu-id="38968-213">Il valore di una proprietà viene confrontato con una costante specificata nel membro **value** dell'Unione.</span><span class="sxs-lookup"><span data-stu-id="38968-213">The value of a property is compared to a constant that is specified in the **Value** member of the union.</span></span> <br/> <span data-ttu-id="38968-214">In fase di visualizzazione, se i valori della proprietà e la costante non corrispondono, viene visualizzato un messaggio di errore formattato con il valore impostato come normale.</span><span class="sxs-lookup"><span data-stu-id="38968-214">At display time, if the property values and constant do not match, a formatted error message appears with the value set as Normal.</span></span><br/>                                                             |
| <span id="PROP_QUAL_FLAGS"></span><span id="prop_qual_flags"></span><dl> <span data-ttu-id="38968-215"><dt>**flag di PROP \_ qual \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-215"><dt>**PROP\_QUAL\_FLAGS**</dt></span></span> </dl>                                   | <span data-ttu-id="38968-216">Il valore della proprietà viene confrontato con i bit specifici identificati nel membro **lpSet** dell'Unione.</span><span class="sxs-lookup"><span data-stu-id="38968-216">The value of the property is compared to specific BITs identified in the **lpSet** member of the union.</span></span><br/>                                                                                                                                                                                                              |
| <span id="PROP_QUAL_ARRAY"></span><span id="prop_qual_array"></span><dl> <span data-ttu-id="38968-217"><dt>**\_Array prop qual \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38968-217"><dt>**PROP\_QUAL\_ARRAY**</dt></span></span> </dl>                                   | <span data-ttu-id="38968-218">Il valore di una proprietà specifica una matrice di valori.</span><span class="sxs-lookup"><span data-stu-id="38968-218">The value of a property specifies an array of values.</span></span> <span data-ttu-id="38968-219">La lunghezza dei dati associati determina la lunghezza di una matrice.</span><span class="sxs-lookup"><span data-stu-id="38968-219">The length of attached data determines the length of an array.</span></span> <br/> <span data-ttu-id="38968-220">Quando \_ \_ si imposta il valore della matrice prop, il membro Union della struttura dei dati **PROPERTYINFO** viene impostato su **null** e viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="38968-220">When the PROP\_QUAL\_ARRAY value is set, the union member of the **PROPERTYINFO** data structure is set to **NULL** and ignored.</span></span><br/>                                                    |



 

</dd> <dt>

<span data-ttu-id="38968-221">**lpExtendedInfo**</span><span class="sxs-lookup"><span data-stu-id="38968-221">**lpExtendedInfo**</span></span>
</dt> <dd>

<span data-ttu-id="38968-222">Riservato (membro di Union).</span><span class="sxs-lookup"><span data-stu-id="38968-222">Reserved (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="38968-223">**lpRange**</span><span class="sxs-lookup"><span data-stu-id="38968-223">**lpRange**</span></span>
</dt> <dd>

<span data-ttu-id="38968-224">Puntatore a una struttura di [intervallo](range.md) che definisce un intervallo di valori.</span><span class="sxs-lookup"><span data-stu-id="38968-224">Pointer to a [RANGE](range.md) structure that defines a range of values.</span></span> <span data-ttu-id="38968-225">Questo membro deve essere impostato se il membro **dataqualifier** di questa struttura è impostato su Prop \_ qual \_ Range (membro di Union).</span><span class="sxs-lookup"><span data-stu-id="38968-225">This member must be set if the **DataQualifier** member of this structure is set to PROP\_QUAL\_RANGE (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="38968-226">**lpSet**</span><span class="sxs-lookup"><span data-stu-id="38968-226">**lpSet**</span></span>
</dt> <dd>

<span data-ttu-id="38968-227">Puntatore a una struttura di [set](set.md) che specifica un set di valori o di etichette.</span><span class="sxs-lookup"><span data-stu-id="38968-227">Pointer to a [SET](set.md) structure that specifies a set of values or labels.</span></span> <span data-ttu-id="38968-228">Questo membro deve essere impostato se il membro **dataqualifier** della struttura è impostato su Prop quale \_ \_ set, prop quale \_ \_ labeled \_ set o prop \_ qual \_ Flags (member of Union).</span><span class="sxs-lookup"><span data-stu-id="38968-228">This member must be set if the **DataQualifier** member of the structure is set to PROP\_QUAL\_SET, PROP\_QUAL\_LABELED\_SET, or PROP\_QUAL\_FLAGS (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="38968-229">**Maschera**</span><span class="sxs-lookup"><span data-stu-id="38968-229">**Bitmask**</span></span>
</dt> <dd>

<span data-ttu-id="38968-230">Obsoleto (membro di Union).</span><span class="sxs-lookup"><span data-stu-id="38968-230">Obsolete (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="38968-231">**Valore**</span><span class="sxs-lookup"><span data-stu-id="38968-231">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="38968-232">Valore costante utilizzato quando **dataqualifier** è impostato su Prop \_ qual \_ const (membro di Union).</span><span class="sxs-lookup"><span data-stu-id="38968-232">Constant value used when the **DataQualifier** is set to PROP\_QUAL\_CONST (member of union).</span></span>

</dd> <dt>

<span data-ttu-id="38968-233">**FormatStringSize**</span><span class="sxs-lookup"><span data-stu-id="38968-233">**FormatStringSize**</span></span>
</dt> <dd>

<span data-ttu-id="38968-234">Dimensione massima utilizzata solo per la descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="38968-234">Maximum size used only for the property description.</span></span>

</dd> <dt>

<span data-ttu-id="38968-235">**InstanceData**</span><span class="sxs-lookup"><span data-stu-id="38968-235">**InstanceData**</span></span>
</dt> <dd>

<span data-ttu-id="38968-236">Consente di specificare la funzione Format chiamata per formattare i dati visualizzati per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="38968-236">Specify the format function that is called to format the displayed data for the property.</span></span> <span data-ttu-id="38968-237">Per utilizzare il formattatore generico, specificare la funzione **FormatPropertyInstance** .</span><span class="sxs-lookup"><span data-stu-id="38968-237">To use the generic formatter, specify the **FormatPropertyInstance** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38968-238">Commenti</span><span class="sxs-lookup"><span data-stu-id="38968-238">Remarks</span></span>

<span data-ttu-id="38968-239">La struttura **PROPERTYINFO** viene utilizzata nelle chiamate alla funzione [AddProperty](/previous-versions/bb251873(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="38968-239">The **PROPERTYINFO** structure is used in calls to the [AddProperty](/previous-versions/bb251873(v=msdn.10)) function.</span></span> <span data-ttu-id="38968-240">La funzione **AddProperty** aggiunge una singola definizione di proprietà al [*database della proprietà*](p.md)parser.</span><span class="sxs-lookup"><span data-stu-id="38968-240">The **AddProperty** function adds a single property definition to the parser [*property database*](p.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="38968-241">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38968-241">Requirements</span></span>



| <span data-ttu-id="38968-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="38968-242">Requirement</span></span> | <span data-ttu-id="38968-243">Valore</span><span class="sxs-lookup"><span data-stu-id="38968-243">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="38968-244">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38968-244">Minimum supported client</span></span><br/> | <span data-ttu-id="38968-245">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="38968-245">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="38968-246">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38968-246">Minimum supported server</span></span><br/> | <span data-ttu-id="38968-247">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="38968-247">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="38968-248">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38968-248">Header</span></span><br/>                   | <dl> <span data-ttu-id="38968-249"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="38968-249"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38968-250">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38968-250">See also</span></span>

<dl> <dt>

<span data-ttu-id="38968-251">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="38968-251">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="38968-252">INTERVALLO</span><span class="sxs-lookup"><span data-stu-id="38968-252">RANGE</span></span>](range.md)
</dt> <dt>

[<span data-ttu-id="38968-253">SET</span><span class="sxs-lookup"><span data-stu-id="38968-253">SET</span></span>](set.md)
</dt> </dl>

 

