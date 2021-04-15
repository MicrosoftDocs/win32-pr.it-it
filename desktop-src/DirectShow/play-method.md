---
description: Il metodo Play riproduce il titolo del DVD corrente.
ms.assetid: fe9dc266-5b12-479d-85cb-50cc6bb9d580
title: Metodo Play (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62323c9c86be476a35977dadf554bbfca3bca91
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521297"
---
# <a name="play-method-directshow"></a>Metodo Play (DirectShow)

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `Play` metodo riproduce il titolo del DVD corrente.

``` syntax
MSWebDVD.Play()
```

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Se la riproduzione viene sospesa o arrestata e [**EnableResetOnStop**](enableresetonstop-property.md) è true, la chiamata di **Play** riprende la riproduzione alla velocità normale nella posizione corrente. Se la riproduzione viene interrotta e **EnableResetOnStop** è false, la chiamata a **Play** provocherà la riproduzione del disco all'inizio del primo titolo.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riprendi**](resume-method.md)
</dt> </dl>

 

 



