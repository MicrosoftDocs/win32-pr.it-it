---
description: Il metodo SelectParentalLevel imposta il livello padre specificato per la riproduzione successiva.
ms.assetid: ffd1e204-6ed2-4190-8635-9f3866d38099
title: Metodo SelectParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb00172b8e61f353c45981af628eb396bca7a7df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521273"
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

Specifica il livello di gestione padre come intero. Per abilitare la gestione padre, il parametro *iLevel* deve essere compreso tra 1 e 8. Per disabilitare la gestione padre, impostare *iLevel* su-1.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Specifica l'utente corrente sotto forma di stringa. (Attualmente ignorata).

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Specifica la password attualmente archiviata nel registro di sistema sotto forma di stringa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questo metodo imposta il livello di accesso nell'oggetto MSWebDVD, che determina il contenuto di cui l'utente può eseguire la riproduzione. I livelli superiori possono riprodurre contenuto di livello inferiore, ma i livelli inferiori non possono riprodurre contenuto di livello superiore. Il significato esatto dei livelli di gestione padre di otto DVD varia a seconda del paese. In Stati Uniti e in Canada, viene eseguito il mapping dei livelli alle categorie di classificazione di Motion Picture Association of America (MPAA). Per impostazione predefinita, la gestione padre in DVD Navigator è disabilitata.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
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

 

 



