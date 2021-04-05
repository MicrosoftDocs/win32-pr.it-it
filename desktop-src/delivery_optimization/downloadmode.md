---
title: Enumerazione modalità (Deliveryoptimization. h)
description: Definisce le diverse modalità di download utilizzate dall'ottimizzazione per il recapito.
ms.assetid: 7E9407C6-A22F-459E-B316-5E7809F0067A
keywords:
- In questa modalità Ottimizzazione recapito viene ignorato e al suo posto viene usato BITS. Seleziona ad esempio questa modalità per consentire ai client di usare BranchCache. enumerazione
topic_type:
- apiref
api_name:
- DownloadMode
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0cde44a3d211040e2cc1dd62afd54f8284f5493e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048282"
---
# <a name="downloadmode-enumeration"></a><span data-ttu-id="f6ab2-106">Enumerazione modalità</span><span class="sxs-lookup"><span data-stu-id="f6ab2-106">DownloadMode enumeration</span></span>

<span data-ttu-id="f6ab2-107">Definisce le diverse modalità di download utilizzate dall'ottimizzazione per il recapito.</span><span class="sxs-lookup"><span data-stu-id="f6ab2-107">Defines the different download modes that Delivery Optimization uses.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6ab2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6ab2-108">Syntax</span></span>


```C++
typedef enum _DownloadMode { 
  DownloadMode_CdnOnly   = 0,
  DownloadMode_Lan       = 1,
  DownloadMode_Group     = 2,
  DownloadMode_Internet  = 3,
  DownloadMode_Simple    = 99,
  DownloadMode_Bypass    = 100
} DownloadMode;
```



## <a name="constants"></a><span data-ttu-id="f6ab2-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="f6ab2-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f6ab2-110"><span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**</span><span class="sxs-lookup"><span data-stu-id="f6ab2-110"><span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**</span></span>
</dt> <dd>

<span data-ttu-id="f6ab2-111">Questa impostazione Disabilita la memorizzazione nella cache peer-to-peer, ma consente comunque all'ottimizzazione del recapito di scaricare il contenuto dai server Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f6ab2-111">This setting disables peer-to-peer caching but still allows Delivery Optimization to download content from Microsoft servers.</span></span> <span data-ttu-id="f6ab2-112">Questa modalità usa i metadati aggiuntivi forniti dai servizi cloud di ottimizzazione recapito per un'esperienza di download affidabile ed efficiente senza peer.</span><span class="sxs-lookup"><span data-stu-id="f6ab2-112">This mode uses additional metadata provided by the Delivery Optimization cloud services for a peerless reliable and efficient download experience.</span></span>

</dd> <dt>

<span data-ttu-id="f6ab2-113"><span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**</span><span class="sxs-lookup"><span data-stu-id="f6ab2-113"><span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**</span></span>
</dt> <dd>

<span data-ttu-id="f6ab2-114">Questa modalità operativa predefinita per Ottimizzazione recapito consente la condivisione peer sulla stessa rete.</span><span class="sxs-lookup"><span data-stu-id="f6ab2-114">This default operating mode for Delivery Optimization enables peer sharing on the same network.</span></span>

</dd> <dt>

<span data-ttu-id="f6ab2-115"><span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**</span><span class="sxs-lookup"><span data-stu-id="f6ab2-115"><span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**</span></span>
</dt> <dd>

