---
title: Struttura CB_CONNECTION_INFO (Cbclient. h)
description: Contiene informazioni su una richiesta di connessione in ingresso.
ms.assetid: BA908425-3B68-40AA-B1E3-153D6873EF2C
ms.tgt_platform: multiple
keywords:
- Struttura CB_CONNECTION_INFO Servizi Desktop remoto
- Puntatore alla struttura PCB_CONNECTION_INFO Servizi Desktop remoto
topic_type:
- apiref
api_name:
- CB_CONNECTION_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36370a4faa823f509d1f3356768add0ece9a6904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400401"
---
# <a name="cb_connection_info-structure"></a><span data-ttu-id="acc21-105">Struttura delle informazioni di \_ connessione CB \_</span><span class="sxs-lookup"><span data-stu-id="acc21-105">CB\_CONNECTION\_INFO structure</span></span>

<span data-ttu-id="acc21-106">Contiene informazioni su una richiesta di connessione in ingresso.</span><span class="sxs-lookup"><span data-stu-id="acc21-106">Contains information about an incoming connection request.</span></span> <span data-ttu-id="acc21-107">Questa struttura viene utilizzata con il metodo [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="acc21-107">This structure is used with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="acc21-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="acc21-108">Syntax</span></span>


```C++
typedef struct {
  WCHAR            UserName[CB_USERNAME_LENGTH];
  WCHAR            Domain[CB_DOMAINNAME_LENGTH];
  WCHAR            InitialProgram[CB_INITAPP_LENGTH];
  CB_RESOURCE_TYPE Resource;
  WCHAR            PluginName[CB_PLUGINNAME_LENGTH];
  WCHAR            FarmName[CB_FARMNAME_LENGTH];
  DWORD            dwVendorInfoLength;
  PBYTE            pVendorSpecificInfo;
} CB_CONNECTION_INFO, *PCB_CONNECTION_INFO;
```



## <a name="members"></a><span data-ttu-id="acc21-109">Members</span><span class="sxs-lookup"><span data-stu-id="acc21-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="acc21-110">**UserName**</span><span class="sxs-lookup"><span data-stu-id="acc21-110">**UserName**</span></span>
</dt> <dd>

<span data-ttu-id="acc21-111">Nome dell'utente che richiede una sessione.</span><span class="sxs-lookup"><span data-stu-id="acc21-111">The name of the user requesting a session.</span></span>

</dd> <dt>

<span data-ttu-id="acc21-112">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="acc21-112">**Domain**</span></span>
</dt> <dd>

<span data-ttu-id="acc21-113">Nome del dominio di cui è membro il nome **utente** .</span><span class="sxs-lookup"><span data-stu-id="acc21-113">The name of the domain that **UserName** is a member of.</span></span>

</dd> <dt>

<span data-ttu-id="acc21-114">**InitialProgram**</span><span class="sxs-lookup"><span data-stu-id="acc21-114">**InitialProgram**</span></span>
</dt> <dd>

<span data-ttu-id="acc21-115">Percorso completo e nome file del programma iniziale avviato all'avvio della sessione.</span><span class="sxs-lookup"><span data-stu-id="acc21-115">The fully qualified path and file name of the initial program that is started when the session is started.</span></span> <span data-ttu-id="acc21-116">Impostare questo membro su una stringa vuota se non è necessario avviare alcun programma iniziale.</span><span class="sxs-lookup"><span data-stu-id="acc21-116">Set this member to an empty string if no initial program should be started.</span></span>

</dd> <dt>

<span data-ttu-id="acc21-117">**Risorsa**</span><span class="sxs-lookup"><span data-stu-id="acc21-117">**Resource**</span></span>
</dt> <dd>

<span data-ttu-id="acc21-118">Valore dell'enumerazione del [**\_ \_ tipo di risorsa CB**](cb-resource-type.md) che specifica il tipo di risorsa a cui si connette la connessione in ingresso.</span><span class="sxs-lookup"><span data-stu-id="acc21-118">A value of the [**CB\_RESOURCE\_TYPE**](cb-resource-type.md) enumeration that specifies the type of resource that the incoming connection is connecting to.</span></span> <span data-ttu-id="acc21-119">Se il membro **pluginName** è **null**, questo membro viene usato da connessione Desktop remoto broker per determinare il plug-in da richiamare per determinare il computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="acc21-119">If the **PluginName** member is **NULL**, this member is used to by the Remote Desktop Connection Broker to determine which plug-in to invoke for determining the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="acc21-120">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="acc21-120">**PluginName**</span></span>
</dt> <dd>

<span data-ttu-id="acc21-121">Nome del plug-in da richiamare per determinare il computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="acc21-121">The name of the plug-in to invoke to determine the target computer.</span></span> <span data-ttu-id="acc21-122">Se questo parametro è **null**, viene usato il membro della **risorsa** per determinare il plug-in da richiamare.</span><span class="sxs-lookup"><span data-stu-id="acc21-122">If this parameter is **NULL**, the **Resource** member is used to determine which plug-in to invoke.</span></span>

</dd> <dt>

<span data-ttu-id="acc21-123">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="acc21-123">**FarmName**</span></span>
</dt> <dd>

<span data-ttu-id="acc21-124">Nome della farm che contiene i computer, uno dei quali sarà il computer di destinazione in cui verrà reindirizzata la connessione.</span><span class="sxs-lookup"><span data-stu-id="acc21-124">The name of the farm that contains the computers, one of which will be the target computer where the connection will be redirected.</span></span>

</dd> <dt>

<span data-ttu-id="acc21-125">**dwVendorInfoLength**</span><span class="sxs-lookup"><span data-stu-id="acc21-125">**dwVendorInfoLength**</span></span>
</dt> <dd>

<span data-ttu-id="acc21-126">Questo membro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="acc21-126">This member is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="acc21-127">**pVendorSpecificInfo**</span><span class="sxs-lookup"><span data-stu-id="acc21-127">**pVendorSpecificInfo**</span></span>
</dt> <dd>

<span data-ttu-id="acc21-128">Questo membro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="acc21-128">This member is reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="acc21-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="acc21-129">Requirements</span></span>



| <span data-ttu-id="acc21-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="acc21-130">Requirement</span></span> | <span data-ttu-id="acc21-131">Valore</span><span class="sxs-lookup"><span data-stu-id="acc21-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="acc21-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acc21-132">Minimum supported client</span></span><br/> | <span data-ttu-id="acc21-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="acc21-133">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="acc21-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acc21-134">Minimum supported server</span></span><br/> | <span data-ttu-id="acc21-135">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="acc21-135">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="acc21-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="acc21-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="acc21-137"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="acc21-137"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acc21-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="acc21-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acc21-139">**IConnectionBrokerClient::GetTargetInfo**</span><span class="sxs-lookup"><span data-stu-id="acc21-139">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





