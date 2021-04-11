---
description: Schema del profilo broadband mobile V2.
ms.assetid: 0E140DCC-373C-44B3-8A91-F38AE7A5797C
title: Schema del profilo broadband mobile V2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1328e2b108c80addc8f69584cd1b3cbd797ac777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129019"
---
# <a name="mobile-broadband-profile-schema-v2"></a><span data-ttu-id="8a718-103">Schema del profilo broadband mobile V2</span><span class="sxs-lookup"><span data-stu-id="8a718-103">Mobile Broadband Profile Schema v2</span></span>

<span data-ttu-id="8a718-104">Lo schema del profilo a banda larga 8Mobile di Windows V2 è disponibile nello spazio dei nomi `https://www.microsoft.com/networking/WWAN/profile/v2` .</span><span class="sxs-lookup"><span data-stu-id="8a718-104">The Windows 8Mobile Broadband Profile Schema v2 is available in the namespace `https://www.microsoft.com/networking/WWAN/profile/v2`.</span></span>

-   [<span data-ttu-id="8a718-105">Elementi del profilo Mobile Broadband schema V2</span><span class="sxs-lookup"><span data-stu-id="8a718-105">Mobile Broadband Profile Schema v2 Elements</span></span>](mobile-broadband-profile-schema-v2-elements.md)

``` syntax
<xs:schema targetNamespace="https://www.microsoft.com/networking/WWAN/profile/v2"
    xmlns="https://www.microsoft.com/networking/WWAN/profile/v2" 
    xmlns:xs="https://www.w3.org/2001/XMLSchema"
    xmlns:WWAN_profile_v1="https://www.microsoft.com/networking/WWAN/profile/v1" 
    elementFormDefault="qualified">

    <xs:import namespace="https://www.microsoft.com/networking/WWAN/profile/v1" schemaLocation="WWAN_profile_v1.xsd"/>

    <!-- Flag to indicate whether this is a purchase profile, default is "false" -->
    <xs:element name="IsPurchaseProfile" type="xs:boolean"/>

    <!-- Display Provider Name -->
    <xs:element name="DisplayProviderName" type="WWAN_profile_v1:providerNameType"/>

</xs:schema>
```

 

 



