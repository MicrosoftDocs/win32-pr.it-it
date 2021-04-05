---
description: Indica se la connessione a una LAN wireless deve essere automatica o avviata dall'utente.
ms.assetid: 0fad8392-3053-494b-9b30-1db85408a437
title: Elemento connectionMode (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 3dafb9561bf8b5e3c5c66eb23bd5e286cbd38118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753754"
---
# <a name="connectionmode-wlanprofile-element"></a><span data-ttu-id="da1ed-103">Elemento connectionMode (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="da1ed-103">connectionMode (WLANProfile) Element</span></span>

<span data-ttu-id="da1ed-104">L'elemento connectionMode (WLANProfile) indica se la connessione a una LAN wireless deve essere automatica o avviata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="da1ed-104">The connectionMode (WLANProfile) element indicates whether connection to a wireless LAN should be automatic or initiated by user.</span></span>

<span data-ttu-id="da1ed-105">Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) è impostato su ESS, questo valore può essere automatico o manuale.</span><span class="sxs-lookup"><span data-stu-id="da1ed-105">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to ESS, this value can be either auto or manual.</span></span> <span data-ttu-id="da1ed-106">Se questo elemento è assente, il valore predefinito è auto.</span><span class="sxs-lookup"><span data-stu-id="da1ed-106">The default value is auto if this element is absent.</span></span>

<span data-ttu-id="da1ed-107">Se [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) è impostato su IBSS, questo valore deve essere manuale.</span><span class="sxs-lookup"><span data-stu-id="da1ed-107">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to IBSS, this value must be manual.</span></span>

``` syntax
<xs:element name="connectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="manual"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="da1ed-108">L'elemento **ConnectionMode** è definito dall'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="da1ed-108">The **connectionMode** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="da1ed-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="da1ed-109">Remarks</span></span>

<span data-ttu-id="da1ed-110">Nella tabella seguente vengono descritti i valori di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="da1ed-110">The following table describes the enumeration values.</span></span>



| <span data-ttu-id="da1ed-111">Valore</span><span class="sxs-lookup"><span data-stu-id="da1ed-111">Value</span></span>  | <span data-ttu-id="da1ed-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da1ed-112">Description</span></span>                                                                                                |
|--------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da1ed-113">auto</span><span class="sxs-lookup"><span data-stu-id="da1ed-113">auto</span></span>   | <span data-ttu-id="da1ed-114">La connessione alla rete wireless deve essere avviata automaticamente ogni volta che la rete è compresa nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="da1ed-114">The connection to the wireless network should be initiated automatically whenever the network is in range.</span></span> |
| <span data-ttu-id="da1ed-115">manual</span><span class="sxs-lookup"><span data-stu-id="da1ed-115">manual</span></span> | <span data-ttu-id="da1ed-116">La connessione alla rete wireless è avviate da solo sulla richiesta esplicita di un utente.</span><span class="sxs-lookup"><span data-stu-id="da1ed-116">The connection to the wireless network is only initated upon the explicit request of a user.</span></span>               |



 

## <a name="examples"></a><span data-ttu-id="da1ed-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="da1ed-117">Examples</span></span>

<span data-ttu-id="da1ed-118">Per visualizzare i profili di esempio che usano l'elemento **ConnectionMode** , vedere esempi di profili [wireless](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="da1ed-118">To view sample profiles that use the **connectionMode** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da1ed-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da1ed-119">Requirements</span></span>



| <span data-ttu-id="da1ed-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="da1ed-120">Requirement</span></span> | <span data-ttu-id="da1ed-121">Valore</span><span class="sxs-lookup"><span data-stu-id="da1ed-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="da1ed-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da1ed-122">Minimum supported client</span></span><br/> | <span data-ttu-id="da1ed-123">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="da1ed-123">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="da1ed-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da1ed-124">Minimum supported server</span></span><br/> | <span data-ttu-id="da1ed-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="da1ed-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="da1ed-126">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="da1ed-126">Redistributable</span></span><br/>          | <span data-ttu-id="da1ed-127">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="da1ed-127">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="da1ed-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da1ed-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="da1ed-129">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="da1ed-129">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="da1ed-130">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="da1ed-130">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="da1ed-131">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="da1ed-131">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="da1ed-132">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="da1ed-132">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




