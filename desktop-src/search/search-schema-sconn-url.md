---
description: L' <url> elemento specifica un URL per il percorso di questo connettore di ricerca.
ms.assetid: fdc9e138-2e98-4f01-ab7b-0c3dfad5a4dd
title: Elemento URL simpleLocation (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c40f45ccecb9a1fb81a64f6d749c5050ed1958a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306072"
---
# <a name="simplelocation-url-element-search-connector-schema"></a><span data-ttu-id="652f9-103">Elemento URL simpleLocation (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="652f9-103">simpleLocation url Element (Search Connector Schema)</span></span>

<span data-ttu-id="652f9-104">L' <url> elemento specifica un URL per il percorso di questo connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="652f9-104">The <url> element specifies a URL for the location for this search connector.</span></span> <span data-ttu-id="652f9-105">Questo valore può essere un URL file://normale come definito nella RFC 1738 ( https://www.ietf.org/rfc/rfc1738.txt) documento o o un URL che usa il protocollo KnownFolders:.</span><span class="sxs-lookup"><span data-stu-id="652f9-105">This value can be a regular file:// URL as defined in the RFC 1738 (https://www.ietf.org/rfc/rfc1738.txt) document or or a URL that uses the knownfolders: protocol.</span></span> <span data-ttu-id="652f9-106">Questo elemento non ha elementi figlio e nessun attributo.</span><span class="sxs-lookup"><span data-stu-id="652f9-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="652f9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="652f9-107">Syntax</span></span>


```
<!-- url element for simpleLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0">
                <xs:all>
                    <xs:element name="url" type="xs:anyURI"/>
                    <xs:element name="serialized" minOccurs="0"/>
                </xs:all>
                
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="652f9-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="652f9-108">Element Information</span></span>



| <span data-ttu-id="652f9-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="652f9-109">Parent Element</span></span>                                                                             | <span data-ttu-id="652f9-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="652f9-110">Child Elements</span></span> |
|--------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="652f9-111">Elemento simpleLocation (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="652f9-111">simpleLocation Element (Search Connector Schema)</span></span>](search-schema-sconn-simplelocation.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="652f9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="652f9-112">Remarks</span></span>

<span data-ttu-id="652f9-113">Vedere [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid) per un elenco di GUID di cartelle note.</span><span class="sxs-lookup"><span data-stu-id="652f9-113">See [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid) for a list of known folder GUIDs.</span></span> <span data-ttu-id="652f9-114">Usare il formato seguente per il valore di questo elemento quando si usa il protocollo cartellanota:.</span><span class="sxs-lookup"><span data-stu-id="652f9-114">Use the following format for the value of this element when using the knownfolder: protocol.</span></span>


```
<url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
```



<span data-ttu-id="652f9-115">Nella tabella seguente vengono illustrati i GUID delle cartelle note di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="652f9-115">The following table shows the Windows 7 known folder GUIDs.</span></span>



| <span data-ttu-id="652f9-116">Cartella nota</span><span class="sxs-lookup"><span data-stu-id="652f9-116">Known folder</span></span>                     | <span data-ttu-id="652f9-117">GUID</span><span class="sxs-lookup"><span data-stu-id="652f9-117">GUID</span></span>                                         |
|----------------------------------|----------------------------------------------|
| <span data-ttu-id="652f9-118">\_ADMINTOOLS FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-118">FOLDERID\_AdminTools</span></span>             | <span data-ttu-id="652f9-119">{724EF170-A42D-4FEF-9F-26-B6-0E-84-6F-BA-4F}</span><span class="sxs-lookup"><span data-stu-id="652f9-119">{724EF170-A42D-4FEF-9F-26-B6-0E-84-6F-BA-4F}</span></span> |
| <span data-ttu-id="652f9-120">\_APPUPDATES FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-120">FOLDERID\_AppUpdates</span></span>             | <span data-ttu-id="652f9-121">{a305ce99-f527-492b-8B-1a-7e-76-fa-98-D6-E4}</span><span class="sxs-lookup"><span data-stu-id="652f9-121">{a305ce99-f527-492b-8b-1a-7e-76-fa-98-d6-e4}</span></span> |
| <span data-ttu-id="652f9-122">\_ADDNEWPROGRAMS FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-122">FOLDERID\_AddNewPrograms</span></span>         | <span data-ttu-id="652f9-123">{de61d971-5ebc-4F02-a3-a9-6C-82-89-5e-5C-04}</span><span class="sxs-lookup"><span data-stu-id="652f9-123">{de61d971-5ebc-4f02-a3-a9-6c-82-89-5e-5c-04}</span></span> |
| <span data-ttu-id="652f9-124">\_CDBURNING FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-124">FOLDERID\_CDBurning</span></span>              | <span data-ttu-id="652f9-125">{9E52AB10-F80D-49DF-AC-B8-43 -30-F5-68-78-55}</span><span class="sxs-lookup"><span data-stu-id="652f9-125">{9E52AB10-F80D-49DF-AC-B8-43-30-F5-68-78-55}</span></span> |
| <span data-ttu-id="652f9-126">\_CHANGEREMOVEPROGRAMS FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-126">FOLDERID\_ChangeRemovePrograms</span></span>   | <span data-ttu-id="652f9-127">{df7266ac-9274-4867-8D-55-3B-D6-61-de-87-2D}</span><span class="sxs-lookup"><span data-stu-id="652f9-127">{df7266ac-9274-4867-8d-55-3b-d6-61-de-87-2d}</span></span> |
| <span data-ttu-id="652f9-128">\_COMMONADMINTOOLS FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-128">FOLDERID\_CommonAdminTools</span></span>       | <span data-ttu-id="652f9-129">{D0384E7D-BAC3-4797-8F-14-CB-A2-29-B3-92-B5}</span><span class="sxs-lookup"><span data-stu-id="652f9-129">{D0384E7D-BAC3-4797-8F-14-CB-A2-29-B3-92-B5}</span></span> |
| <span data-ttu-id="652f9-130">\_COMMONOEMLINKS FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-130">FOLDERID\_CommonOEMLinks</span></span>         | <span data-ttu-id="652f9-131">{C1BAE2D0-10DF-4334-BE-DD-7A-A2-0B-22-7A-9D}</span><span class="sxs-lookup"><span data-stu-id="652f9-131">{C1BAE2D0-10DF-4334-BE-DD-7A-A2-0B-22-7A-9D}</span></span> |
| <span data-ttu-id="652f9-132">\_COMMONPROGRAMS FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-132">FOLDERID\_CommonPrograms</span></span>         | <span data-ttu-id="652f9-133">{0139D44E-6AFE-49F2-86-90-3D-AF-CA-E6-FF-B8}</span><span class="sxs-lookup"><span data-stu-id="652f9-133">{0139D44E-6AFE-49F2-86-90-3D-AF-CA-E6-FF-B8}</span></span> |
| <span data-ttu-id="652f9-134">\_COMMONSTARTMENU FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-134">FOLDERID\_CommonStartMenu</span></span>        | <span data-ttu-id="652f9-135">{A4115719-D62E-491D-AA-7C-E7-4B-8B-E3-B0-67}</span><span class="sxs-lookup"><span data-stu-id="652f9-135">{A4115719-D62E-491D-AA-7C-E7-4B-8B-E3-B0-67}</span></span> |
| <span data-ttu-id="652f9-136">\_COMMONSTARTUP FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-136">FOLDERID\_CommonStartup</span></span>          | <span data-ttu-id="652f9-137">{82A5EA35-D9CD-47C5-96 -29-E1-5D-2F-71-4E-6E}</span><span class="sxs-lookup"><span data-stu-id="652f9-137">{82A5EA35-D9CD-47C5-96-29-E1-5D-2F-71-4E-6E}</span></span> |
| <span data-ttu-id="652f9-138">\_COMMONTEMPLATES FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-138">FOLDERID\_CommonTemplates</span></span>        | <span data-ttu-id="652f9-139">{B94237E7-57AC-4347-91-51-B0-8C-6C-32-D1-F7}</span><span class="sxs-lookup"><span data-stu-id="652f9-139">{B94237E7-57AC-4347-91-51-B0-8C-6C-32-D1-F7}</span></span> |
| <span data-ttu-id="652f9-140">\_COMPUTERFOLDER FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-140">FOLDERID\_ComputerFolder</span></span>         | <span data-ttu-id="652f9-141">{0AC0837C-BBF8-452A-85-0D-79-D0-8E-66-7C-A7}</span><span class="sxs-lookup"><span data-stu-id="652f9-141">{0AC0837C-BBF8-452A-85-0D-79-D0-8E-66-7C-A7}</span></span> |
| <span data-ttu-id="652f9-142">\_CONFLICTFOLDER FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-142">FOLDERID\_ConflictFolder</span></span>         | <span data-ttu-id="652f9-143">{4bfefb45-347d-4006-a5-be-AC-0C-B0-56-71-92}</span><span class="sxs-lookup"><span data-stu-id="652f9-143">{4bfefb45-347d-4006-a5-be-ac-0c-b0-56-71-92}</span></span> |
| <span data-ttu-id="652f9-144">\_CONNECTIONSFOLDER FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-144">FOLDERID\_ConnectionsFolder</span></span>      | <span data-ttu-id="652f9-145">{6F0CD92B-2E97-45D1-88-FF-B0-D1-86-B8-DE-DD}</span><span class="sxs-lookup"><span data-stu-id="652f9-145">{6F0CD92B-2E97-45D1-88-FF-B0-D1-86-B8-DE-DD}</span></span> |
| <span data-ttu-id="652f9-146">\_Contatti FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-146">FOLDERID\_Contacts</span></span>               | <span data-ttu-id="652f9-147">{56784854-C6CB-462b-81-69-88-E3-50-AC-B8-82}</span><span class="sxs-lookup"><span data-stu-id="652f9-147">{56784854-c6cb-462b-81-69-88-e3-50-ac-b8-82}</span></span> |
| <span data-ttu-id="652f9-148">\_CONTROLPANELFOLDER FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-148">FOLDERID\_ControlPanelFolder</span></span>     | <span data-ttu-id="652f9-149">{82A74AEB-AEB4-465C-A0-14-D0-97-EE-34-6D-63}</span><span class="sxs-lookup"><span data-stu-id="652f9-149">{82A74AEB-AEB4-465C-A0-14-D0-97-EE-34-6D-63}</span></span> |
| <span data-ttu-id="652f9-150">\_Cookie FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-150">FOLDERID\_Cookies</span></span>                | <span data-ttu-id="652f9-151">{2B0F765D-C0E9-4171-90-8E-08-A6-11-B8-4F-F6}</span><span class="sxs-lookup"><span data-stu-id="652f9-151">{2B0F765D-C0E9-4171-90-8E-08-A6-11-B8-4F-F6}</span></span> |
| <span data-ttu-id="652f9-152">Desktop di FOLDERID \_</span><span class="sxs-lookup"><span data-stu-id="652f9-152">FOLDERID\_Desktop</span></span>                | <span data-ttu-id="652f9-153">{B4BFCC3A-DB2C-424C-B0-29-7F-E9-9A-87-C6-41}</span><span class="sxs-lookup"><span data-stu-id="652f9-153">{B4BFCC3A-DB2C-424C-B0-29-7F-E9-9A-87-C6-41}</span></span> |
| <span data-ttu-id="652f9-154">\_DEVICEMETADATASTORE FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-154">FOLDERID\_DeviceMetadataStore</span></span>    | <span data-ttu-id="652f9-155">{5ce4a5e9-e4eb-479d-B8-9F-13-0C-02-88-61-55}</span><span class="sxs-lookup"><span data-stu-id="652f9-155">{5ce4a5e9-e4eb-479d-b8-9f-13-0c-02-88-61-55}</span></span> |
| <span data-ttu-id="652f9-156">\_Documenti FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-156">FOLDERID\_Documents</span></span>              | <span data-ttu-id="652f9-157">{FDD39AD0-238F-46AF-AD-B4-6C-85-48-03-69-C7}</span><span class="sxs-lookup"><span data-stu-id="652f9-157">{FDD39AD0-238F-46AF-AD-B4-6C-85-48-03-69-C7}</span></span> |
| <span data-ttu-id="652f9-158">\_DOCUMENTSLIBRARY FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-158">FOLDERID\_DocumentsLibrary</span></span>       | <span data-ttu-id="652f9-159">{7b0db17d-9cd2-4a93-97-33 -46-cc-89-02-2e-7C}</span><span class="sxs-lookup"><span data-stu-id="652f9-159">{7b0db17d-9cd2-4a93-97-33-46-cc-89-02-2e-7c}</span></span> |
| <span data-ttu-id="652f9-160">Download di FOLDERID \_</span><span class="sxs-lookup"><span data-stu-id="652f9-160">FOLDERID\_Downloads</span></span>              | <span data-ttu-id="652f9-161">{374de290-123f-4565-91-64-39-C4-92-5e-46-7B}</span><span class="sxs-lookup"><span data-stu-id="652f9-161">{374de290-123f-4565-91-64-39-c4-92-5e-46-7b}</span></span> |
| <span data-ttu-id="652f9-162">FOLDERID \_ Preferiti</span><span class="sxs-lookup"><span data-stu-id="652f9-162">FOLDERID\_Favorites</span></span>              | <span data-ttu-id="652f9-163">{1777F761-68AD-4D8A-87-BD-30-B7-59-FA-33-DD}</span><span class="sxs-lookup"><span data-stu-id="652f9-163">{1777F761-68AD-4D8A-87-BD-30-B7-59-FA-33-DD}</span></span> |
| <span data-ttu-id="652f9-164">\_Tipi di carattere FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-164">FOLDERID\_Fonts</span></span>                  | <span data-ttu-id="652f9-165">{FD228CB7-AE11-4AE3-86-4C-16-F3-91-0A-B8-FE}</span><span class="sxs-lookup"><span data-stu-id="652f9-165">{FD228CB7-AE11-4AE3-86-4C-16-F3-91-0A-B8-FE}</span></span> |
| <span data-ttu-id="652f9-166">\_Giochi FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-166">FOLDERID\_Games</span></span>                  | <span data-ttu-id="652f9-167">{cac52c1a-b53d-4edc-92-D7-6B-2e-8a-C1-94-34}</span><span class="sxs-lookup"><span data-stu-id="652f9-167">{cac52c1a-b53d-4edc-92-d7-6b-2e-8a-c1-94-34}</span></span> |
| <span data-ttu-id="652f9-168">\_GAMETASKS FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-168">FOLDERID\_GameTasks</span></span>              | <span data-ttu-id="652f9-169">{54fae61-4dd8-4787 -80-B6-9-2 -20-C4-B7-0}</span><span class="sxs-lookup"><span data-stu-id="652f9-169">{54fae61-4dd8-4787-80-b6-9-2-20-c4-b7-0}</span></span>     |
| <span data-ttu-id="652f9-170">\_Cronologia FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-170">FOLDERID\_History</span></span>                | <span data-ttu-id="652f9-171">{D9DC8A3B-B784-432E-A7-81-5A-11-30-A7-59-63}</span><span class="sxs-lookup"><span data-stu-id="652f9-171">{D9DC8A3B-B784-432E-A7-81-5A-11-30-A7-59-63}</span></span> |
| <span data-ttu-id="652f9-172">\_Gruppo Home FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-172">FOLDERID\_HomeGroup</span></span>              | <span data-ttu-id="652f9-173">{52528a6b-b9e3-4ADD-B6-d-58-8C-2D-BA-84-2D}</span><span class="sxs-lookup"><span data-stu-id="652f9-173">{52528a6b-b9e3-4add-b6-d-58-8c-2d-ba-84-2d}</span></span>  |
| <span data-ttu-id="652f9-174">\_IMPLICITAPPSHORTCUTS FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-174">FOLDERID\_ImplicitAppShortcuts</span></span>   | <span data-ttu-id="652f9-175">{bcb5256f-79f6-4CEE-B7-25-DC-34-E4-2-FD-46}</span><span class="sxs-lookup"><span data-stu-id="652f9-175">{bcb5256f-79f6-4cee-b7-25-dc-34-e4-2-fd-46}</span></span>  |
| <span data-ttu-id="652f9-176">\_INTERNETCACHE FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-176">FOLDERID\_InternetCache</span></span>          | <span data-ttu-id="652f9-177">{352481E8-33BE-4251-BA-85-60-07-CA-ED-CF-9D}</span><span class="sxs-lookup"><span data-stu-id="652f9-177">{352481E8-33BE-4251-BA-85-60-07-CA-ED-CF-9D}</span></span> |
| <span data-ttu-id="652f9-178">\_INTERNETFOLDER FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-178">FOLDERID\_InternetFolder</span></span>         | <span data-ttu-id="652f9-179">{4D9F7874-4E0C-4904-96-7B-40-B0-D2-0C-3E-4B}</span><span class="sxs-lookup"><span data-stu-id="652f9-179">{4D9F7874-4E0C-4904-96-7B-40-B0-D2-0C-3E-4B}</span></span> |
| <span data-ttu-id="652f9-180">\_Librerie FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-180">FOLDERID\_Libraries</span></span>              | <span data-ttu-id="652f9-181">{1b3ea5dc-B587-4786-B4-EF-BD-1D-C3-32-AE-AE}</span><span class="sxs-lookup"><span data-stu-id="652f9-181">{1b3ea5dc-b587-4786-b4-ef-bd-1d-c3-32-ae-ae}</span></span> |
| <span data-ttu-id="652f9-182">\_Collegamenti FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-182">FOLDERID\_Links</span></span>                  | <span data-ttu-id="652f9-183">{bfb9d5e0-c6a9-404C-B2-B2-AE-6D-B6-AF-49-68}</span><span class="sxs-lookup"><span data-stu-id="652f9-183">{bfb9d5e0-c6a9-404c-b2-b2-ae-6d-b6-af-49-68}</span></span> |
| <span data-ttu-id="652f9-184">\_LocalAppData FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-184">FOLDERID\_LocalAppData</span></span>           | <span data-ttu-id="652f9-185">{F1B32785-6FBA-4FCF-9D-55-7B-8E-7F-15-70-91}</span><span class="sxs-lookup"><span data-stu-id="652f9-185">{F1B32785-6FBA-4FCF-9D-55-7B-8E-7F-15-70-91}</span></span> |
| <span data-ttu-id="652f9-186">\_LOCALAPPDATALOW FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-186">FOLDERID\_LocalAppDataLow</span></span>        | <span data-ttu-id="652f9-187">{A520A1A4-1780-4FF6-BD-18-16-73-43-C5-AF-16}</span><span class="sxs-lookup"><span data-stu-id="652f9-187">{A520A1A4-1780-4FF6-BD-18-16-73-43-C5-AF-16}</span></span> |
| <span data-ttu-id="652f9-188">\_LOCALIZEDRESOURCESDIR FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-188">FOLDERID\_LocalizedResourcesDir</span></span>  | <span data-ttu-id="652f9-189">{2A00375E-224C-49DE-B8-D1-44-0D-F7-EF-3D-DC}</span><span class="sxs-lookup"><span data-stu-id="652f9-189">{2A00375E-224C-49DE-B8-D1-44-0D-F7-EF-3D-DC}</span></span> |
| <span data-ttu-id="652f9-190">\_Musica FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-190">FOLDERID\_Music</span></span>                  | <span data-ttu-id="652f9-191">{4BD8D571-6D19-48D3-BE-97-42-22-20-08-0E-43}</span><span class="sxs-lookup"><span data-stu-id="652f9-191">{4BD8D571-6D19-48D3-BE-97-42-22-20-08-0E-43}</span></span> |
| <span data-ttu-id="652f9-192">\_MUSICLIBRARY FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-192">FOLDERID\_MusicLibrary</span></span>           | <span data-ttu-id="652f9-193">{2112ab0a-C86A-4FFE-a3-68-d-E9-6e-47-1-2e}</span><span class="sxs-lookup"><span data-stu-id="652f9-193">{2112ab0a-c86a-4ffe-a3-68-d-e9-6e-47-1-2e}</span></span>   |
| <span data-ttu-id="652f9-194">\_NETHOOD FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-194">FOLDERID\_NetHood</span></span>                | <span data-ttu-id="652f9-195">{C5ABBF53-E17F-4121-89-00-86-62-6F-C2-C9-73}</span><span class="sxs-lookup"><span data-stu-id="652f9-195">{C5ABBF53-E17F-4121-89-00-86-62-6F-C2-C9-73}</span></span> |
| <span data-ttu-id="652f9-196">\_NETWORKFOLDER FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-196">FOLDERID\_NetworkFolder</span></span>          | <span data-ttu-id="652f9-197">{D20BEEC4-5CA8-4905-AE-3B-BF-25-1E-A0-9B-53}</span><span class="sxs-lookup"><span data-stu-id="652f9-197">{D20BEEC4-5CA8-4905-AE-3B-BF-25-1E-A0-9B-53}</span></span> |
| <span data-ttu-id="652f9-198">\_ORIGINALIMAGES FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-198">FOLDERID\_OriginalImages</span></span>         | <span data-ttu-id="652f9-199">{2C36C0AA-5812-4B87-BF-D0-4C-D0-DF-B1-9B-39}</span><span class="sxs-lookup"><span data-stu-id="652f9-199">{2C36C0AA-5812-4b87-bf-d0-4c-d0-df-b1-9b-39}</span></span> |
| <span data-ttu-id="652f9-200">FOLDERID \_ Fotoalbum</span><span class="sxs-lookup"><span data-stu-id="652f9-200">FOLDERID\_PhotoAlbums</span></span>            | <span data-ttu-id="652f9-201">{69D2CF90-FC33-4FB7-9A-0C-EB-B0-F0-FC-B4-3C}</span><span class="sxs-lookup"><span data-stu-id="652f9-201">{69D2CF90-FC33-4FB7-9A-0C-EB-B0-F0-FC-B4-3C}</span></span> |
| <span data-ttu-id="652f9-202">Immagini di FOLDERID \_</span><span class="sxs-lookup"><span data-stu-id="652f9-202">FOLDERID\_Pictures</span></span>               | <span data-ttu-id="652f9-203">{33E28130-4E1E-4676-83-5A-98-39-5C-3B-C3-BB}</span><span class="sxs-lookup"><span data-stu-id="652f9-203">{33E28130-4E1E-4676-83-5A-98-39-5C-3B-C3-BB}</span></span> |
| <span data-ttu-id="652f9-204">\_PICTURESLIBRARY FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-204">FOLDERID\_PicturesLibrary</span></span>        | <span data-ttu-id="652f9-205">{a990ae9f-A03B-4e80-94-BC-99-12-D7-50-41-4}</span><span class="sxs-lookup"><span data-stu-id="652f9-205">{a990ae9f-a03b-4e80-94-bc-99-12-d7-50-41-4}</span></span>  |
| <span data-ttu-id="652f9-206">FOLDERID \_ playlist</span><span class="sxs-lookup"><span data-stu-id="652f9-206">FOLDERID\_Playlists</span></span>              | <span data-ttu-id="652f9-207">{DE92C1C7-837F-4F69-A3-BB-86-E6-31-20-4A-23}</span><span class="sxs-lookup"><span data-stu-id="652f9-207">{DE92C1C7-837F-4F69-A3-BB-86-E6-31-20-4A-23}</span></span> |
| <span data-ttu-id="652f9-208">\_PRINTERSFOLDER FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-208">FOLDERID\_PrintersFolder</span></span>         | <span data-ttu-id="652f9-209">{76FC4E2D-D6AD-4519-A6-63 -37-BD-56-06-81-85}</span><span class="sxs-lookup"><span data-stu-id="652f9-209">{76FC4E2D-D6AD-4519-A6-63-37-BD-56-06-81-85}</span></span> |
| <span data-ttu-id="652f9-210">\_PRINTHOOD FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-210">FOLDERID\_PrintHood</span></span>              | <span data-ttu-id="652f9-211">{9274BD8D-CFD1-41C3-B3-5E-B1-3F-55-A7-58-F4}</span><span class="sxs-lookup"><span data-stu-id="652f9-211">{9274BD8D-CFD1-41C3-B3-5E-B1-3F-55-A7-58-F4}</span></span> |
| <span data-ttu-id="652f9-212">\_Profilo FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-212">FOLDERID\_Profile</span></span>                | <span data-ttu-id="652f9-213">{5E6C858F-0E22-4760-9A-FE-EA-33-17-B6-71-73}</span><span class="sxs-lookup"><span data-stu-id="652f9-213">{5E6C858F-0E22-4760-9A-FE-EA-33-17-B6-71-73}</span></span> |
| <span data-ttu-id="652f9-214">\_ProgramData FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-214">FOLDERID\_ProgramData</span></span>            | <span data-ttu-id="652f9-215">{62AB5D82-FDC1-4DC3-A9-DD-07-0D-1D-49-5D-97}</span><span class="sxs-lookup"><span data-stu-id="652f9-215">{62AB5D82-FDC1-4DC3-A9-DD-07-0D-1D-49-5D-97}</span></span> |
| <span data-ttu-id="652f9-216">\_PROGRAMFILESX86 FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-216">FOLDERID\_ProgramFilesX86</span></span>        | <span data-ttu-id="652f9-217">{7C5A40EF-A0FB-4BFC-87-4A-C0-F2-E0-B9-FA-8E}</span><span class="sxs-lookup"><span data-stu-id="652f9-217">{7C5A40EF-A0FB-4BFC-87-4A-C0-F2-E0-B9-FA-8E}</span></span> |
| <span data-ttu-id="652f9-218">\_PROGRAMFILESCOMMONX86 FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-218">FOLDERID\_ProgramFilesCommonX86</span></span>  | <span data-ttu-id="652f9-219">{DE974D24-D9C6-4D3E-BF-91-F4-45-51 -20-B9-17}</span><span class="sxs-lookup"><span data-stu-id="652f9-219">{DE974D24-D9C6-4D3E-BF-91-F4-45-51-20-B9-17}</span></span> |
| <span data-ttu-id="652f9-220">\_PROGRAMFILESX64 FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-220">FOLDERID\_ProgramFilesX64</span></span>        | <span data-ttu-id="652f9-221">{6d809377-6af0-444B-89-57-a3-77-3F-02-20-0E}</span><span class="sxs-lookup"><span data-stu-id="652f9-221">{6d809377-6af0-444b-89-57-a3-77-3f-02-20-0e}</span></span> |
| <span data-ttu-id="652f9-222">\_PROGRAMFILESCOMMONX64 FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-222">FOLDERID\_ProgramFilesCommonX64</span></span>  | <span data-ttu-id="652f9-223">{6365d5a7-f0d-45E5-87-F6-d-a5-6B-6a-4F-7D}</span><span class="sxs-lookup"><span data-stu-id="652f9-223">{6365d5a7-f0d-45e5-87-f6-d-a5-6b-6a-4f-7d}</span></span>   |
| <span data-ttu-id="652f9-224">\_Programmi FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-224">FOLDERID\_ProgramFiles</span></span>           | <span data-ttu-id="652f9-225">{905E63B6-C1BF-494E-B2-9C-65-B7-32-D3-D2-1a}</span><span class="sxs-lookup"><span data-stu-id="652f9-225">{905e63b6-c1bf-494e-b2-9c-65-b7-32-d3-d2-1a}</span></span> |
| <span data-ttu-id="652f9-226">\_PROGRAMFILESCOMMON FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-226">FOLDERID\_ProgramFilesCommon</span></span>     | <span data-ttu-id="652f9-227">{F7F1ED05-9F6D-47A2-AA-AE-29-D3-17-C6-F0-66}</span><span class="sxs-lookup"><span data-stu-id="652f9-227">{F7F1ED05-9F6D-47A2-AA-AE-29-D3-17-C6-F0-66}</span></span> |
| <span data-ttu-id="652f9-228">\_Programmi FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-228">FOLDERID\_Programs</span></span>               | <span data-ttu-id="652f9-229">{A77F5D77-2E2B-44C3-A6-A2-AB-A6-01-05-4A-51}</span><span class="sxs-lookup"><span data-stu-id="652f9-229">{A77F5D77-2E2B-44C3-A6-A2-AB-A6-01-05-4A-51}</span></span> |
| <span data-ttu-id="652f9-230">FOLDERID \_ pubblico</span><span class="sxs-lookup"><span data-stu-id="652f9-230">FOLDERID\_Public</span></span>                 | <span data-ttu-id="652f9-231">{DFDF76A2-C82A-4D63-90-6A-56-44-AC-45-73-85}</span><span class="sxs-lookup"><span data-stu-id="652f9-231">{DFDF76A2-C82A-4D63-90-6A-56-44-AC-45-73-85}</span></span> |
| <span data-ttu-id="652f9-232">\_PUBLICDESKTOP FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-232">FOLDERID\_PublicDesktop</span></span>          | <span data-ttu-id="652f9-233">{C4AA340D-F20F-4863-AF-EF-F8-7E-F2-E6-BA-25}</span><span class="sxs-lookup"><span data-stu-id="652f9-233">{C4AA340D-F20F-4863-AF-EF-F8-7E-F2-E6-BA-25}</span></span> |
| <span data-ttu-id="652f9-234">\_PUBLICDOCUMENTS FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-234">FOLDERID\_PublicDocuments</span></span>        | <span data-ttu-id="652f9-235">{ED4824AF-DCE4-45A8-81-E2-FC-79-65-08-36-34}</span><span class="sxs-lookup"><span data-stu-id="652f9-235">{ED4824AF-DCE4-45A8-81-E2-FC-79-65-08-36-34}</span></span> |
| <span data-ttu-id="652f9-236">\_PUBLICDOWNLOADS FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-236">FOLDERID\_PublicDownloads</span></span>        | <span data-ttu-id="652f9-237">{3d644c9b-1fb8-4F30-9B-45-F6-70-23-5F-79-C0}</span><span class="sxs-lookup"><span data-stu-id="652f9-237">{3d644c9b-1fb8-4f30-9b-45-f6-70-23-5f-79-c0}</span></span> |
| <span data-ttu-id="652f9-238">\_PUBLICGAMETASKS FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-238">FOLDERID\_PublicGameTasks</span></span>        | <span data-ttu-id="652f9-239">{debf2536-e1a8-4c59-B6-a2-41-45-86-47-6a-EA}</span><span class="sxs-lookup"><span data-stu-id="652f9-239">{debf2536-e1a8-4c59-b6-a2-41-45-86-47-6a-ea}</span></span> |
| <span data-ttu-id="652f9-240">\_PUBLICMUSIC FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-240">FOLDERID\_PublicMusic</span></span>            | <span data-ttu-id="652f9-241">{3214FAB5-9757 -4298-BB-61-92-A9-DE-AA-44-FF}</span><span class="sxs-lookup"><span data-stu-id="652f9-241">{3214FAB5-9757-4298-BB-61-92-A9-DE-AA-44-FF}</span></span> |
| <span data-ttu-id="652f9-242">\_PUBLICPICTURES FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-242">FOLDERID\_PublicPictures</span></span>         | <span data-ttu-id="652f9-243">{B6EBFB86-6907-413C-9A-F7-4F-C2-AB-F0-7C-C5}</span><span class="sxs-lookup"><span data-stu-id="652f9-243">{B6EBFB86-6907-413C-9A-F7-4F-C2-AB-F0-7C-C5}</span></span> |
| <span data-ttu-id="652f9-244">\_PUBLICRINGTONES FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-244">FOLDERID\_PublicRingtones</span></span>        | <span data-ttu-id="652f9-245">{E555AB60-153B-4D17-9F-04-A5-FE-99-FC-15-EC}</span><span class="sxs-lookup"><span data-stu-id="652f9-245">{E555AB60-153B-4D17-9F-04-A5-FE-99-FC-15-EC}</span></span> |
| <span data-ttu-id="652f9-246">\_PUBLICVIDEOS FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-246">FOLDERID\_PublicVideos</span></span>           | <span data-ttu-id="652f9-247">{2400183A-6185-49FB-A2-D8-4A-39-2A-60-2B-A3}</span><span class="sxs-lookup"><span data-stu-id="652f9-247">{2400183A-6185-49FB-A2-D8-4A-39-2A-60-2B-A3}</span></span> |
| <span data-ttu-id="652f9-248">\_QUICKLAUNCH FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-248">FOLDERID\_QuickLaunch</span></span>            | <span data-ttu-id="652f9-249">{52a4f021-7b75-48a9-9F-6B-4B-87-a2-10-BC-8F}</span><span class="sxs-lookup"><span data-stu-id="652f9-249">{52a4f021-7b75-48a9-9f-6b-4b-87-a2-10-bc-8f}</span></span> |
| <span data-ttu-id="652f9-250">FOLDERID \_ recenti</span><span class="sxs-lookup"><span data-stu-id="652f9-250">FOLDERID\_Recent</span></span>                 | <span data-ttu-id="652f9-251">{AE50C081-EBD2-438A-86-55-8A-09-2E-34-98-7A}</span><span class="sxs-lookup"><span data-stu-id="652f9-251">{AE50C081-EBD2-438A-86-55-8A-09-2E-34-98-7A}</span></span> |
| <span data-ttu-id="652f9-252">\_RECORDEDTVLIBRARY FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-252">FOLDERID\_RecordedTVLibrary</span></span>      | <span data-ttu-id="652f9-253">{1a6fdba2-f42d-4358-a7-98-B7-4D-74-59-26-C5}</span><span class="sxs-lookup"><span data-stu-id="652f9-253">{1a6fdba2-f42d-4358-a7-98-b7-4d-74-59-26-c5}</span></span> |
| <span data-ttu-id="652f9-254">\_RECYCLEBINFOLDER FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-254">FOLDERID\_RecycleBinFolder</span></span>       | <span data-ttu-id="652f9-255">{B7534046-3ECB-4C18-BE-4E-64-CD-4C-B7-D6-AC}</span><span class="sxs-lookup"><span data-stu-id="652f9-255">{B7534046-3ECB-4C18-BE-4E-64-CD-4C-B7-D6-AC}</span></span> |
| <span data-ttu-id="652f9-256">\_RESOURCEDIR FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-256">FOLDERID\_ResourceDir</span></span>            | <span data-ttu-id="652f9-257">{8AD10C31-2ADB-4296-A8-F7-E4-70-12 -32-C9-72}</span><span class="sxs-lookup"><span data-stu-id="652f9-257">{8AD10C31-2ADB-4296-A8-F7-E4-70-12-32-C9-72}</span></span> |
| <span data-ttu-id="652f9-258">FOLDERID \_ ringtones</span><span class="sxs-lookup"><span data-stu-id="652f9-258">FOLDERID\_Ringtones</span></span>              | <span data-ttu-id="652f9-259">{C870044B-F49E-4126-A9-C3-B5-2A-1F-F4-11-E8}</span><span class="sxs-lookup"><span data-stu-id="652f9-259">{C870044B-F49E-4126-A9-C3-B5-2A-1F-F4-11-E8}</span></span> |
| <span data-ttu-id="652f9-260">\_ROAMINGAPPDATA FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-260">FOLDERID\_RoamingAppData</span></span>         | <span data-ttu-id="652f9-261">{3EB685DB-65F9-4CF6-A0-3A-E3-EF-65-72-9F-3D}</span><span class="sxs-lookup"><span data-stu-id="652f9-261">{3EB685DB-65F9-4CF6-A0-3A-E3-EF-65-72-9F-3D}</span></span> |
| <span data-ttu-id="652f9-262">\_SAMPLEPLAYLISTS FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-262">FOLDERID\_SamplePlaylists</span></span>        | <span data-ttu-id="652f9-263">{15CA69B3-30EE-49C1-AC-E1-6B-5E-C3-72-AF-B5}</span><span class="sxs-lookup"><span data-stu-id="652f9-263">{15CA69B3-30EE-49C1-AC-E1-6B-5E-C3-72-AF-B5}</span></span> |
| <span data-ttu-id="652f9-264">\_SAMPLEMUSIC FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-264">FOLDERID\_SampleMusic</span></span>            | <span data-ttu-id="652f9-265">{B250C668-F57D-4EE1-A6-3C-29-0E-E7-D1-AA-1F}</span><span class="sxs-lookup"><span data-stu-id="652f9-265">{B250C668-F57D-4EE1-A6-3C-29-0E-E7-D1-AA-1F}</span></span> |
| <span data-ttu-id="652f9-266">\_SAMPLEPICTURES FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-266">FOLDERID\_SamplePictures</span></span>         | <span data-ttu-id="652f9-267">{C4900540-2379-4C75-84-4B-64-E6-FA-F8-71-6B}</span><span class="sxs-lookup"><span data-stu-id="652f9-267">{C4900540-2379-4C75-84-4B-64-E6-FA-F8-71-6B}</span></span> |
| <span data-ttu-id="652f9-268">\_SAMPLEVIDEOS FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-268">FOLDERID\_SampleVideos</span></span>           | <span data-ttu-id="652f9-269">{859EAD94-2E85-48AD-A7-1A-09-69-CB-56-A6-CD}</span><span class="sxs-lookup"><span data-stu-id="652f9-269">{859EAD94-2E85-48AD-A7-1A-09-69-CB-56-A6-CD}</span></span> |
| <span data-ttu-id="652f9-270">\_Tes partenze FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-270">FOLDERID\_SavedGames</span></span>             | <span data-ttu-id="652f9-271">{4c5c32ff-bb9d-43b0-B5-B4-2D-72-E5-4E-AA-a4}</span><span class="sxs-lookup"><span data-stu-id="652f9-271">{4c5c32ff-bb9d-43b0-b5-b4-2d-72-e5-4e-aa-a4}</span></span> |
| <span data-ttu-id="652f9-272">\_SAVEDSEARCHES FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-272">FOLDERID\_SavedSearches</span></span>          | <span data-ttu-id="652f9-273">{7d1d3a04-Denis-4115-95-CF-2F-29-da-29-20-da}</span><span class="sxs-lookup"><span data-stu-id="652f9-273">{7d1d3a04-debb-4115-95-cf-2f-29-da-29-20-da}</span></span> |
| <span data-ttu-id="652f9-274">FOLDERID \_ Cerca \_ CSC</span><span class="sxs-lookup"><span data-stu-id="652f9-274">FOLDERID\_SEARCH\_CSC</span></span>            | <span data-ttu-id="652f9-275">{ee32e446-31ca-4ABA-81-4F-a5-EB-D2-FD-6D-5e}</span><span class="sxs-lookup"><span data-stu-id="652f9-275">{ee32e446-31ca-4aba-81-4f-a5-eb-d2-fd-6d-5e}</span></span> |
| <span data-ttu-id="652f9-276">\_MAPI ricerca \_ FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-276">FOLDERID\_SEARCH\_MAPI</span></span>           | <span data-ttu-id="652f9-277">{98ec0e18-2098-4d44-86-44-66-97-93 -15-a2-81}</span><span class="sxs-lookup"><span data-stu-id="652f9-277">{98ec0e18-2098-4d44-86-44-66-97-93-15-a2-81}</span></span> |
| <span data-ttu-id="652f9-278">\_SEARCHHOME FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-278">FOLDERID\_SearchHome</span></span>             | <span data-ttu-id="652f9-279">{190337d1-B8CA-4121-a6-39-6D-47-2D-16-97-2a}</span><span class="sxs-lookup"><span data-stu-id="652f9-279">{190337d1-b8ca-4121-a6-39-6d-47-2d-16-97-2a}</span></span> |
| <span data-ttu-id="652f9-280">FOLDERID \_ SendTo</span><span class="sxs-lookup"><span data-stu-id="652f9-280">FOLDERID\_SendTo</span></span>                 | <span data-ttu-id="652f9-281">{8983036C-27C0-404B-8F-08-10-2D-10-DC-FD-74}</span><span class="sxs-lookup"><span data-stu-id="652f9-281">{8983036C-27C0-404B-8F-08-10-2D-10-DC-FD-74}</span></span> |
| <span data-ttu-id="652f9-282">\_STARTMENU FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-282">FOLDERID\_StartMenu</span></span>              | <span data-ttu-id="652f9-283">{625B53C3-AB48-4EC1-BA-1F-A1-EF-41-46-FC-19}</span><span class="sxs-lookup"><span data-stu-id="652f9-283">{625B53C3-AB48-4EC1-BA-1F-A1-EF-41-46-FC-19}</span></span> |
| <span data-ttu-id="652f9-284">Avvio di FOLDERID \_</span><span class="sxs-lookup"><span data-stu-id="652f9-284">FOLDERID\_Startup</span></span>                | <span data-ttu-id="652f9-285">{B97D20BB-F46A-4C97-BA-10-5E-36-08-43-08-54}</span><span class="sxs-lookup"><span data-stu-id="652f9-285">{B97D20BB-F46A-4C97-BA-10-5E-36-08-43-08-54}</span></span> |
| <span data-ttu-id="652f9-286">\_SYNCMANAGERFOLDER FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-286">FOLDERID\_SyncManagerFolder</span></span>      | <span data-ttu-id="652f9-287">{43668BF8-C14E-49B2-97-C9-74-77 -84-D7-84-B7}</span><span class="sxs-lookup"><span data-stu-id="652f9-287">{43668BF8-C14E-49B2-97-C9-74-77-84-D7-84-B7}</span></span> |
| <span data-ttu-id="652f9-288">\_SYNCRESULTSFOLDER FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-288">FOLDERID\_SyncResultsFolder</span></span>      | <span data-ttu-id="652f9-289">{289a9a43-BE44-4057-a4-1B-58-7a-76-D7-E7-F9}</span><span class="sxs-lookup"><span data-stu-id="652f9-289">{289a9a43-be44-4057-a4-1b-58-7a-76-d7-e7-f9}</span></span> |
| <span data-ttu-id="652f9-290">\_SYNCSETUPFOLDER FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-290">FOLDERID\_SyncSetupFolder</span></span>        | <span data-ttu-id="652f9-291">{f214138-B1D3-4A90-BB-a9-27-CB-C0-C5-38-9a}</span><span class="sxs-lookup"><span data-stu-id="652f9-291">{f214138-b1d3-4a90-bb-a9-27-cb-c0-c5-38-9a}</span></span>  |
| <span data-ttu-id="652f9-292">\_Sistema FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-292">FOLDERID\_System</span></span>                 | <span data-ttu-id="652f9-293">{1AC14E77-02E7-4E5D-B7-44-2E-B1-AE-51-98-B7}</span><span class="sxs-lookup"><span data-stu-id="652f9-293">{1AC14E77-02E7-4E5D-B7-44-2E-B1-AE-51-98-B7}</span></span> |
| <span data-ttu-id="652f9-294">\_SYSTEMX86 FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-294">FOLDERID\_SystemX86</span></span>              | <span data-ttu-id="652f9-295">{D65231B0-B2F1-4857-A4-CE-A8-E7-C6-EA-7D-27}</span><span class="sxs-lookup"><span data-stu-id="652f9-295">{D65231B0-B2F1-4857-A4-CE-A8-E7-C6-EA-7D-27}</span></span> |
| <span data-ttu-id="652f9-296">\_Modelli FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-296">FOLDERID\_Templates</span></span>              | <span data-ttu-id="652f9-297">{A63293E8-664E-48DB-A0-79-DF-75-9E-05-09-F7}</span><span class="sxs-lookup"><span data-stu-id="652f9-297">{A63293E8-664E-48DB-A0-79-DF-75-9E-05-09-F7}</span></span> |
| <span data-ttu-id="652f9-298">\_USERPINNED FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-298">FOLDERID\_UserPinned</span></span>             | <span data-ttu-id="652f9-299">{9e3995ab-1f9c-4f13-B8-27 -48-B2-4B-6C-71-74}</span><span class="sxs-lookup"><span data-stu-id="652f9-299">{9e3995ab-1f9c-4f13-b8-27-48-b2-4b-6c-71-74}</span></span> |
| <span data-ttu-id="652f9-300">\_USERSFILES FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-300">FOLDERID\_UsersFiles</span></span>             | <span data-ttu-id="652f9-301">{f3ce0f7c-4901-4acc-86-48-D5-D4-4B-04-EF-8F}</span><span class="sxs-lookup"><span data-stu-id="652f9-301">{f3ce0f7c-4901-4acc-86-48-d5-d4-4b-04-ef-8f}</span></span> |
| <span data-ttu-id="652f9-302">\_USERSLIBRARIES FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-302">FOLDERID\_UsersLibraries</span></span>         | <span data-ttu-id="652f9-303">{a302545d-definitely-464B-AB-E8-61-C8-64-8D-93-9B}</span><span class="sxs-lookup"><span data-stu-id="652f9-303">{a302545d-deff-464b-ab-e8-61-c8-64-8d-93-9b}</span></span> |
| <span data-ttu-id="652f9-304">FOLDERID \_ UserProfile</span><span class="sxs-lookup"><span data-stu-id="652f9-304">FOLDERID\_UserProfiles</span></span>           | <span data-ttu-id="652f9-305">{0762D272-C50A-4BB0-A3-82-69-7D-CD-72-9B-80}</span><span class="sxs-lookup"><span data-stu-id="652f9-305">{0762D272-C50A-4BB0-A3-82-69-7D-CD-72-9B-80}</span></span> |
| <span data-ttu-id="652f9-306">\_USERPROGRAMFILES FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-306">FOLDERID\_UserProgramFiles</span></span>       | <span data-ttu-id="652f9-307">{5cd7aee2-2219-4a67-B8-5D-6C-9C-E1-56 -60-CB}</span><span class="sxs-lookup"><span data-stu-id="652f9-307">{5cd7aee2-2219-4a67-b8-5d-6c-9c-e1-56-60-cb}</span></span> |
| <span data-ttu-id="652f9-308">\_USERPROGRAMFILESCOMMON FOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-308">FOLDERID\_UserProgramFilesCommon</span></span> | <span data-ttu-id="652f9-309">{bcbd3057-ca5c-4622-B4-2D-BC-56-dB-0A-E5-16}</span><span class="sxs-lookup"><span data-stu-id="652f9-309">{bcbd3057-ca5c-4622-b4-2d-bc-56-db-0a-e5-16}</span></span> |
| <span data-ttu-id="652f9-310">Video su FOLDERID \_</span><span class="sxs-lookup"><span data-stu-id="652f9-310">FOLDERID\_Videos</span></span>                 | <span data-ttu-id="652f9-311">{18989B1D-99B5-455B-84-1C-AB-7C-74-E4-GG-FC}</span><span class="sxs-lookup"><span data-stu-id="652f9-311">{18989B1D-99B5-455B-84-1C-AB-7C-74-E4-DD-FC}</span></span> |
| <span data-ttu-id="652f9-312">FOLDERID \_ VideosLibrary {</span><span class="sxs-lookup"><span data-stu-id="652f9-312">FOLDERID\_VideosLibrary {</span></span>        | <span data-ttu-id="652f9-313">491e922f-5643-4AF4-A7-EB-4e-7A-13-8D-81-74}</span><span class="sxs-lookup"><span data-stu-id="652f9-313">491e922f-5643-4af4-a7-eb-4e-7a-13-8d-81-74}</span></span>  |
| <span data-ttu-id="652f9-314">FOLDERID \_ Windows {</span><span class="sxs-lookup"><span data-stu-id="652f9-314">FOLDERID\_Windows {</span></span>              | <span data-ttu-id="652f9-315">F38BF404-1D43-42F2-93-05 -67-DE-0B-28-FC-23}</span><span class="sxs-lookup"><span data-stu-id="652f9-315">F38BF404-1D43-42F2-93-05-67-DE-0B-28-FC-23}</span></span>  |



 

## <a name="examples"></a><span data-ttu-id="652f9-316">Esempio</span><span class="sxs-lookup"><span data-stu-id="652f9-316">Examples</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
    ...
</searchConnectionDescription>
```




```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <simpleLocation>
        <url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
    </simpleLocation>
    ...
</searchConnectionDescription>
```



## <a name="related-topics"></a><span data-ttu-id="652f9-317">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="652f9-317">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="652f9-318">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="652f9-318">KNOWNFOLDERID</span></span>](/windows/desktop/shell/knownfolderid)
</dt> </dl>

 

 
