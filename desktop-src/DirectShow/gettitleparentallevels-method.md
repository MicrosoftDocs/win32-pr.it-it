---
description: Il metodo GetTitleParentalLevels recupera i livelli di gestione padre per il titolo specificato.
ms.assetid: 076808d7-6cb6-4d81-b26d-c7945db298f2
title: Metodo GetTitleParentalLevels
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6db82ca21c2fdd023aa472e4c3428260464a8612
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401210"
---
# <a name="gettitleparentallevels-method"></a>Metodo GetTitleParentalLevels

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `GetTitleParentalLevels` metodo recupera i livelli di gestione padre per il titolo specificato.

``` syntax
[ iLevels = ] MSWebDVD.GetTitleParentalLevels(iTitle)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Specifica il titolo come intero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero i cui singoli bit indicano i livelli di gestione padre (PML) impostati nel titolo specificato.

## <a name="remarks"></a>Commenti

Un titolo può includere capitoli o segmenti brevi che hanno un PML diverso dal totale di PML per il titolo. Utilizzare questo metodo per determinare tutti gli PMLs che verranno rilevati durante la riproduzione di un titolo specificato. Il numero intero restituito è un set di flag di bit definiti come illustrato nella tabella seguente. Eseguire un'operazione con AND bit per bit su *iLevels* e ogni valore possibile. Se l'operazione restituisce **true**, il valore PML verrà rilevato in un determinato punto del titolo.



| Valore  | Descrizione          |
|--------|----------------------|
| 0x100  | Livello padre 1 DVD |
| 0x200  | Livello parentale DVD 2 |
| 0x400  | Livello parentale DVD 3 |
| 0x800  | Livello parentale DVD 4 |
| 0x1000 | Livello parentale DVD 5 |
| 0x2000 | DVD padre livello 6 |
| 0x4000 | Livello parentale DVD 7 |
| 0x8000 | Livello parentale DVD 8 |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> </dl>

 

 



