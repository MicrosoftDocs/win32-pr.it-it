---
description: Il metodo DVDAdm. SaveParentalCountry Salva il nuovo paese/area padre dell'applicazione nel registro di sistema.
ms.assetid: 2185ad7d-c7c1-4d8b-82e7-5ed5fffaff26
title: Metodo SaveParentalCountry (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9ca47a6ca10f25298b4eb10fdcf532c8d764b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328609"
---
# <a name="saveparentalcountry-method"></a><span data-ttu-id="de5b0-103">Metodo SaveParentalCountry</span><span class="sxs-lookup"><span data-stu-id="de5b0-103">SaveParentalCountry Method</span></span>

> [!Note]  
> <span data-ttu-id="de5b0-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="de5b0-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="de5b0-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="de5b0-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="de5b0-106">Il `DVDAdm.SaveParentalCountry` metodo salva il nuovo paese/area padre dell'applicazione nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="de5b0-106">The `DVDAdm.SaveParentalCountry` method saves the application's new parental country/region to the registry.</span></span>

``` syntax
DVD.DVDAdm.SaveParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="de5b0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="de5b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de5b0-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span><span class="sxs-lookup"><span data-stu-id="de5b0-108"><span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*</span></span>
</dt> <dd>

<span data-ttu-id="de5b0-109">Specifica il paese/area padre come intero.</span><span class="sxs-lookup"><span data-stu-id="de5b0-109">Specifies the parental country/region as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="de5b0-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="de5b0-110"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="de5b0-111">Specifica il nome utente sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="de5b0-111">Specifies the user name as a String.</span></span> <span data-ttu-id="de5b0-112">(Attualmente ignorata).</span><span class="sxs-lookup"><span data-stu-id="de5b0-112">(Currently ignored.)</span></span>

</dd> <dt>

<span data-ttu-id="de5b0-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="de5b0-113"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="de5b0-114">Specifica la password sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="de5b0-114">Specifies the password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de5b0-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de5b0-115">Return value</span></span>

<span data-ttu-id="de5b0-116">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="de5b0-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de5b0-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="de5b0-117">Remarks</span></span>

<span data-ttu-id="de5b0-118">Questo metodo consente a un utente che conosce la password corrente di salvare una nuova impostazione del paese padre/area geografica nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="de5b0-118">This method enables a user who knows the current password to save a new parental country/region setting to the registry.</span></span> <span data-ttu-id="de5b0-119">Come per tutti i metodi di **MSDVDAdm**, questo metodo non influisce sul livello corrente del lettore. modifica solo l'impostazione del registro di sistema, in modo che la volta successiva che viene creato l'oggetto MSWebDVD verrà aperto con il nuovo paese/area geografica.</span><span class="sxs-lookup"><span data-stu-id="de5b0-119">As with all the methods of **MSDVDAdm**, this method does not affect the current level in the player; it changes only the registry setting, so that the next time the MSWebDVD object is created, it will open with the new country/region.</span></span> <span data-ttu-id="de5b0-120">Per modificare il paese padre/area geografica nel lettore, chiamare [**SelectParentalCountry**](selectparentalcountry-method.md), che non modifica l'impostazione del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="de5b0-120">To change the parental country/region in the player, call [**SelectParentalCountry**](selectparentalcountry-method.md), which does not change the registry setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="de5b0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de5b0-121">Requirements</span></span>



| <span data-ttu-id="de5b0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="de5b0-122">Requirement</span></span> | <span data-ttu-id="de5b0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="de5b0-123">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="de5b0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de5b0-124">Header</span></span><br/> | <dl> <span data-ttu-id="de5b0-125"><dt>Segmento. h</dt></span><span class="sxs-lookup"><span data-stu-id="de5b0-125"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de5b0-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de5b0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de5b0-127">**SaveParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="de5b0-127">**SaveParentalLevel**</span></span>](saveparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="de5b0-128">Oggetto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="de5b0-128">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




