---
description: GetPlayerParentalLevel recupera il livello di gestione genitori impostato nell'oggetto MSWebDVD.
ms.assetid: 451e0891-4e5d-4a01-94b8-290f5a804ff1
title: Metodo GetPlayerParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0426c48589449e03b78d894300ff2c83d83d625a269b19f0e985f78d49973f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756481"
---
# <a name="getplayerparentallevel-method"></a>Metodo GetPlayerParentalLevel

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

recupera `GetPlayerParentalLevel` il livello di gestione dei genitori impostato nell'oggetto **MSWebDVD.**

``` syntax
[ iLevel = ] MSWebDVD.GetPlayerParentalLevel()
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che specifica il livello di genitori corrente nello strumento di navigazione DVD oppure -1 se la gestione dei genitori è disabilitata.

## <a name="remarks"></a>Commenti

Un'applicazione lettore è responsabile dell'applicazione del controllo genitori. Il livello di genitori del giocatore è un valore impostato da un'applicazione che può essere usato per indicare il livello di genitori più alto che l'utente corrente può visualizzare. Quando lo strumento di navigazione DVD rileva un nuovo livello genitori, usare questo metodo per determinare se il nuovo livello è maggiore del livello impostato dall'applicazione tramite [**SelectParentalLevel.**](selectparentallevel-method.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**SelezionareParentalCountry**](selectparentalcountry-method.md)
</dt> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> </dl>

 

 



