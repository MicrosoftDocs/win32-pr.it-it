---
description: La proprietà CurrentAudioStream imposta o Recupera il numero del flusso audio abilitato.
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: Proprietà CurrentAudioStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b67d81eeec21aec164f3ca865ee3f2de4cd3f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304118"
---
# <a name="currentaudiostream-property"></a><span data-ttu-id="f1230-103">Proprietà CurrentAudioStream</span><span class="sxs-lookup"><span data-stu-id="f1230-103">CurrentAudioStream Property</span></span>

> [!Note]  
> <span data-ttu-id="f1230-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f1230-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f1230-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="f1230-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f1230-106">La `CurrentAudioStream` proprietà imposta o Recupera il numero del flusso audio abilitato.</span><span class="sxs-lookup"><span data-stu-id="f1230-106">The `CurrentAudioStream` property sets or retrieves the number of the enabled audio stream.</span></span>

``` syntax
[ iStream = ] MSWebDVD.CurrentAudioStream
```

## <a name="return-value"></a><span data-ttu-id="f1230-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1230-107">Return Value</span></span>

<span data-ttu-id="f1230-108">Restituisce un valore intero compreso tra 0 e 7 che indica il flusso audio corrente.</span><span class="sxs-lookup"><span data-stu-id="f1230-108">Returns an integer value from 0 through 7 indicating the current audio stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1230-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1230-109">Remarks</span></span>

<span data-ttu-id="f1230-110">Questa proprietà è di lettura/scrittura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="f1230-110">This property is read/write with no default value.</span></span> <span data-ttu-id="f1230-111">Prima di provare a impostare un nuovo flusso audio, chiamare [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) per verificare che il flusso sia disponibile.</span><span class="sxs-lookup"><span data-stu-id="f1230-111">Before attempting to set a new audio stream, call [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) to verify that the stream is available.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1230-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1230-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1230-113">**AudioStreamsAvailable**</span><span class="sxs-lookup"><span data-stu-id="f1230-113">**AudioStreamsAvailable**</span></span>](audiostreamsavailable-property.md)
</dt> </dl>

 

 



