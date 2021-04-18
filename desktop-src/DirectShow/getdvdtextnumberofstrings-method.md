---
description: Il metodo GetDVDTextNumberOfStrings Recupera il numero di stringhe di testo disponibili per la lingua specificata.
ms.assetid: 84d2b5b7-b474-48a4-9058-ea9da8109398
title: Metodo GetDVDTextNumberOfStrings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18c9c4fadfd28d6cddc8b9013a6e426aebe9f816
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304198"
---
# <a name="getdvdtextnumberofstrings-method"></a>Metodo GetDVDTextNumberOfStrings

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `GetDVDTextNumberOfStrings` metodo recupera il numero di stringhe di testo disponibili per la lingua specificata.

``` syntax
[ iStrings = ] MSWebDVD.GetDVDTextNumberOfStrings(iLangIndex)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iLangIndex"></span><span id="ilangindex"></span><span id="ILANGINDEX"></span>*iLangIndex*
</dt> <dd>

Specifica il linguaggio come intero. Il valore deve essere compreso tra zero e uno minore del valore restituito da [**GetDVDTextNumberOfLanguages**](getdvdtextnumberoflanguages-method.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che specifica il numero di stringhe contenute nel disco nella lingua specificata.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetto MSWebDVD](mswebdvd-object.md)
</dt> </dl>

 

 



