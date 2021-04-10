---
title: Elenco di profili, criteri e client
description: Elenco di profili, criteri e client
ms.assetid: 8bfbe4f6-b098-43c8-acb7-2c489ebe0ad3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc10fb3a59a2461d9138f8b209f69d31eb3fa1fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963208"
---
# <a name="listing-profiles-policies-and-clients"></a><span data-ttu-id="209df-103">Elenco di profili, criteri e client</span><span class="sxs-lookup"><span data-stu-id="209df-103">Listing Profiles, Policies, and Clients</span></span>

<span data-ttu-id="209df-104">Il codice VBScript seguente enumera i profili, i criteri e i client nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="209df-104">The following VBScript code enumerates the profiles, policies, and clients on the local computer.</span></span>


```VB
Option Explicit

Const DATA_STORE_LOCAL = 0
Const PROPERTY_SDO_NAME = 2

Const PROPERTY_IAS_POLICIES_COLLECTION = 1025
Const PROPERTY_IAS_PROFILES_COLLECTION = 1026

Const PROPERTY_IAS_PROTOCOLS_COLLECTION = 1027

Const PROPERTY_RADIUS_CLIENTS_COLLECTION = 1029

Const PROPERTY_CLIENT_REQUIRE_SIGNATURE = 1024 
Const PROPERTY_CLIENT_SHARED_SECRET = 1026 
Const PROPERTY_CLIENT_NAS_MANUFACTURER = 1027 
Const PROPERTY_CLIENT_ADDRESS = 1028 


Const PROPERTY_PROFILE_ATTRIBUTES_COLLECTION = 1024
Const PROPERTY_ATTRIBUTE_ID = 1024
Const PROPERTY_ATTRIBUTE_DISPLAY_NAME = 1035

Const PROPERTY_POLICY_CONSTRAINT = 1024
Const PROPERTY_POLICY_MERIT = 1025 
Const PROPERTY_POLICY_PROFILE_NAME = 1028 
Const PROPERTY_POLICY_ACTION = 1029
Const PROPERTY_POLICY_CONDITIONS_COLLECTION = 1030

Const PROPERTY_CONDITION_TEXT = 1024


Dim sdoMachine, sdoServiceSDO
Dim sdoCollProfiles, sdoCollProtocols, sdoCollClients, sdoCollPolicies
Dim sdoCollAttributes, sdoCollConditions
Dim sdoRADIUS
Dim vtProfile, vtProtocol, vtClient, vtPolicy, vtAttribute, vtCondition

Set sdoMachine = CreateObject("IAS.SdoMachine")
sdoMachine.Attach vbNullString
Set sdoServiceSDO = sdoMachine.GetServiceSDO(DATA_STORE_LOCAL, "IAS")

'
' List Profiles and Attributes
'
Set sdoCollProfiles = sdoServiceSDO.GetProperty(PROPERTY_IAS_PROFILES_COLLECTION)

WScript.Echo sdoCollProfiles.Count & " Profiles found."
For Each vtProfile in sdoCollProfiles
    WScript.Echo "- " & Chr(34) & vtProfile.GetProperty(PROPERTY_SDO_NAME) & Chr(34)
    set sdoCollAttributes = vtProfile.GetProperty(PROPERTY_PROFILE_ATTRIBUTES_COLLECTION)
    WScript.Echo sdoCollAttributes.Count & " Attributes found."
    For Each vtAttribute in sdoCollAttributes
        WScript.Echo " - " & Chr(34) & vtAttribute.GetProperty(PROPERTY_SDO_NAME) & Chr(34)
        WScript.Echo "   LDAPName " & Chr(34) & vtAttribute.GetProperty(PROPERTY_ATTRIBUTE_DISPLAY_NAME) & Chr(34)
        WScript.Echo "   Id " & Chr(34) & vtAttribute.GetProperty(PROPERTY_ATTRIBUTE_ID) & Chr(34)
    Next 'vtAttribute
Next 'vtProfile

'
' List Policies and Conditions
'
Set sdoCollPolicies = sdoServiceSDO.GetProperty(PROPERTY_IAS_POLICIES_COLLECTION)

WScript.Echo sdoCollPolicies.Count & " Policies found."
For Each vtPolicy in sdoCollPolicies
    WScript.Echo "- " & Chr(34) & vtPolicy.GetProperty(PROPERTY_SDO_NAME) & Chr(34)

    WScript.Echo "  Merit " & Chr(34) & vtPolicy.GetProperty(PROPERTY_POLICY_MERIT) & Chr(34)
    WScript.Echo "  Policy Name " & Chr(34) & vtPolicy.GetProperty(PROPERTY_POLICY_PROFILE_NAME) & Chr(34)

    set sdoCollConditions = vtPolicy.GetProperty(PROPERTY_POLICY_CONDITIONS_COLLECTION)
    WScript.Echo sdoCollConditions.Count & " Conditions found."
    For Each vtCondition in sdoCollConditions
        WScript.Echo " - " & Chr(34) & vtCondition.GetProperty(PROPERTY_SDO_NAME) & Chr(34)
        WScript.Echo "   Text " & Chr(34) & vtCondition.GetProperty(PROPERTY_CONDITION_TEXT) & Chr(34)
    Next 'vtCondition
Next 'vtPolicy 

'
' List Clients
'
Set sdoCollProtocols = sdoServiceSDO.GetProperty(PROPERTY_IAS_PROTOCOLS_COLLECTION)
Set sdoRADIUS = sdoCollProtocols.Item("Microsoft Radius Protocol")
Set sdoCollClients = sdoRADIUS.GetProperty(PROPERTY_RADIUS_CLIENTS_COLLECTION)

WScript.Echo 
WScript.Echo sdoCollClients.Count & " Clients found."
For Each vtClient in sdoCollClients
    WScript.Echo "- " & Chr(34) & vtClient.GetProperty(PROPERTY_SDO_NAME) & Chr(34)
    WScript.Echo " - Require Signature " & Chr(34) & vtClient.GetProperty(PROPERTY_CLIENT_REQUIRE_SIGNATURE) & Chr(34)
    WScript.Echo " - Shared Secret " & Chr(34) & vtClient.GetProperty(PROPERTY_CLIENT_SHARED_SECRET) & Chr(34)
    WScript.Echo " - NAS Manufacturer" & Chr(34) & vtClient.GetProperty(PROPERTY_CLIENT_NAS_MANUFACTURER) & Chr(34)
    WScript.Echo " - Address" & Chr(34) & vtClient.GetProperty(PROPERTY_CLIENT_ADDRESS) & Chr(34)
Next 'vtClient
```



## <a name="related-topics"></a><span data-ttu-id="209df-105">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="209df-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="209df-106">**CLIENTPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="209df-106">**CLIENTPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-clientproperties)
</dt> <dt>

[<span data-ttu-id="209df-107">Enumerazione di oggetti in una raccolta</span><span class="sxs-lookup"><span data-stu-id="209df-107">Enumerating Objects in a Collection</span></span>](/windows/desktop/Nps/sdo-enumerating-objects-in-a-collection)
</dt> <dt>

[<span data-ttu-id="209df-108">**IASCOMMONPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="209df-108">**IASCOMMONPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties)
</dt> <dt>

[<span data-ttu-id="209df-109">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="209df-109">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> <dt>

[<span data-ttu-id="209df-110">**ISdo**</span><span class="sxs-lookup"><span data-stu-id="209df-110">**ISdo**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[<span data-ttu-id="209df-111">**ISdoMachine**</span><span class="sxs-lookup"><span data-stu-id="209df-111">**ISdoMachine**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdomachine)
</dt> <dt>

[<span data-ttu-id="209df-112">**RADIUSPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="209df-112">**RADIUSPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-radiusproperties)
</dt> </dl>

 

 