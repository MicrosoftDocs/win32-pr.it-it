---
description: Definisce gli elementi di configurazione 802.1 X.
ms.assetid: 4755356e-cb4b-4eed-a494-ca0d17f5184f
title: Schema OneX
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9df45ed7981c055e955afe72333a42db99ddb21a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227392"
---
# <a name="onex-schema"></a><span data-ttu-id="09c29-103">Schema OneX</span><span class="sxs-lookup"><span data-stu-id="09c29-103">OneX Schema</span></span>

<span data-ttu-id="09c29-104">Lo schema OneX definisce gli elementi di configurazione 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="09c29-104">The OneX Schema defines 802.1X configuration elements.</span></span> <span data-ttu-id="09c29-105">Tutti gli elementi dello schema OneX si applicano ai profili cablati e wireless.</span><span class="sxs-lookup"><span data-stu-id="09c29-105">All OneX schema elements apply to both wired and wireless profiles.</span></span> <span data-ttu-id="09c29-106">Per un elenco di elementi definiti, vedere [elementi dello schema Onex](onexschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="09c29-106">For a list of defined elements, see [OneX Schema Elements](onexschema-elements.md).</span></span>

<span data-ttu-id="09c29-107">L'elemento radice di un profilo 802.1 X è l'elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="09c29-107">The root element of an 802.1X profile is the [**OneX**](onexschema-onex-element.md) element.</span></span> <span data-ttu-id="09c29-108">Ogni profilo avrà esattamente un elemento radice.</span><span class="sxs-lookup"><span data-stu-id="09c29-108">Each profile will have exactly one root element.</span></span> <span data-ttu-id="09c29-109">L'elemento **Onex** si trova nello `https://www.microsoft.com/networking/OneX/v1` spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="09c29-109">The **OneX** element is in the `https://www.microsoft.com/networking/OneX/v1` namespace.</span></span>

<span data-ttu-id="09c29-110">Per visualizzare i profili di esempio per reti wireless che includono elementi di configurazione 802.1 X, vedere gli esempi di profilo seguenti:</span><span class="sxs-lookup"><span data-stu-id="09c29-110">To view sample profiles for wireless networks that include 802.1X configuration elements, see the following profile samples:</span></span>

-   [<span data-ttu-id="09c29-111">Esempio di profilo bootstrap</span><span class="sxs-lookup"><span data-stu-id="09c29-111">Bootstrap Profile Sample</span></span>](bootstrap-profile-sample.md)
-   [<span data-ttu-id="09c29-112">Esempio di profilo FIPS</span><span class="sxs-lookup"><span data-stu-id="09c29-112">FIPS Profile Sample</span></span>](fips-profile-sample.md)
-   [<span data-ttu-id="09c29-113">Esempio di profilo Single Sign-On</span><span class="sxs-lookup"><span data-stu-id="09c29-113">Single Sign-On Profile Sample</span></span>](single-sign-on-profile-sample.md)
-   [<span data-ttu-id="09c29-114">Esempio di profilo WPA-Enterprise con PEAP-MSCHAPv2</span><span class="sxs-lookup"><span data-stu-id="09c29-114">WPA-Enterprise with PEAP-MSCHAPv2 Profile Sample</span></span>](wpa-enterprise-with-peap-mschapv2-profile-sample.md)
-   [<span data-ttu-id="09c29-115">Esempio di profilo WPA-Enterprise con TLS</span><span class="sxs-lookup"><span data-stu-id="09c29-115">WPA-Enterprise with TLS Profile Sample</span></span>](wpa-enterprise-with-tls-profile-sample.md)
-   [<span data-ttu-id="09c29-116">Esempio di profilo WPA2-Enterprise con PEAP-MSCHAPv2</span><span class="sxs-lookup"><span data-stu-id="09c29-116">WPA2-Enterprise with PEAP-MSCHAPv2 Profile Sample</span></span>](wpa2-enterprise-with-peap-mschapv2-profile-sample.md)
-   [<span data-ttu-id="09c29-117">Esempio di profilo WPA2-Enterprise con TLS</span><span class="sxs-lookup"><span data-stu-id="09c29-117">WPA2-Enterprise with TLS Profile Sample</span></span>](wpa2-enterprise-with-tls-profile-sample.md)

<span data-ttu-id="09c29-118">Per visualizzare i profili di esempio per reti cablate che includono elementi di configurazione 802.1 X, vedere gli esempi di profilo seguenti:</span><span class="sxs-lookup"><span data-stu-id="09c29-118">To view sample profiles for wired networks that include 802.1X configuration elements, see the following profile samples:</span></span>

-   [<span data-ttu-id="09c29-119">Esempio di profilo certificato del computer</span><span class="sxs-lookup"><span data-stu-id="09c29-119">Machine Certificate Profile Sample</span></span>](machine-certificate-profile-sample.md)
-   [<span data-ttu-id="09c29-120">Esempio di profilo PEAP</span><span class="sxs-lookup"><span data-stu-id="09c29-120">PEAP Profile Sample</span></span>](peap-profile-sample.md)
-   [<span data-ttu-id="09c29-121">Profilo di esempio certificato smart card</span><span class="sxs-lookup"><span data-stu-id="09c29-121">Smart Card Certificate Sample Profile</span></span>](smart-card-certificate-profile-sample.md)

 

 



