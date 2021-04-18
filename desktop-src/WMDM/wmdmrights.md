---
title: Struttura WMDMRIGHTS
description: La struttura WMDMRIGHTS descrive i diritti di utilizzo del contenuto.
ms.assetid: 1be9167b-0d20-4a17-a42b-9696ada2b539
keywords:
- Struttura WMDMRIGHTS Windows Media Gestione dispositivi
- Puntatore alla struttura PWMDMRIGHTS Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- WMDMRIGHTS
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8bc3bcd61efc64d32daa3179b77a9aaa518d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325004"
---
# <a name="wmdmrights-structure"></a><span data-ttu-id="fa537-105">Struttura WMDMRIGHTS</span><span class="sxs-lookup"><span data-stu-id="fa537-105">WMDMRIGHTS structure</span></span>

<span data-ttu-id="fa537-106">La struttura **WMDMRIGHTS** descrive i diritti di utilizzo del contenuto.</span><span class="sxs-lookup"><span data-stu-id="fa537-106">The **WMDMRIGHTS** structure describes content-use rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa537-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa537-107">Syntax</span></span>


```C++
typedef struct __WMDMRIGHTS {
  UINT         cbSize;
  DWORD        dwContentType;
  DWORD        fuFlags;
  DWORD        fuRights;
  DWORD        dwAppSec;
  DWORD        dwPlaybackCount;
  WMDMDATETIME ExpirationDate;
} WMDMRIGHTS, *PWMDMRIGHTS;
```



## <a name="members"></a><span data-ttu-id="fa537-108">Members</span><span class="sxs-lookup"><span data-stu-id="fa537-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="fa537-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="fa537-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="fa537-110">Dimensioni, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="fa537-110">Size of the structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="fa537-111">**dwContentType**</span><span class="sxs-lookup"><span data-stu-id="fa537-111">**dwContentType**</span></span>
</dt> <dd>

<span data-ttu-id="fa537-112">**DWORD** che contiene il tipo di contenuto.</span><span class="sxs-lookup"><span data-stu-id="fa537-112">**DWORD** containing the type of content.</span></span>

</dd> <dt>

<span data-ttu-id="fa537-113">**fuFlags**</span><span class="sxs-lookup"><span data-stu-id="fa537-113">**fuFlags**</span></span>
</dt> <dd>

<span data-ttu-id="fa537-114">Campo di bit che specifica le opzioni dei diritti in uso per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="fa537-114">Bit field specifying the rights options in use for the content.</span></span>



| <span data-ttu-id="fa537-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fa537-115">Value</span></span>                        | <span data-ttu-id="fa537-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa537-116">Description</span></span>                                  |
|------------------------------|----------------------------------------------|
| <span data-ttu-id="fa537-117">\_diritti WMDM \_ PLAYBACKCOUNT</span><span class="sxs-lookup"><span data-stu-id="fa537-117">WMDM\_RIGHTS\_PLAYBACKCOUNT</span></span>  | <span data-ttu-id="fa537-118">Numero di volte in cui il file può essere riprodotto.</span><span class="sxs-lookup"><span data-stu-id="fa537-118">Number of times that the file can be played.</span></span> |
| <span data-ttu-id="fa537-119">\_diritti WMDM \_ EXPIRATIONDATE</span><span class="sxs-lookup"><span data-stu-id="fa537-119">WMDM\_RIGHTS\_EXPIRATIONDATE</span></span> | <span data-ttu-id="fa537-120">Data di scadenza del file.</span><span class="sxs-lookup"><span data-stu-id="fa537-120">Expiration date of the file.</span></span>                 |
| <span data-ttu-id="fa537-121">\_diritti WMDM \_ FREESERIALIDS</span><span class="sxs-lookup"><span data-stu-id="fa537-121">WMDM\_RIGHTS\_FREESERIALIDS</span></span>  | <span data-ttu-id="fa537-122">Identificatore seriale gratuito del file.</span><span class="sxs-lookup"><span data-stu-id="fa537-122">Free serial identifier of the file.</span></span>          |
| <span data-ttu-id="fa537-123">\_Gruppo GROUPID Rights WMDM \_</span><span class="sxs-lookup"><span data-stu-id="fa537-123">WMDM\_RIGHTS\_GROUPID Group</span></span>  | <span data-ttu-id="fa537-124">Identificatore del file.</span><span class="sxs-lookup"><span data-stu-id="fa537-124">Identifier of the file.</span></span>                      |
| <span data-ttu-id="fa537-125">\_diritti WMDM \_ NAMEDSERIALIDS</span><span class="sxs-lookup"><span data-stu-id="fa537-125">WMDM\_RIGHTS\_NAMEDSERIALIDS</span></span> | <span data-ttu-id="fa537-126">Identificatore seriale denominato del file.</span><span class="sxs-lookup"><span data-stu-id="fa537-126">Named serial identifier of the file.</span></span>         |



 

</dd> <dt>