<span data-ttu-id="f6ab2-116">Quando viene impostata la modalità gruppo, il gruppo viene selezionato automaticamente in base al sito Active Directory Domain Services (AD DS) del dispositivo (Windows 10, versione 1607) o al dominio al quale è autenticato il dispositivo (Windows 10, versione 1511).</span><span class="sxs-lookup"><span data-stu-id="f6ab2-116">When group mode is set, the group is automatically selected based on the device s Active Directory Domain Services (AD DS) site (Windows 10, version 1607) or the domain the device is authenticated to (Windows 10, version 1511).</span></span> <span data-ttu-id="f6ab2-117">In modalità di gruppo, il peering avviene tra le subnet interne, tra i dispositivi che appartengono allo stesso gruppo, inclusi i dispositivi nelle sedi remote.</span><span class="sxs-lookup"><span data-stu-id="f6ab2-117">In group mode, peering occurs across internal subnets, between devices that belong to the same group, including devices in remote offices.</span></span> <span data-ttu-id="f6ab2-118">Puoi usare l'opzione GroupID per creare un gruppo personalizzato indipendentemente dai domini e dai siti di Servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f6ab2-118">You can use the GroupID option to create your own custom group independently of domains and AD DS sites.</span></span> <span data-ttu-id="f6ab2-119">La modalità di download di gruppo è l'opzione consigliata per la maggior parte delle organizzazioni che vuole ottenere la massima ottimizzazione della larghezza di banda con Ottimizzazione recapito.</span><span class="sxs-lookup"><span data-stu-id="f6ab2-119">Group download mode is the recommended option for most organizations looking to achieve the best bandwidth optimization with Delivery Optimization.</span></span>

</dd> <dt>

<span data-ttu-id="f6ab2-120"><span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**</span><span class="sxs-lookup"><span data-stu-id="f6ab2-120"><span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**</span></span>
</dt> <dd>

<span data-ttu-id="f6ab2-121">Questa modalità abilita le origini peer Internet per Ottimizzazione recapito.</span><span class="sxs-lookup"><span data-stu-id="f6ab2-121">Enable Internet peer sources for Delivery Optimization.</span></span>

</dd> <dt>

<span data-ttu-id="f6ab2-122"><span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**</span><span class="sxs-lookup"><span data-stu-id="f6ab2-122"><span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**</span></span>
</dt> <dd>

<span data-ttu-id="f6ab2-123">La modalità semplice disabilita completamente l'uso dei servizi cloud di Ottimizzazione recapito (per gli ambienti offline).</span><span class="sxs-lookup"><span data-stu-id="f6ab2-123">Simple mode disables the use of Delivery Optimization cloud services completely (for offline environments).</span></span> <span data-ttu-id="f6ab2-124">L'ottimizzazione recapito passa automaticamente a questa modalità quando i servizi cloud di ottimizzazione recapito non sono disponibili, non raggiungibili o quando le dimensioni del file di contenuto sono inferiori a 10 MB.</span><span class="sxs-lookup"><span data-stu-id="f6ab2-124">Delivery Optimization switches to this mode automatically when the Delivery Optimization cloud services are unavailable, unreachable or when the content file size is less than 10 MB.</span></span> <span data-ttu-id="f6ab2-125">In questa modalità, l'ottimizzazione del recapito fornisce un'esperienza di download affidabile, senza memorizzazione nella cache peer-to-peer.</span><span class="sxs-lookup"><span data-stu-id="f6ab2-125">In this mode, Delivery Optimization provides a reliable download experience, with no peer-to-peer caching.</span></span>

</dd> <dt>

<span data-ttu-id="f6ab2-126"><span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**</span><span class="sxs-lookup"><span data-stu-id="f6ab2-126"><span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**</span></span>
</dt> <dd>

<span data-ttu-id="f6ab2-127">In questa modalità Ottimizzazione recapito viene ignorato e al suo posto viene usato BITS.</span><span class="sxs-lookup"><span data-stu-id="f6ab2-127">Bypass Delivery Optimization and use BITS, instead.</span></span> <span data-ttu-id="f6ab2-128">Seleziona ad esempio questa modalità per consentire ai client di usare BranchCache.</span><span class="sxs-lookup"><span data-stu-id="f6ab2-128">For example, select this mode so that clients can use BranchCache.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6ab2-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6ab2-129">Requirements</span></span>

| <span data-ttu-id="f6ab2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6ab2-130">Requirement</span></span> | <span data-ttu-id="f6ab2-131">Valore</span><span class="sxs-lookup"><span data-stu-id="f6ab2-131">Value</span></span> |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="f6ab2-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6ab2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f6ab2-133">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6ab2-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="f6ab2-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6ab2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f6ab2-135">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f6ab2-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>  |
| <span data-ttu-id="f6ab2-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6ab2-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6ab2-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6ab2-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>               |
