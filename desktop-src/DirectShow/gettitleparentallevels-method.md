---
description: Il metodo GetTitleParentalLevels recupera i livelli di gestione dei genitori per il titolo specificato.
ms.assetid: 076808d7-6cb6-4d81-b26d-c7945db298f2
title: Metodo GetTitleParentalLevels
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ef462767c280f5e6f1c58679a78ee876e58042dce632f30711c198b4ca574a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536671"
---
# <a name="gettitleparentallevels-method"></a>Metodo GetTitleParentalLevels

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `GetTitleParentalLevels` metodo recupera i livelli di gestione dei genitori per il titolo specificato.

``` syntax
[ iLevels = ] MSWebDVD.GetTitleParentalLevels(iTitle)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Specifica il titolo come integer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero i cui singoli bit indicano i livelli di gestione dei genitori (PML) impostati nel titolo specificato.

## <a name="remarks"></a>Commenti

Un titolo può avere capitoli o anche segmenti brevi con un PML diverso dal PML complessivo per il titolo. Usare questo metodo per determinare tutti i file PML che verranno rilevati durante la riproduzione di un titolo specificato. L'intero restituito è un set di flag di bit definiti come illustrato nella tabella seguente. Eseguire un'operazione AND bit per bit *su iLevels* e ogni valore possibile. Se l'operazione **restituisce true,** significa che PML verrà rilevato a un certo punto di questo titolo.



| Valore  | Descrizione          |
|--------|----------------------|
| 0x100  | DVD Livello genitori 1 |
| 0x200  | DVD Livello genitori 2 |
| 0x400  | DVD Livello genitori 3 |
| 0x800  | DVD Livello genitori 4 |
| 0x1000 | DVD Livello genitori 5 |
| 0x2000 | DVD Livello genitori 6 |
| 0x4000 | DVD Livello genitori 7 |
| 0x8000 | DVD Livello genitori 8 |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**SelezionareParentalCountry**](selectparentalcountry-method.md)
</dt> </dl>

 

 



