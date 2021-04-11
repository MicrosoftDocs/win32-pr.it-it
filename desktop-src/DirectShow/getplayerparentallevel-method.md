---
description: GetPlayerParentalLevel Recupera il livello di gestione padre impostato nell'oggetto MSWebDVD.
ms.assetid: 451e0891-4e5d-4a01-94b8-290f5a804ff1
title: Metodo GetPlayerParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bac51e776a45e0d1fa748fc995240292474e902
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123498"
---
# <a name="getplayerparentallevel-method"></a>Metodo GetPlayerParentalLevel

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

`GetPlayerParentalLevel`Recupera il livello di gestione padre impostato nell'oggetto **mswebdvd** .

``` syntax
[ iLevel = ] MSWebDVD.GetPlayerParentalLevel()
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che specifica il livello padre corrente nel navigatore DVD oppure-1 se la gestione padre è disabilitata.

## <a name="remarks"></a>Commenti

Un'applicazione lettore è responsabile dell'applicazione dei controlli padre. Il livello padre del lettore è un valore impostato da un'applicazione che può essere usato per indicare il livello padre più alto che l'utente corrente può visualizzare. Quando il navigatore DVD rileva un nuovo livello padre, usare questo metodo per determinare se il nuovo livello è maggiore del livello impostato dall'applicazione tramite [**SelectParentalLevel**](selectparentallevel-method.md).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> </dl>

 

 



