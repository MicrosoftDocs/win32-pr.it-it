---
description: La proprietà DVDAdm. DefaultSubpictureLCID imposta o recupera l'impostazione del registro di sistema per l'LCID predefinito specificato dall'utente per il flusso di immagine.
ms.assetid: 12dd308e-483b-489d-8d81-8da399bfac4d
title: Proprietà DefaultSubpictureLCID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f52227dc220bef474e872cbd695c78dc65f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522785"
---
# <a name="defaultsubpicturelcid-property"></a><span data-ttu-id="6b527-103">Proprietà DefaultSubpictureLCID</span><span class="sxs-lookup"><span data-stu-id="6b527-103">DefaultSubpictureLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="6b527-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6b527-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="6b527-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="6b527-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="6b527-106">La `DVDAdm.DefaultSubpictureLCID` proprietà imposta o recupera l'impostazione del registro di sistema per l'LCID predefinito specificato dall'utente per il flusso dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="6b527-106">The `DVDAdm.DefaultSubpictureLCID` property sets or retrieves the registry setting for the user-specified default LCID for the subpicture stream.</span></span>

``` syntax
[ iSubpictureLCID = ] DVD.DVDAdm.DefaultSubpictureLCID
```

## <a name="return-value"></a><span data-ttu-id="6b527-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b527-107">Return Value</span></span>

<span data-ttu-id="6b527-108">Restituisce un valore intero che rappresenta l'LCID della sottoimmagine predefinita specificato dall'utente come archiviato nelle impostazioni del registro di sistema per l'applicazione DVD.</span><span class="sxs-lookup"><span data-stu-id="6b527-108">Returns an Integer value representing the user-specified default subpicture LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="6b527-109">Questo valore non è necessariamente lo stesso del flusso di immagine predefinita come creato nel DVD.</span><span class="sxs-lookup"><span data-stu-id="6b527-109">This value is not necessarily the same as the default subpicture stream as authored on the DVD.</span></span> <span data-ttu-id="6b527-110">Per l'intervallo degli LCID validi, vedere la documentazione di Win32 in Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="6b527-110">For the range of valid LCIDs, see the Win32 documentation in the Platform SDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b527-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b527-111">Remarks</span></span>

<span data-ttu-id="6b527-112">Questa proprietà è di lettura/scrittura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="6b527-112">This property is read/write with no default value.</span></span> <span data-ttu-id="6b527-113">Se non viene specificato alcun LCID della sottoimmagine predefinita, l'oggetto MSDVDAdm riprodurrà il flusso dell'immagine subpicture contrassegnato come flusso predefinito sul disco.</span><span class="sxs-lookup"><span data-stu-id="6b527-113">If no default subpicture LCID is specified, the MSDVDAdm object will play the subpicture stream that is marked as the default stream on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b527-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b527-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b527-115">Oggetto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="6b527-115">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



