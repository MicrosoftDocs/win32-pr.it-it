---
description: Il metodo AcceptParentalLevelChange accetta o rifiuta il nuovo livello di gestione genitori temporaneo.
ms.assetid: b3d58069-16dc-4598-90ea-6136c2f62ac7
title: Metodo AcceptParentalLevelChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea4742622ce9a2c65cdce660a8bae7fab6f84171d6bd61cdf88475c2bcd788c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873591"
---
# <a name="acceptparentallevelchange-method"></a>Metodo AcceptParentalLevelChange

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il metodo AcceptParentalLevelChange accetta o rifiuta il nuovo livello di gestione genitori temporaneo.

``` syntax
        MSWebDVD.AcceptParentalLevelChange(bAccept)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*bAccept*
</dt> <dd>

Specifica il nuovo livello di genitori come valore booleano.



| Valore | Descrizione                               |
|-------|-------------------------------------------|
| true  | Accettare il nuovo livello di gestione dei genitori. |
| false | Rifiutare il nuovo livello di gestione dei genitori. |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Chiamare questo metodo in risposta a una notifica dell'evento EC DVD PARENTAL LEVEL CHANGE per specificare se lo strumento di spostamento DVD deve riprodurre il contenuto con il nuovo livello di genitorio o un ramo in cui il disco specifica se il nuovo livello viene \_ \_ \_ \_ rifiutato.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Applicazione dei livelli di gestione dei genitori](enforcing-parental-management-levels.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**NotifyParentalLevelChange**](notifyparentallevelchange-method.md)
</dt> <dt>

[**SelezionareParentalCountry**](selectparentalcountry-method.md)
</dt> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> </dl>

 

 