<span data-ttu-id="fa537-127">**fuRights**</span><span class="sxs-lookup"><span data-stu-id="fa537-127">**fuRights**</span></span>
</dt> <dd>

<span data-ttu-id="fa537-128">Campo di bit contenente i bit dei diritti per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="fa537-128">Bit field containing the rights bits for the content.</span></span>



| <span data-ttu-id="fa537-129">Valore</span><span class="sxs-lookup"><span data-stu-id="fa537-129">Value</span></span>                                     | <span data-ttu-id="fa537-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa537-130">Description</span></span>                                   |
|-------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="fa537-131">WMDM \_ Rights \_ Play \_ sul \_ PC</span><span class="sxs-lookup"><span data-stu-id="fa537-131">WMDM\_RIGHTS\_PLAY\_ON\_PC</span></span>                | <span data-ttu-id="fa537-132">Il contenuto può essere riprodotto in un personal computer.</span><span class="sxs-lookup"><span data-stu-id="fa537-132">Content can be played on a personal computer.</span></span> |
| <span data-ttu-id="fa537-133">\_Copia diritti \_ WMDM \_ nel \_ \_ dispositivo non SDMI \_</span><span class="sxs-lookup"><span data-stu-id="fa537-133">WMDM\_RIGHTS\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="fa537-134">Il contenuto può essere copiato in un dispositivo non SDMI.</span><span class="sxs-lookup"><span data-stu-id="fa537-134">Content can be copied to a non-SDMI device.</span></span>   |
| <span data-ttu-id="fa537-135">\_Copia diritti \_ WMDM \_ su \_ CD</span><span class="sxs-lookup"><span data-stu-id="fa537-135">WMDM\_RIGHTS\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="fa537-136">Il contenuto può essere copiato in un CD.</span><span class="sxs-lookup"><span data-stu-id="fa537-136">Content can be copied to a CD.</span></span>                |
| <span data-ttu-id="fa537-137">\_Copia diritti \_ WMDM \_ nel \_ \_ dispositivo SDMI</span><span class="sxs-lookup"><span data-stu-id="fa537-137">WMDM\_RIGHTS\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="fa537-138">Il contenuto può essere copiato in un dispositivo SDMI.</span><span class="sxs-lookup"><span data-stu-id="fa537-138">Content can be copied to an SDMI device.</span></span>      |



 

</dd> <dt>

<span data-ttu-id="fa537-139">**dwAppSec**</span><span class="sxs-lookup"><span data-stu-id="fa537-139">**dwAppSec**</span></span>
</dt> <dd>

<span data-ttu-id="fa537-140">Matrice di byte che specifica il livello minimo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fa537-140">Byte array that specifies the minimum level of application security.</span></span>

</dd> <dt>

<span data-ttu-id="fa537-141">**dwPlaybackCount**</span><span class="sxs-lookup"><span data-stu-id="fa537-141">**dwPlaybackCount**</span></span>
</dt> <dd>

<span data-ttu-id="fa537-142">**DWORD** contenente il numero di volte rimanenti di cui è possibile eseguire il rendering del contenuto.</span><span class="sxs-lookup"><span data-stu-id="fa537-142">**DWORD** containing the number of remaining times that the content can be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="fa537-143">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="fa537-143">**ExpirationDate**</span></span>
</dt> <dd>

<span data-ttu-id="fa537-144">Struttura [**WMDMDATETIME**](wmdmdatetime.md) contenente la data e l'ora di scadenza per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="fa537-144">[**WMDMDATETIME**](wmdmdatetime.md) structure containing the expiration date and time for the content.</span></span> <span data-ttu-id="fa537-145">Se la licenza non ha una data di scadenza, il membro **wYear** è impostato su 0xffff e tutti gli altri membri di **WMDMDATETIME** vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="fa537-145">If the license has no expiration date, the **wYear** member is set to 0xFFFF, and all other members of **WMDMDATETIME** are ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa537-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa537-146">Requirements</span></span>



| <span data-ttu-id="fa537-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa537-147">Requirement</span></span> | <span data-ttu-id="fa537-148">Valore</span><span class="sxs-lookup"><span data-stu-id="fa537-148">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fa537-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa537-149">Header</span></span><br/> | <dl> <span data-ttu-id="fa537-150"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fa537-150"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa537-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa537-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa537-152">**IMDSPStorage:: getrights**</span><span class="sxs-lookup"><span data-stu-id="fa537-152">**IMDSPStorage::GetRights**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getrights)
</dt> <dt>

[<span data-ttu-id="fa537-153">**IWMDMStorage:: getrights**</span><span class="sxs-lookup"><span data-stu-id="fa537-153">**IWMDMStorage::GetRights**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights)
</dt> <dt>

[<span data-ttu-id="fa537-154">**WMDMDATETIME**</span><span class="sxs-lookup"><span data-stu-id="fa537-154">**WMDMDATETIME**</span></span>](wmdmdatetime.md)
</dt> <dt>

[<span data-ttu-id="fa537-155">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="fa537-155">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





