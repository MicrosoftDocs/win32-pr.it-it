---
description: La proprietà DefaultAudioLanguageExt recupera l'estensione predefinita del linguaggio audio DVD.
ms.assetid: 628af2aa-e528-4689-953b-558e13e1d513
title: Proprietà DefaultAudioLanguageExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5ce89099cd8e31cde9beb8bb3c8a9f1e16b3b0f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520962"
---
# <a name="defaultaudiolanguageext-property"></a>Proprietà DefaultAudioLanguageExt

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `DefaultAudioLanguageExt` proprietà recupera l'estensione predefinita del linguaggio audio DVD.

``` syntax
[ iLangExt = ] MSWebDVD.DefaultAudioLanguageExt
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che indica l'estensione predefinita della lingua audio. Per i valori possibili, vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura e non prevede alcun valore predefinito. La tabella seguente mostra i valori possibili per le estensioni del linguaggio audio DVD.



| Valore | Descrizione       |
|-------|-------------------|
| 0     | NotSpecified      |
| 1     | Sottotitoli          |
| 2     | VisuallyImpaired  |
| 3     | DirectorComments1 |
| 4     | DirectorComments2 |



 

 

 



