---
description: La proprietà CurrentCCService imposta o recupera il servizio di sottotitoli codificati corrente.
ms.assetid: 094cf812-3122-4d5f-af8a-afd1c2264a2b
title: Proprietà CurrentCCService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d836e852d1a144abb5422f71d0127eb9c37b8f333dce0723db2c2b3b1889ec50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075961"
---
# <a name="currentccservice-property"></a>Proprietà CurrentCCService

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `CurrentCCService` proprietà imposta o recupera il servizio di sottotitoli codificati corrente.

``` syntax
[ iService = ] MSWebDVD.CurrentCCService
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che indica il tipo di servizio di sottotitoli codificati abilitato.

## <a name="remarks"></a>Commenti

I valori possibili di questa proprietà sono:



| Valore | Descrizione                                                          |
|-------|----------------------------------------------------------------------|
| 0x0   | Nessun servizio corrente. Si tratta del valore predefinito.                       |
| 0x1   | Didascalia vera, primo campo. Servizio predefinito.                       |
| 0x2   | Sottotitoli per la lingua secondaria, secondo campo. In genere non viene usato. |



 

Si tratta di una proprietà di lettura/scrittura.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CCActive**](ccactive-property.md)
</dt> </dl>

 

 



