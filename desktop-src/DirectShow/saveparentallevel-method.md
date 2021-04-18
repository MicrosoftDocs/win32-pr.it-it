---
description: Il metodo DVDAdm. SaveParentalLevel salva un nuovo livello padre predefinito nel registro di sistema.
ms.assetid: 8ad22098-acbd-41fd-9224-829b3cc5f8ae
title: Metodo SaveParentalLevel (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d30d26264dff077de391b6b513f7e9ab5048c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328606"
---
# <a name="saveparentallevel-method"></a><span data-ttu-id="7ee5c-103">Metodo SaveParentalLevel</span><span class="sxs-lookup"><span data-stu-id="7ee5c-103">SaveParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="7ee5c-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7ee5c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="7ee5c-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="7ee5c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="7ee5c-106">Il metodo **DVDAdm. SaveParentalLevel** salva un nuovo livello padre predefinito nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7ee5c-106">The **DVDAdm.SaveParentalLevel** method saves a new default parental level to the registry.</span></span>

``` syntax
DVD.DVDAdm.SaveParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="7ee5c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ee5c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ee5c-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span><span class="sxs-lookup"><span data-stu-id="7ee5c-108"><span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*</span></span>
</dt> <dd>

<span data-ttu-id="7ee5c-109">Specifica il livello padre come valore anInteger compreso tra 1 e 8.</span><span class="sxs-lookup"><span data-stu-id="7ee5c-109">Specifies the parental level as anInteger value from 1 through 8.</span></span>

</dd> <dt>

<span data-ttu-id="7ee5c-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="7ee5c-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="7ee5c-111">Specifica il nome utente sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="7ee5c-111">Specifies the user name as a String.</span></span> <span data-ttu-id="7ee5c-112">(Attualmente ignorata).</span><span class="sxs-lookup"><span data-stu-id="7ee5c-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="7ee5c-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="7ee5c-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="7ee5c-114">Specifica la password sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="7ee5c-114">Specifies the password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ee5c-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ee5c-115">Return Value</span></span>

<span data-ttu-id="7ee5c-116">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="7ee5c-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ee5c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ee5c-117">Remarks</span></span>

<span data-ttu-id="7ee5c-118">Questo metodo consente a un utente che conosce la password corrente di salvare una nuova impostazione del livello padre nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7ee5c-118">This method enables a user who knows the current password to save a new parental level setting to the registry.</span></span> <span data-ttu-id="7ee5c-119">Come per tutti i metodi di **MSDVDAdm**, questo metodo non influisce sul livello corrente del lettore. viene modificata solo l'impostazione del registro di sistema, in modo che la volta successiva in cui viene avviato l'oggetto MSWebDVD verrà aperto con il nuovo livello.</span><span class="sxs-lookup"><span data-stu-id="7ee5c-119">As with all the methods of **MSDVDAdm**, this method does not affect the current level in the player; it changes only the registry setting, so that the next time the MSWebDVD object is started, it will open with the new level.</span></span> <span data-ttu-id="7ee5c-120">Specificare-1 per disabilitare la gestione padre.</span><span class="sxs-lookup"><span data-stu-id="7ee5c-120">Specify -1 to disable parental management.</span></span> <span data-ttu-id="7ee5c-121">Per modificare il livello padre nel lettore, chiamare [**SelectParentalLevel**](selectparentallevel-method.md), che non modifica l'impostazione del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7ee5c-121">To change the parental level in the player, call [**SelectParentalLevel**](selectparentallevel-method.md), which does not change the registry setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ee5c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ee5c-122">Requirements</span></span>



| <span data-ttu-id="7ee5c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ee5c-123">Requirement</span></span> | <span data-ttu-id="7ee5c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7ee5c-124">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7ee5c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ee5c-125">Header</span></span><br/> | <dl> <span data-ttu-id="7ee5c-126"><dt>Segmento. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ee5c-126"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ee5c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ee5c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ee5c-128">Oggetto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="7ee5c-128">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




