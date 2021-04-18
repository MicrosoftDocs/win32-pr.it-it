---
description: Rappresenta una coppia chiave/valore.
ms.assetid: B13E9C5F-5B13-4EE5-AE5F-F51B61BDB9B7
title: Classe Msvm_KvpExchangeDataItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeDataItem
- Msvm_KvpExchangeDataItem.InstanceID
- Msvm_KvpExchangeDataItem.Caption
- Msvm_KvpExchangeDataItem.Description
- Msvm_KvpExchangeDataItem.ElementName
- Msvm_KvpExchangeDataItem.Source
- Msvm_KvpExchangeDataItem.Name
- Msvm_KvpExchangeDataItem.Data
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 540c54a694dab1c80a32f9648a90c5b5bf1e48a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318342"
---
# <a name="msvm_kvpexchangedataitem-class"></a><span data-ttu-id="181db-103">\_Classe MSVM KvpExchangeDataItem</span><span class="sxs-lookup"><span data-stu-id="181db-103">Msvm\_KvpExchangeDataItem class</span></span>

<span data-ttu-id="181db-104">Rappresenta una coppia chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="181db-104">Represents a key/value pair.</span></span>

<span data-ttu-id="181db-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="181db-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="181db-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="181db-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_KvpExchangeDataItem : CIM_ManagedElement
{
  string InstanceID;
  string Caption = "Key-Value Pair Exchange Data Item";
  string Description = "Microsoft Key-Value Pair Exchange Data Item";
  string ElementName = "Key-Value Pair Exchange Data Item";
  uint16 Source;
  string Name;
  string Data;
};
```

## <a name="members"></a><span data-ttu-id="181db-107">Members</span><span class="sxs-lookup"><span data-stu-id="181db-107">Members</span></span>

<span data-ttu-id="181db-108">La **classe \_ KvpExchangeDataItem di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="181db-108">The **Msvm\_KvpExchangeDataItem** class has these types of members:</span></span>

-   [<span data-ttu-id="181db-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="181db-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="181db-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="181db-110">Properties</span></span>

<span data-ttu-id="181db-111">La **classe \_ KvpExchangeDataItem di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="181db-111">The **Msvm\_KvpExchangeDataItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="181db-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="181db-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="181db-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="181db-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="181db-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="181db-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="181db-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="181db-115">A short description of the object.</span></span> <span data-ttu-id="181db-116">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="181db-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="181db-117">**Dati**</span><span class="sxs-lookup"><span data-stu-id="181db-117">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="181db-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="181db-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="181db-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="181db-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="181db-120">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="181db-120">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="181db-121">Parte relativa al valore della coppia chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="181db-121">The value portion of the key/value pair.</span></span>

</dd> <dt>

<span data-ttu-id="181db-122">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="181db-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="181db-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="181db-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="181db-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="181db-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="181db-125">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="181db-125">A description of the object.</span></span> <span data-ttu-id="181db-126">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="181db-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="181db-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="181db-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="181db-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="181db-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="181db-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="181db-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="181db-130">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="181db-130">A display name for the object.</span></span> <span data-ttu-id="181db-131">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="181db-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="181db-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="181db-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="181db-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="181db-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="181db-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="181db-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="181db-135">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="181db-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="181db-136">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="181db-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="181db-137">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="181db-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="181db-138">**Nome**</span><span class="sxs-lookup"><span data-stu-id="181db-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="181db-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="181db-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="181db-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="181db-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="181db-141">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="181db-141">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="181db-142">Parte chiave della coppia chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="181db-142">The key portion of the key/value pair.</span></span>



| <span data-ttu-id="181db-143">Chiave</span><span class="sxs-lookup"><span data-stu-id="181db-143">Key</span></span>                                                                                                     | <span data-ttu-id="181db-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="181db-144">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="181db-145"><dt>CSDVersion</dt></span><span class="sxs-lookup"><span data-stu-id="181db-145"><dt>"CSDVersion"</dt></span></span> </dl>                 | <span data-ttu-id="181db-146">Stringa che rappresenta la Service Pack più recente installata nel sistema guest.</span><span class="sxs-lookup"><span data-stu-id="181db-146">A string that represents the latest service pack installed on the guest system.</span></span> <span data-ttu-id="181db-147">Ad esempio, "Service Pack 2".</span><span class="sxs-lookup"><span data-stu-id="181db-147">For example, "Service Pack 2".</span></span> <span data-ttu-id="181db-148">Se non è stato installato alcun Service Pack, questa stringa è vuota.</span><span class="sxs-lookup"><span data-stu-id="181db-148">If no service pack has been installed, this string is empty.</span></span><br/>                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="181db-149"><dt>FullyQualifiedDomainName</dt></span><span class="sxs-lookup"><span data-stu-id="181db-149"><dt>"FullyQualifiedDomainName"</dt></span></span> </dl>   | <span data-ttu-id="181db-150">Stringa che rappresenta il nome DNS completo che identifica in modo univoco il computer locale.</span><span class="sxs-lookup"><span data-stu-id="181db-150">A string that represents the fully qualified DNS name that uniquely identifies the local computer.</span></span> <span data-ttu-id="181db-151">Questo nome è una combinazione del nome host DNS e del nome di dominio DNS, usando il formato *hostname*. *NomeDominio*.</span><span class="sxs-lookup"><span data-stu-id="181db-151">This name is a combination of the DNS host name and the DNS domain name, using the format *HostName*.*DomainName*.</span></span> <span data-ttu-id="181db-152">Se il computer locale è un nodo di un cluster, questo valore è il nome DNS completo del server virtuale del cluster.</span><span class="sxs-lookup"><span data-stu-id="181db-152">If the local computer is a node in a cluster, this value is the fully qualified DNS name of the cluster virtual server.</span></span> <span data-ttu-id="181db-153">Questo valore corrisponde al nome restituito dalla funzione [**presunto GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) quando il parametro *NameType* è "ComputerNameDnsFullyQualified".</span><span class="sxs-lookup"><span data-stu-id="181db-153">This value matches the name returned by the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function when the *NameType* parameter is "ComputerNameDnsFullyQualified".</span></span><br/> |
| <dl> <span data-ttu-id="181db-154"><dt>"IntegrationServicesVersion"</dt></span><span class="sxs-lookup"><span data-stu-id="181db-154"><dt>"IntegrationServicesVersion"</dt></span></span> </dl> | <span data-ttu-id="181db-155">Stringa che rappresenta la versione del Integration Services attualmente installata nella macchina virtuale Guest (ad esempio, "6.1.7000.0").</span><span class="sxs-lookup"><span data-stu-id="181db-155">A string representing the version of the Integration Services currently installed in the guest virtual machine (for example, "6.1.7000.0").</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="181db-156"><dt>"NetworkAddressIPv4"</dt></span><span class="sxs-lookup"><span data-stu-id="181db-156"><dt>"NetworkAddressIPv4"</dt></span></span> </dl>         | <span data-ttu-id="181db-157">Stringa che contiene un elenco delimitato da punti e virgola degli indirizzi IPv4 attualmente assegnati alla macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="181db-157">A string that contains a semicolon-delimited list of the IPv4 addresses currently assigned to the guest virtual machine.</span></span> <span data-ttu-id="181db-158">L'elenco viene aggiornato automaticamente ogni volta che viene apportata una modifica alla configurazione TCP/IP nella macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="181db-158">The list is automatically updated whenever a TCP/IP configuration change occurs on the guest virtual machine.</span></span> <span data-ttu-id="181db-159">Ogni indirizzo è rappresentato nella notazione decimale del punto.</span><span class="sxs-lookup"><span data-stu-id="181db-159">Each address is represented in dot-decimal notation.</span></span> <br/>                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="181db-160"><dt>"NetworkAddressIPv6"</dt></span><span class="sxs-lookup"><span data-stu-id="181db-160"><dt>"NetworkAddressIPv6"</dt></span></span> </dl>         | <span data-ttu-id="181db-161">Stringa che contiene un elenco delimitato da punti e virgola degli indirizzi IPv6 attualmente assegnati alla macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="181db-161">A string that contains a semicolon-delimited list of the IPv6 addresses currently assigned to the guest virtual machine.</span></span> <span data-ttu-id="181db-162">L'elenco viene aggiornato automaticamente ogni volta che viene apportata una modifica alla configurazione TCP/IP nella macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="181db-162">The list is automatically updated whenever a TCP/IP configuration change occurs on the guest virtual machine.</span></span> <span data-ttu-id="181db-163">Ogni indirizzo è rappresentato nella notazione esadecimale con due punti.</span><span class="sxs-lookup"><span data-stu-id="181db-163">Each address is represented in colon-hexadecimal notation.</span></span> <span data-ttu-id="181db-164">Gli elenchi IPv4 e IPv6 non sono sempre sincronizzati.</span><span class="sxs-lookup"><span data-stu-id="181db-164">The IPv4 and IPv6 lists are not guaranteed to be in sync at all times.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="181db-165"><dt>"OSBuildNumber"</dt></span><span class="sxs-lookup"><span data-stu-id="181db-165"><dt>"OSBuildNumber"</dt></span></span> </dl>              | <span data-ttu-id="181db-166">Stringa che rappresenta il numero di build del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="181db-166">A string that represents the build number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="181db-167"><dt>"OSEditionId"</dt></span><span class="sxs-lookup"><span data-stu-id="181db-167"><dt>"OSEditionId"</dt></span></span> </dl>                | <span data-ttu-id="181db-168">Stringa che rappresenta l'edizione (SKU) del sistema operativo della macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="181db-168">A string representing the edition (SKU) of the guest virtual machine operating system.</span></span> <span data-ttu-id="181db-169">Per un elenco di valori possibili, vedere la funzione [**GetProductInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) .</span><span class="sxs-lookup"><span data-stu-id="181db-169">For a list of possible values, see the [**GetProductInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) function.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="181db-170"><dt>OSName</dt></span><span class="sxs-lookup"><span data-stu-id="181db-170"><dt>"OSName"</dt></span></span> </dl>                     | <span data-ttu-id="181db-171">Stringa che rappresenta il nome del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="181db-171">A string that represents the name of the operating system.</span></span> <span data-ttu-id="181db-172">Questo valore deriva dalla voce del registro di sistema seguente: **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProductName**</span><span class="sxs-lookup"><span data-stu-id="181db-172">This value comes from the following registry entry: **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**ProductName**</span></span><br/> <br/>                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="181db-173"><dt>OSMajorVersion</dt></span><span class="sxs-lookup"><span data-stu-id="181db-173"><dt>"OSMajorVersion"</dt></span></span> </dl>             | <span data-ttu-id="181db-174">Stringa che rappresenta il numero di versione principale del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="181db-174">A string that represents the major version number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="181db-175"><dt>OSMinorVersion</dt></span><span class="sxs-lookup"><span data-stu-id="181db-175"><dt>"OSMinorVersion"</dt></span></span> </dl>             | <span data-ttu-id="181db-176">Stringa che rappresenta il numero di versione secondario del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="181db-176">A string that represents the minor version number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="181db-177"><dt>"OSPlatformId"</dt></span><span class="sxs-lookup"><span data-stu-id="181db-177"><dt>"OSPlatformId"</dt></span></span> </dl>               | <span data-ttu-id="181db-178">Stringa che rappresenta la piattaforma del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="181db-178">A string that represents the operating system platform.</span></span> <span data-ttu-id="181db-179">I valori possibili della proprietà **Data** sono "1" per indicare un sistema Windows non supportato e "2" per indicare un sistema Windows supportato.</span><span class="sxs-lookup"><span data-stu-id="181db-179">The possible values of the **Data** property are "1" to indicate an unsupported Windows system and "2" to indicate a supported Windows system.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="181db-180"><dt>OSVersion</dt></span><span class="sxs-lookup"><span data-stu-id="181db-180"><dt>"OSVersion"</dt></span></span> </dl>                  | <span data-ttu-id="181db-181">Stringa che rappresenta la versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="181db-181">A string that represents the operating system version.</span></span> <span data-ttu-id="181db-182">Il formato di questa stringa è *MajorVersion*. *MinorVersion*. *BuildNumber*.</span><span class="sxs-lookup"><span data-stu-id="181db-182">The format of this string is *MajorVersion*.*MinorVersion*.*BuildNumber*.</span></span> <span data-ttu-id="181db-183">Ad esempio, "5.2.3790" per Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="181db-183">For example, "5.2.3790" for Windows Server 2003.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="181db-184"><dt>ProcessorArchitecture</dt></span><span class="sxs-lookup"><span data-stu-id="181db-184"><dt>"ProcessorArchitecture"</dt></span></span> </dl>      | <span data-ttu-id="181db-185">Stringa che rappresenta l'architettura del processore del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="181db-185">A string that represents the processor architecture of the operating system.</span></span> <span data-ttu-id="181db-186">Per un elenco di valori, vedere il membro **wProcessorArchitecture** della struttura [**delle \_ informazioni di sistema**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) .</span><span class="sxs-lookup"><span data-stu-id="181db-186">For a list of values, see the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="181db-187"><dt>ProductType</dt></span><span class="sxs-lookup"><span data-stu-id="181db-187"><dt>"ProductType"</dt></span></span> </dl>                | <span data-ttu-id="181db-188">Stringa che rappresenta il tipo di prodotto.</span><span class="sxs-lookup"><span data-stu-id="181db-188">A string that represents the product type.</span></span> <span data-ttu-id="181db-189">Per un elenco di valori, vedere il membro **wProductType** della struttura [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="181db-189">For a list of values, see the **wProductType** member of the [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="181db-190"><dt>"RDPAddressIPv4"</dt></span><span class="sxs-lookup"><span data-stu-id="181db-190"><dt>"RDPAddressIPv4"</dt></span></span> </dl>             | <span data-ttu-id="181db-191">Stringa che contiene un elenco delimitato da punti e virgola degli indirizzi IPv4 su cui è attualmente in ascolto lo stack RDP della macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="181db-191">A string that contains a semicolon-delimited list of the IPv4 addresses that the guest virtual machine RDP stack is currently listening on.</span></span> <span data-ttu-id="181db-192">Se lo stack RDP non è attualmente in esecuzione, la stringa sarà vuota.</span><span class="sxs-lookup"><span data-stu-id="181db-192">If the RDP stack is not currently running, the string will be empty.</span></span> <span data-ttu-id="181db-193">L'elenco viene aggiornato automaticamente ogni volta che una modifica della configurazione TCP/IP influiscono sullo stack RDP nella macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="181db-193">The list is automatically updated whenever a TCP/IP configuration change affects the RDP stack on the guest virtual machine.</span></span> <span data-ttu-id="181db-194">Ogni indirizzo è rappresentato nella notazione decimale del punto.</span><span class="sxs-lookup"><span data-stu-id="181db-194">Each address is represented in dot-decimal notation.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="181db-195"><dt>"RDPAddressIPv6"</dt></span><span class="sxs-lookup"><span data-stu-id="181db-195"><dt>"RDPAddressIPv6"</dt></span></span> </dl>             | <span data-ttu-id="181db-196">Stringa che contiene un elenco delimitato da punti e virgola degli indirizzi IPv6 su cui è attualmente in ascolto lo stack RDP della macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="181db-196">A string that contains a semicolon-delimited list of the IPv6 addresses that the guest virtual machine RDP stack is currently listening on.</span></span> <span data-ttu-id="181db-197">Se lo stack RDP non è attualmente in esecuzione, la stringa sarà vuota.</span><span class="sxs-lookup"><span data-stu-id="181db-197">If the RDP stack is not currently running, the string will be empty.</span></span> <span data-ttu-id="181db-198">L'elenco viene aggiornato automaticamente ogni volta che una modifica della configurazione TCP/IP influiscono sullo stack RDP nella macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="181db-198">The list is automatically updated whenever a TCP/IP configuration change affects the RDP stack on the guest virtual machine.</span></span> <span data-ttu-id="181db-199">Ogni indirizzo è rappresentato nella notazione esadecimale con due punti.</span><span class="sxs-lookup"><span data-stu-id="181db-199">Each address is represented in colon-hexadecimal notation.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="181db-200"><dt>"ServicePackMajor"</dt></span><span class="sxs-lookup"><span data-stu-id="181db-200"><dt>"ServicePackMajor"</dt></span></span> </dl>           | <span data-ttu-id="181db-201">Stringa che rappresenta il numero di versione principale dell'Service Pack più recente installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="181db-201">A string that represents the major version number of the latest service pack installed on the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="181db-202"><dt>"ServicePackMinor"</dt></span><span class="sxs-lookup"><span data-stu-id="181db-202"><dt>"ServicePackMinor"</dt></span></span> </dl>           | <span data-ttu-id="181db-203">Stringa che rappresenta il numero di versione secondario del Service Pack più recente installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="181db-203">A string that represents the minor version number of the latest service pack installed on the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="181db-204"><dt>"SuiteMask"</dt></span><span class="sxs-lookup"><span data-stu-id="181db-204"><dt>"SuiteMask"</dt></span></span> </dl>                  | <span data-ttu-id="181db-205">Stringa che rappresenta i gruppi di prodotti disponibili nel sistema.</span><span class="sxs-lookup"><span data-stu-id="181db-205">A string that represents the product suites available on the system.</span></span> <span data-ttu-id="181db-206">Questa stringa è una combinazione dei valori del membro **wSuiteMask** della struttura [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="181db-206">This string is a combination of any of the values of the **wSuiteMask** member of the [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="181db-207">**Origine**</span><span class="sxs-lookup"><span data-stu-id="181db-207">**Source**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="181db-208">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="181db-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="181db-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="181db-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="181db-210">Origine dei dati.</span><span class="sxs-lookup"><span data-stu-id="181db-210">The source of the data.</span></span>



| <span data-ttu-id="181db-211">Valore</span><span class="sxs-lookup"><span data-stu-id="181db-211">Value</span></span>                                                                        | <span data-ttu-id="181db-212">Significato</span><span class="sxs-lookup"><span data-stu-id="181db-212">Meaning</span></span>                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="181db-213"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="181db-213"><dt>0</dt></span></span> </dl> | <span data-ttu-id="181db-214">"HostExchangeItems" quando viene eseguito il push dall'host.</span><span class="sxs-lookup"><span data-stu-id="181db-214">"HostExchangeItems" when pushed by the host.</span></span><br/>                                                                                                                                                                                      |
| <dl> <span data-ttu-id="181db-215"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="181db-215"><dt>1</dt></span></span> </dl> | <span data-ttu-id="181db-216">"GuestExchangeItems" quando viene eseguito il push dalla macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="181db-216">"GuestExchangeItems" when pushed by the guest virtual machine.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="181db-217"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="181db-217"><dt>2</dt></span></span> </dl> | <span data-ttu-id="181db-218">"GuestIntrinsicExchangeItems" quando viene popolato automaticamente dalla macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="181db-218">"GuestIntrinsicExchangeItems" when automatically populated by the guest virtual machine.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="181db-219"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="181db-219"><dt>4</dt></span></span> </dl> | <span data-ttu-id="181db-220">Indica che l'elemento è solo host e non è condiviso con la macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="181db-220">Indicates that the item is host-only and not shared with the guest virtual machine.</span></span> <span data-ttu-id="181db-221">Utilizzato con la proprietà **HostOnlyItems** della classe [**MSVM \_ KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="181db-221">Used with the **HostOnlyItems** property of the [**Msvm\_KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md) class.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="181db-222">Commenti</span><span class="sxs-lookup"><span data-stu-id="181db-222">Remarks</span></span>

<span data-ttu-id="181db-223">L'accesso alla **classe \_ KvpExchangeDataItem di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="181db-223">Access to the **Msvm\_KvpExchangeDataItem** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="181db-224">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="181db-224">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="181db-225">Requisiti</span><span class="sxs-lookup"><span data-stu-id="181db-225">Requirements</span></span>



| <span data-ttu-id="181db-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="181db-226">Requirement</span></span> | <span data-ttu-id="181db-227">Valore</span><span class="sxs-lookup"><span data-stu-id="181db-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="181db-228">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="181db-228">Minimum supported client</span></span><br/> | <span data-ttu-id="181db-229">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="181db-229">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="181db-230">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="181db-230">Minimum supported server</span></span><br/> | <span data-ttu-id="181db-231">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="181db-231">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="181db-232">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="181db-232">Namespace</span></span><br/>                | <span data-ttu-id="181db-233">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="181db-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="181db-234">MOF</span><span class="sxs-lookup"><span data-stu-id="181db-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="181db-235"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="181db-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="181db-236">DLL</span><span class="sxs-lookup"><span data-stu-id="181db-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="181db-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="181db-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="181db-238">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="181db-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="181db-239">**\_ManagementName CIM**</span><span class="sxs-lookup"><span data-stu-id="181db-239">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> <dt>

[<span data-ttu-id="181db-240">**\_ManagementName CIM**</span><span class="sxs-lookup"><span data-stu-id="181db-240">**CIM\_ManagedElement**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)
</dt> </dl>

 

