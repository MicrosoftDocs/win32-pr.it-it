---
description: Definisce un profilo WLAN utilizzato dal servizio di configurazione automatica WiFi nativo.
ms.assetid: 8312d213-1d01-4bd0-a8d9-65ca23560888
title: Schema WLAN_profile
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d484215ca53ddcd97dbef4adf4aac17cd8457b3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128839"
---
# <a name="wlan_profile-schema"></a><span data-ttu-id="8b703-103">\_Schema profilo WLAN</span><span class="sxs-lookup"><span data-stu-id="8b703-103">WLAN\_profile Schema</span></span>

<span data-ttu-id="8b703-104">Lo \_ schema del profilo WLAN definisce un profilo WLAN utilizzato dal servizio di configurazione automatica WiFi nativo.</span><span class="sxs-lookup"><span data-stu-id="8b703-104">The WLAN\_profile Schema defines a WLAN profile used by the Native Wifi AutoConfig service.</span></span>

<span data-ttu-id="8b703-105">Il servizio di configurazione automatica accetta i profili wireless dall'agente di Criteri di gruppo, l'interfaccia di scripting (**netsh**), l'interfaccia utente o dall'interfaccia di configurazione flash USB.</span><span class="sxs-lookup"><span data-stu-id="8b703-105">The AutoConfig service accepts wireless profiles from the Group Policy Agent, the scripting interface (**netsh**), the user interface, or from the USB flash configuration interface.</span></span>

<span data-ttu-id="8b703-106">Un profilo ricevuto da uno di questi sistemi viene mappato allo \_ schema del profilo WLAN e archiviato nell'archivio profili.</span><span class="sxs-lookup"><span data-stu-id="8b703-106">A profile received from one of these systems is mapped to the WLAN\_profile schema and stored in the profile store.</span></span> <span data-ttu-id="8b703-107">I profili possono essere esportati dall'archivio profili usando i comandi netsh o usando elementi API, ad esempio [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).</span><span class="sxs-lookup"><span data-stu-id="8b703-107">Profiles can be exported from the profile store using netsh commands or using API elements such as [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile).</span></span>

<span data-ttu-id="8b703-108">L'elemento radice di un profilo WLAN è l'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8b703-108">The root element of a WLAN profile is the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span> <span data-ttu-id="8b703-109">Ogni profilo avrà esattamente un elemento radice.</span><span class="sxs-lookup"><span data-stu-id="8b703-109">Each profile will have exactly one root element.</span></span> <span data-ttu-id="8b703-110">L'elemento **WLANProfile** si trova nello spazio dei nomi `https://www.microsoft.com/networking/WLAN/profile/v1` .</span><span class="sxs-lookup"><span data-stu-id="8b703-110">The **WLANProfile** element is in the namespace `https://www.microsoft.com/networking/WLAN/profile/v1`.</span></span>

<span data-ttu-id="8b703-111">Per visualizzare i profili WLAN di esempio, vedere esempi di profili [wireless](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="8b703-111">To view sample WLAN profiles, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

-   [<span data-ttu-id="8b703-112">\_Elementi dello schema del profilo WLAN</span><span class="sxs-lookup"><span data-stu-id="8b703-112">WLAN\_profile Schema Elements</span></span>](wlan-profileschema-elements.md)
-   [<span data-ttu-id="8b703-113">\_Tipi semplici dello schema del profilo WLAN</span><span class="sxs-lookup"><span data-stu-id="8b703-113">WLAN\_profile Schema Simple Types</span></span>](wlan-profileschema-simple-types.md)

## <a name="related-topics"></a><span data-ttu-id="8b703-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8b703-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8b703-115">[Comandi Netsh per WLAN (wireless local area network)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="8b703-115">[Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10))</span></span>
</dt> </dl>

 

 
