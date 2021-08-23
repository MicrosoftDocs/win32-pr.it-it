---
description: Il metodo SelectParentalCountry imposta il paese/area geografica dei genitori specificato per la riproduzione successiva.
ms.assetid: 70368351-c7b9-4640-a4f7-7d972b8e4628
title: Metodo SelectParentalCountry
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d148145f2c38cdb01da209e02f6400301da851e1d2b41e5adaf84b2338ad21c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684061"
---
# <a name="selectparentalcountry-method"></a>Metodo SelectParentalCountry

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `SelectParentalCountry` metodo imposta il paese/area genitori specificato per la riproduzione successiva.

``` syntax
MSWebDVD.SelectParentalCountry(iCountry, sUserName, sPassword)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iCountry"></span><span id="icountry"></span><span id="ICOUNTRY"></span>*iCountry*
</dt> <dd>

Specifica il paese come numero intero.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Specifica l'utente connesso corrente come stringa. (Attualmente ignorato).

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Specifica la stringa della password dell'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il paese/area geografica dei genitori determina come vengono interpretati i livelli dei genitori.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
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

 

 



