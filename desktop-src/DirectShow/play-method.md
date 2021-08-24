---
description: Il metodo Play riproduce il titolo del DVD corrente.
ms.assetid: fe9dc266-5b12-479d-85cb-50cc6bb9d580
title: Metodo Play (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d4cea7dc53afc6a116ad052da9a4ca0d52c2e8687d99bde854d3f89fa60a9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633561"
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

Se la riproduzione viene sospesa o arrestata e [**EnableResetOnStop**](enableresetonstop-property.md) è true, la chiamata a **Play** riprenderà la riproduzione alla velocità normale nella posizione corrente. Se la riproduzione viene arrestata e **EnableResetOnStop** è false, la chiamata a **Play** causerà l'avvio della riproduzione del disco all'inizio del primo titolo.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Riprendi**](resume-method.md)
</dt> </dl>

 

 



