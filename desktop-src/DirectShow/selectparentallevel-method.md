---
description: Il metodo SelectParentalLevel imposta il livello di genitori specificato per la riproduzione successiva.
ms.assetid: ffd1e204-6ed2-4190-8635-9f3866d38099
title: Metodo SelectParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95de7e8cbf1fb6fa284eddefa1ba07ebb9268825116fdac9c97fbd5d42bac84e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684041"
---
# <a name="selectparentallevel-method"></a>Metodo SelectParentalLevel

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `SelectParentalLevel` metodo imposta il livello padre specificato per la riproduzione successiva.

``` syntax
MSWebDVD.SelectParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*
</dt> <dd>

Specifica il livello di gestione dei genitori come integer. Per abilitare la gestione dei genitori, il *parametro iLevel* deve essere compreso tra 1 e 8. Per disabilitare la gestione dei genitori, impostare *iLevel* su -1.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Specifica l'utente corrente come stringa. (Attualmente ignorato).

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Specifica la password attualmente archiviata nel Registro di sistema come stringa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questo metodo imposta il livello di accesso nell'oggetto MSWebDVD, che determina il contenuto che l'utente può riprodurre. I livelli superiori possono riprodurre contenuto di livello inferiore, ma i livelli inferiori non possono riprodurre contenuto di livello superiore. Il significato esatto degli otto livelli di gestione dei genitori dvd varia a seconda del paese o dell'area geografica. Nel Stati Uniti e in Canada, i livelli vengono mappati alle categorie di classificazione MPAA (Motion Picture Association of America). La gestione dei genitori nello strumento di navigazione DVD è disabilitata per impostazione predefinita.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SelezionareParentalCountry**](selectparentalcountry-method.md)
</dt> <dt>

[**NotifyParentalLevelChange**](notifyparentallevelchange-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**AcceptParentalLevelChange**](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



