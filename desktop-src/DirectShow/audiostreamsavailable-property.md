---
description: La proprietà AudioStreamsAvailable Recupera il numero di flussi audio disponibili nel titolo corrente.
ms.assetid: 4359ec30-920a-4b34-8e27-4cf1d9452aa8
title: Proprietà AudioStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb68020b30f4349fcbbb464150624d75250a0dbf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876409"
---
# <a name="audiostreamsavailable-property"></a><span data-ttu-id="bcd7b-103">Proprietà AudioStreamsAvailable</span><span class="sxs-lookup"><span data-stu-id="bcd7b-103">AudioStreamsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="bcd7b-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bcd7b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="bcd7b-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="bcd7b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="bcd7b-106">La `AudioStreamsAvailable` proprietà recupera il numero di flussi audio disponibili nel titolo corrente.</span><span class="sxs-lookup"><span data-stu-id="bcd7b-106">The `AudioStreamsAvailable` property retrieves the number of audio streams available in the current title.</span></span>

``` syntax
[ iStreams = ] MSWebDVD.AudioStreamsAvailable
```

## <a name="return-value"></a><span data-ttu-id="bcd7b-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bcd7b-107">Return Value</span></span>

<span data-ttu-id="bcd7b-108">Restituisce un valore intero compreso tra 1 e 8 che rappresenta il numero di flussi audio disponibili nel titolo corrente.</span><span class="sxs-lookup"><span data-stu-id="bcd7b-108">Returns an integer value from 1 through 8 representing the number of audio streams available in the current title.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcd7b-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="bcd7b-109">Remarks</span></span>

<span data-ttu-id="bcd7b-110">Questa proprietà è di sola lettura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="bcd7b-110">This property is read-only with no default value.</span></span> <span data-ttu-id="bcd7b-111">L'uso principale di più flussi audio consiste nel fornire colonne di film in più linguaggi.</span><span class="sxs-lookup"><span data-stu-id="bcd7b-111">The primary use of multiple audio streams is to provide movie soundtracks in more than one language.</span></span> <span data-ttu-id="bcd7b-112">In genere, non tutti i titoli di un disco hanno tutti i flussi audio abilitati.</span><span class="sxs-lookup"><span data-stu-id="bcd7b-112">Typically, not every title on a disc has all audio streams enabled.</span></span> <span data-ttu-id="bcd7b-113">Il film di funzionalità, ad esempio, potrebbe avere Soundtrack in tre lingue diverse, ma i trailer potrebbero avere solo una colonna della lingua inglese.</span><span class="sxs-lookup"><span data-stu-id="bcd7b-113">For example, the feature movie might have soundtracks in three different languages, but the trailers might have only an English soundtrack.</span></span> <span data-ttu-id="bcd7b-114">Prima che un utente possa selezionare un flusso, l'applicazione deve determinare quali flussi sono disponibili nel titolo corrente.</span><span class="sxs-lookup"><span data-stu-id="bcd7b-114">Before a user can select a stream, the application must determine which streams are available within the current title.</span></span> <span data-ttu-id="bcd7b-115">Si noti che determinati flussi sono identificati da un indice compreso tra 0 e 7.</span><span class="sxs-lookup"><span data-stu-id="bcd7b-115">Note that particular streams are identified by an index from zero through 7.</span></span>

<span data-ttu-id="bcd7b-116">I dischi di solito presentano un menu che mostra le Soundtrack disponibili, consentendo all'utente di selezionare il flusso audio da abilitare.</span><span class="sxs-lookup"><span data-stu-id="bcd7b-116">Discs generally present a menu showing the available soundtracks, enabling the user to select the audio stream to enable.</span></span>

## <a name="see-also"></a><span data-ttu-id="bcd7b-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bcd7b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcd7b-118">**GetAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="bcd7b-118">**GetAudioLanguage**</span></span>](getaudiolanguage-method.md)
</dt> </dl>

 

 



