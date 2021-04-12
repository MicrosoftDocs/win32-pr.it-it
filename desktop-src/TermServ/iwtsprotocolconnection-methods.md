---
title: Metodi IWTSProtocolConnection
description: L'interfaccia IWTSProtocolConnection espone i metodi seguenti.
ms.assetid: DBB96D6B-F5A5-4CAF-974F-44D76B9CBFB6
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb89f63aea6b1904eb4319dcce541aeb4d15d34f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396963"
---
# <a name="iwtsprotocolconnection-methods"></a><span data-ttu-id="1371a-103">Metodi IWTSProtocolConnection</span><span class="sxs-lookup"><span data-stu-id="1371a-103">IWTSProtocolConnection Methods</span></span>

<span data-ttu-id="1371a-104">\[IWTSProtocolConnection non è più disponibile per l'uso a partire da Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="1371a-104">\[IWTSProtocolConnection is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="1371a-105">L'interfaccia [**IWTSProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection) espone i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="1371a-105">The [**IWTSProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwtsprotocolconnection) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1371a-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="1371a-106">In this section</span></span>

-   [<span data-ttu-id="1371a-107">**Metodo AcceptConnection**</span><span class="sxs-lookup"><span data-stu-id="1371a-107">**AcceptConnection method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-acceptconnection)
-   [<span data-ttu-id="1371a-108">**Metodo AuthenticateClientToSession**</span><span class="sxs-lookup"><span data-stu-id="1371a-108">**AuthenticateClientToSession method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-authenticateclienttosession)
-   [<span data-ttu-id="1371a-109">**Metodo Close**</span><span class="sxs-lookup"><span data-stu-id="1371a-109">**Close method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-close)
-   [<span data-ttu-id="1371a-110">**Metodo ConnectNotify**</span><span class="sxs-lookup"><span data-stu-id="1371a-110">**ConnectNotify method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-connectnotify)
-   [<span data-ttu-id="1371a-111">**Metodo CreateVirtualChannel**</span><span class="sxs-lookup"><span data-stu-id="1371a-111">**CreateVirtualChannel method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-createvirtualchannel)
-   [<span data-ttu-id="1371a-112">**Metodo DisconnectNotify**</span><span class="sxs-lookup"><span data-stu-id="1371a-112">**DisconnectNotify method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-disconnectnotify)
-   [<span data-ttu-id="1371a-113">**Metodo GetClientData**</span><span class="sxs-lookup"><span data-stu-id="1371a-113">**GetClientData method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getclientdata)
-   [<span data-ttu-id="1371a-114">**Metodo GetLastInputTime**</span><span class="sxs-lookup"><span data-stu-id="1371a-114">**GetLastInputTime method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlastinputtime)
-   [<span data-ttu-id="1371a-115">**Metodo GetLicenseConnection**</span><span class="sxs-lookup"><span data-stu-id="1371a-115">**GetLicenseConnection method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlicenseconnection)
-   [<span data-ttu-id="1371a-116">**Metodo GetLogonErrorRedirector**</span><span class="sxs-lookup"><span data-stu-id="1371a-116">**GetLogonErrorRedirector method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getlogonerrorredirector)
-   [<span data-ttu-id="1371a-117">**Metodo GetProtocolHandles**</span><span class="sxs-lookup"><span data-stu-id="1371a-117">**GetProtocolHandles method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getprotocolhandles)
-   [<span data-ttu-id="1371a-118">**Metodo GetProtocolStatus**</span><span class="sxs-lookup"><span data-stu-id="1371a-118">**GetProtocolStatus method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getprotocolstatus)
-   [<span data-ttu-id="1371a-119">**Metodo GetShadowConnection**</span><span class="sxs-lookup"><span data-stu-id="1371a-119">**GetShadowConnection method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getshadowconnection)
-   [<span data-ttu-id="1371a-120">**Metodo GetUserCredentials**</span><span class="sxs-lookup"><span data-stu-id="1371a-120">**GetUserCredentials method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getusercredentials)
-   [<span data-ttu-id="1371a-121">**Metodo GetUserData**</span><span class="sxs-lookup"><span data-stu-id="1371a-121">**GetUserData method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-getuserdata)
-   [<span data-ttu-id="1371a-122">**Metodo IsUserAllowedToLogon**</span><span class="sxs-lookup"><span data-stu-id="1371a-122">**IsUserAllowedToLogon method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-isuserallowedtologon)
-   [<span data-ttu-id="1371a-123">**Metodo LogonNotify**</span><span class="sxs-lookup"><span data-stu-id="1371a-123">**LogonNotify method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-logonnotify)
-   [<span data-ttu-id="1371a-124">**Metodo NotifySessionId**</span><span class="sxs-lookup"><span data-stu-id="1371a-124">**NotifySessionId method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-notifysessionid)
-   [<span data-ttu-id="1371a-125">**Metodo QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="1371a-125">**QueryProperty method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-queryproperty)
-   [<span data-ttu-id="1371a-126">**Metodo SendBeep**</span><span class="sxs-lookup"><span data-stu-id="1371a-126">**SendBeep method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sendbeep)
-   [<span data-ttu-id="1371a-127">**Metodo SendPolicyData**</span><span class="sxs-lookup"><span data-stu-id="1371a-127">**SendPolicyData method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sendpolicydata)
-   [<span data-ttu-id="1371a-128">**Metodo SessionArbitrationEnumeration**</span><span class="sxs-lookup"><span data-stu-id="1371a-128">**SessionArbitrationEnumeration method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-sessionarbitrationenumeration)
-   [<span data-ttu-id="1371a-129">**SetErrorInfo (metodo)**</span><span class="sxs-lookup"><span data-stu-id="1371a-129">**SetErrorInfo method**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwtsprotocolconnection-seterrorinfo)

 

 




