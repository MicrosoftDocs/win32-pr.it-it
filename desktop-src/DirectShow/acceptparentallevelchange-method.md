---
description: Il metodo AcceptParentalLevelChange accetta o rifiuta il nuovo livello di gestione padre temporaneo.
ms.assetid: b3d58069-16dc-4598-90ea-6136c2f62ac7
title: Metodo AcceptParentalLevelChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b2e81d1d82c4ede14580ed65d88566738dac1b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304276"
---
# <a name="acceptparentallevelchange-method"></a>Metodo AcceptParentalLevelChange

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il metodo AcceptParentalLevelChange accetta o rifiuta il nuovo livello di gestione padre temporaneo.

``` syntax
        MSWebDVD.AcceptParentalLevelChange(bAccept)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*bAccept*
</dt> <dd>

Specifica il nuovo livello padre come valore booleano.



| Valore | Descrizione                               |
|-------|-------------------------------------------|
| true  | Accettare il nuovo livello di gestione padre. |
| false | Rifiutare il nuovo livello di gestione padre. |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Chiamare questo metodo in risposta a una \_ notifica degli \_ eventi di modifica del livello padre di un DVD EC \_ \_ per specificare se il navigatore DVD deve riprodurre il contenuto con il nuovo livello padre oppure creare un ramo in cui il disco specifichi se il nuovo livello viene rifiutato.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Applicazione dei livelli di gestione padre](enforcing-parental-management-levels.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**NotifyParentalLevelChange**](notifyparentallevelchange-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> </dl>

 

 



