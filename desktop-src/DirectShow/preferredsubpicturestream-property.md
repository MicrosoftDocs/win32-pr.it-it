---
description: La proprietà PreferredSubpictureStream Recupera il flusso della sottoimmagine preferita per la sessione di visualizzazione corrente.
ms.assetid: 9c15dc6f-c016-41bf-b03d-e8e5415215ae
title: Proprietà PreferredSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23377d74d3632c665b001ae415dc151ca73bd148
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876517"
---
# <a name="preferredsubpicturestream-property"></a><span data-ttu-id="71936-103">Proprietà PreferredSubpictureStream</span><span class="sxs-lookup"><span data-stu-id="71936-103">PreferredSubpictureStream Property</span></span>

> [!Note]  
> <span data-ttu-id="71936-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="71936-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="71936-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="71936-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="71936-106">La `PreferredSubpictureStream` proprietà recupera il flusso di sottoimmagine preferito per la sessione di visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="71936-106">The `PreferredSubpictureStream` property retrieves the preferred subpicture stream for the current viewing session.</span></span>

``` syntax
[iStream = ] MSWebDVD.PreferredSubpictureStream
```

## <a name="return-value"></a><span data-ttu-id="71936-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71936-107">Return Value</span></span>

<span data-ttu-id="71936-108">Restituisce un valore intero che rappresenta il flusso dell'immagine preferita corrente nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="71936-108">Returns an Integer value representing the current preferred subpicture stream in the system registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="71936-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="71936-109">Remarks</span></span>

<span data-ttu-id="71936-110">Il flusso di sottoimmagine preferito viene impostato con il [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md)dell'oggetto [MSDVDAdm](msdvdadm-object.md) .</span><span class="sxs-lookup"><span data-stu-id="71936-110">The preferred subpicture stream is set with [MSDVDAdm](msdvdadm-object.md) object's [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md).</span></span>

 

 



