---
description: Il metodo SetClipVideoRect consente di ingrandire la visualizzazione video fino al sottorectangle specificato.
ms.assetid: 3940a382-8d53-4ff9-b024-38de1aa00f54
title: Metodo SetClipVideoRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7741a2604ed1c2896b105295020893e23b447e3fa6f6ab7c53def92aa508c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078871"
---
# <a name="setclipvideorect-method"></a>Metodo SetClipVideoRect

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `SetClipVideoRect` metodo consente di ingrandire la visualizzazione video fino al sottorectangle specificato.

``` syntax
MSWebDVD.SetClipVideoRect(oRect)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*
</dt> <dd>

Specifica un oggetto [DVDRect](dvdrect-object.md) che contiene il rettangolo di ritaglio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Quando si imposta un nuovo rettangolo di ritaglio, l'oggetto ingrandisce tale area in base alle dimensioni di visualizzazione complessive dell'applicazione. In questo modo viene creato l'effetto di zoom avanti su una determinata area dello schermo. Per specificare il rettangolo, creare un nuovo [oggetto DVDRect](dvdrect-object.md) e specificarne le proprietà.

Il rettangolo più comune per la visualizzazione di video è 720 x 540.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetClipVideoRect**](getclipvideorect-method.md)
</dt> </dl>

 

 



