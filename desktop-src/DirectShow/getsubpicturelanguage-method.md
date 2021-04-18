---
description: Il metodo GetSubpictureLanguage recupera la lingua per il flusso di sottoimmagine specificato.
ms.assetid: 2a2e6961-99c3-4200-b462-b381f9e37066
title: Metodo GetSubpictureLanguage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f87d1bf95ee13a1a15e631e2bc53477b62b789a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303742"
---
# <a name="getsubpicturelanguage-method"></a><span data-ttu-id="0bea8-103">Metodo GetSubpictureLanguage</span><span class="sxs-lookup"><span data-stu-id="0bea8-103">GetSubpictureLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="0bea8-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0bea8-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="0bea8-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="0bea8-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="0bea8-106">Il `GetSubpictureLanguage` metodo recupera la lingua per il flusso di sottoimmagine specificato.</span><span class="sxs-lookup"><span data-stu-id="0bea8-106">The `GetSubpictureLanguage` method retrieves the language for the specified subpicture stream.</span></span>

``` syntax
[ sLang = ] MSWebDVD.GetSubpictureLanguage(iStream)
```

## <a name="parameters"></a><span data-ttu-id="0bea8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0bea8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bea8-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="0bea8-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="0bea8-109">Specifica il numero del flusso dell'immagine di sottoimmagine di cui si desidera recuperare la lingua del testo come intero.</span><span class="sxs-lookup"><span data-stu-id="0bea8-109">Specifies the subpicture stream number whose text language you want to retrieve as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bea8-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0bea8-110">Return Value</span></span>

<span data-ttu-id="0bea8-111">Restituisce una stringa leggibile che identifica la lingua del flusso audio nel titolo corrente.</span><span class="sxs-lookup"><span data-stu-id="0bea8-111">Returns a human-readable string identifying the language of the audio stream in the current title.</span></span>

 

 



