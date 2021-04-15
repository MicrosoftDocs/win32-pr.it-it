---
description: Il metodo GetAudioLanguage recupera una stringa che indica quale lingua è disponibile nel flusso audio specificato.
ms.assetid: 5ff12058-eb00-4a2c-8d39-88282f68f001
title: Metodo GetAudioLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af71ad7943fe5442ded09f0b599c64c4b7215dac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520649"
---
# <a name="getaudiolanguage-method"></a><span data-ttu-id="41219-103">Metodo GetAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="41219-103">GetAudioLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="41219-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="41219-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="41219-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="41219-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="41219-106">Il `GetAudioLanguage` metodo recupera una stringa che indica quale lingua è disponibile nel flusso audio specificato.</span><span class="sxs-lookup"><span data-stu-id="41219-106">The `GetAudioLanguage` method retrieves a string indicating which language is available on the specified audio stream.</span></span>

``` syntax
[ slang = ] MSWebDVD.GetAudioLanguage(iStream)
```

## <a name="parameters"></a><span data-ttu-id="41219-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="41219-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41219-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="41219-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="41219-109">Specifica il numero di flusso audio nel titolo corrente come intero.</span><span class="sxs-lookup"><span data-stu-id="41219-109">Specifies the audio stream number in the current title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41219-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41219-110">Return Value</span></span>

<span data-ttu-id="41219-111">Restituisce una stringa leggibile che identifica la lingua del flusso audio nel titolo corrente.</span><span class="sxs-lookup"><span data-stu-id="41219-111">Returns a human-readable string identifying the language of the audio stream in the current title.</span></span>

 

 



