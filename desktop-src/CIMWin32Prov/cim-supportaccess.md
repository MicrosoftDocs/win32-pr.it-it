---
description: La \_ classe CIM SupportAccess definisce come ottenere assistenza per un prodotto.
ms.assetid: f42a793f-d71e-498e-9c6b-581aa029a0dd
ms.tgt_platform: multiple
title: Classe CIM_SupportAccess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SupportAccess
- CIM_SupportAccess.CommunicationInfo
- CIM_SupportAccess.CommunicationMode
- CIM_SupportAccess.Description
- CIM_SupportAccess.Locale
- CIM_SupportAccess.SupportAccessId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: db5f1dc4331bd50e2fc61899f9d45fe2cdb0eca0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126871"
---
# <a name="cim_supportaccess-class"></a><span data-ttu-id="01b69-103">CIM \_ SupportAccess (classe)</span><span class="sxs-lookup"><span data-stu-id="01b69-103">CIM\_SupportAccess class</span></span>

<span data-ttu-id="01b69-104">La classe **CIM \_ SupportAccess** definisce come ottenere assistenza per un prodotto.</span><span class="sxs-lookup"><span data-stu-id="01b69-104">The **CIM\_SupportAccess** class defines how to obtain assistance for a product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01b69-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="01b69-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="01b69-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="01b69-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="01b69-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="01b69-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="01b69-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="01b69-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="01b69-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01b69-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{80321714-DB31-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_SupportAccess
{
  string CommunicationInfo;
  uint16 CommunicationMode;
  string Description;
  string Locale;
  string SupportAccessId;
};
```

## <a name="members"></a><span data-ttu-id="01b69-110">Members</span><span class="sxs-lookup"><span data-stu-id="01b69-110">Members</span></span>

<span data-ttu-id="01b69-111">La classe **CIM \_ SupportAccess** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="01b69-111">The **CIM\_SupportAccess** class has these types of members:</span></span>

-   [<span data-ttu-id="01b69-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="01b69-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01b69-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="01b69-113">Properties</span></span>

<span data-ttu-id="01b69-114">La classe **CIM \_ SupportAccess** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="01b69-114">The **CIM\_SupportAccess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01b69-115">**CommunicationInfo**</span><span class="sxs-lookup"><span data-stu-id="01b69-115">**CommunicationInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01b69-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="01b69-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01b69-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01b69-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01b69-118">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| FRU \| 002,11 "," MIF. DMTF \| FRU \| 002,12 ")</span><span class="sxs-lookup"><span data-stu-id="01b69-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.11", "MIF.DMTF\|FRU\|002.12")</span></span>
</dt> </dl>

<span data-ttu-id="01b69-119">Dettagli della modalità di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="01b69-119">Details of the communication mode.</span></span> <span data-ttu-id="01b69-120">Ad esempio, se la proprietà **CommunicationMode** è "Phone", questa proprietà specifica il numero di telefono da chiamare.</span><span class="sxs-lookup"><span data-stu-id="01b69-120">For example, if the **CommunicationMode** property is "Phone", then this property specifies the phone number to call.</span></span>

</dd> <dt>

<span data-ttu-id="01b69-121">**CommunicationMode**</span><span class="sxs-lookup"><span data-stu-id="01b69-121">**CommunicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01b69-122">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01b69-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01b69-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01b69-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01b69-124">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Supporto di DMTF \| \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="01b69-124">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="01b69-125">Forma di comunicazione da usare per ottenere supporto.</span><span class="sxs-lookup"><span data-stu-id="01b69-125">Form of communication to use to obtain support.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="01b69-126"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="01b69-126"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>

<span data-ttu-id="01b69-127"><span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>**Telefono** (2)</span><span class="sxs-lookup"><span data-stu-id="01b69-127"><span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>**Phone** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Fax"></span><span id="fax"></span><span id="FAX"></span>

<span data-ttu-id="01b69-128"><span id="Fax"></span><span id="fax"></span><span id="FAX"></span>**Fax** (3)</span><span class="sxs-lookup"><span data-stu-id="01b69-128"><span id="Fax"></span><span id="fax"></span><span id="FAX"></span>**Fax** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="BBS"></span><span id="bbs"></span>

<span data-ttu-id="01b69-129"><span id="BBS"></span><span id="bbs"></span>**BBS** (4)</span><span class="sxs-lookup"><span data-stu-id="01b69-129"><span id="BBS"></span><span id="bbs"></span>**BBS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>

<span data-ttu-id="01b69-130"><span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>**Servizio online** (5)</span><span class="sxs-lookup"><span data-stu-id="01b69-130"><span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>**Online Service** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>

<span data-ttu-id="01b69-131"><span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>**Pagina Web** (6)</span><span class="sxs-lookup"><span data-stu-id="01b69-131"><span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>**Web Page** (6)</span></span>


</dt> <dd>

<span data-ttu-id="01b69-132">Pagina Web</span><span class="sxs-lookup"><span data-stu-id="01b69-132">Webpage</span></span>

</dd> <dt>

<span id="FTP"></span><span id="ftp"></span>

<span data-ttu-id="01b69-133"><span id="FTP"></span><span id="ftp"></span>**FTP** (7)</span><span class="sxs-lookup"><span data-stu-id="01b69-133"><span id="FTP"></span><span id="ftp"></span>**FTP** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>

<span data-ttu-id="01b69-134"><span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>**Posta elettronica** (8)</span><span class="sxs-lookup"><span data-stu-id="01b69-134"><span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>**E-mail** (8)</span></span>


</dt> <dd>

<span data-ttu-id="01b69-135">E-mail</span><span class="sxs-lookup"><span data-stu-id="01b69-135">Email</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="01b69-136">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="01b69-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01b69-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="01b69-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01b69-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01b69-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01b69-139">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Supporto di DMTF \| \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="01b69-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="01b69-140">Descrizione testuale del tipo di supporto fornito.</span><span class="sxs-lookup"><span data-stu-id="01b69-140">Textual description of the type of support provided.</span></span>

</dd> <dt>

<span data-ttu-id="01b69-141">**Impostazioni locali**</span><span class="sxs-lookup"><span data-stu-id="01b69-141">**Locale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01b69-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="01b69-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01b69-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01b69-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01b69-144">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Supporto \| di DMTF 001,2 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="01b69-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.2"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="01b69-145">Area geografica o dialetto della lingua a cui si riferisce questa risorsa di supporto.</span><span class="sxs-lookup"><span data-stu-id="01b69-145">Geographic region or language dialect to which this support resource pertains.</span></span>

</dd> <dt>

<span data-ttu-id="01b69-146">**SupportAccessId**</span><span class="sxs-lookup"><span data-stu-id="01b69-146">**SupportAccessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01b69-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="01b69-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01b69-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="01b69-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01b69-149">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="01b69-149">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="01b69-150">Stringa arbitraria in formato libero definita dal fornitore del prodotto o dall'organizzazione che distribuisce il prodotto.</span><span class="sxs-lookup"><span data-stu-id="01b69-150">Arbitrary free-form string defined by the product vendor or by the organization that deploys the product.</span></span> <span data-ttu-id="01b69-151">Questa proprietà, poiché è una chiave, deve essere univoca nell'intera azienda.</span><span class="sxs-lookup"><span data-stu-id="01b69-151">This property, since it is a key, should be unique throughout the enterprise.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01b69-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="01b69-152">Remarks</span></span>

<span data-ttu-id="01b69-153">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="01b69-153">WMI does not implement this class.</span></span>

<span data-ttu-id="01b69-154">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="01b69-154">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="01b69-155">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="01b69-155">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="01b69-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01b69-156">Requirements</span></span>



| <span data-ttu-id="01b69-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="01b69-157">Requirement</span></span> | <span data-ttu-id="01b69-158">Valore</span><span class="sxs-lookup"><span data-stu-id="01b69-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01b69-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01b69-159">Minimum supported client</span></span><br/> | <span data-ttu-id="01b69-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01b69-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01b69-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01b69-161">Minimum supported server</span></span><br/> | <span data-ttu-id="01b69-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01b69-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01b69-163">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="01b69-163">Namespace</span></span><br/>                | <span data-ttu-id="01b69-164">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="01b69-164">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="01b69-165">MOF</span><span class="sxs-lookup"><span data-stu-id="01b69-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01b69-166"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01b69-166"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="01b69-167">DLL</span><span class="sxs-lookup"><span data-stu-id="01b69-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01b69-168"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01b69-168"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

