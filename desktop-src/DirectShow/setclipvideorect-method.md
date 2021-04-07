---
description: Il metodo SetClipVideoRect esegue lo zoom della visualizzazione video sul sottorettangolo specificato.
ms.assetid: 3940a382-8d53-4ff9-b024-38de1aa00f54
title: Metodo SetClipVideoRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7f4b003ef20b82f1e783ebf074e8bbd5cc793
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746295"
---
# <a name="setclipvideorect-method"></a>Metodo SetClipVideoRect

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `SetClipVideoRect` metodo esegue lo zoom della visualizzazione video sul sottorettangolo specificato.

``` syntax
MSWebDVD.SetClipVideoRect(oRect)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*
</dt> <dd>

Specifica un oggetto [DVDRect](dvdrect-object.md) che contiene il rettangolo di ridimensionamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Quando si imposta un nuovo rettangolo di ridimensionamento, l'oggetto ingrandisce l'area per adattarla alle dimensioni di visualizzazione complessive dell'applicazione. Questo consente di creare l'effetto zoom avanti su un'area specifica dello schermo. Per specificare il rettangolo, creare un nuovo oggetto [DVDRect](dvdrect-object.md) e compilare le relative proprietà.

Il rettangolo più comune per la visualizzazione video è 720 x 540.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetClipVideoRect**](getclipvideorect-method.md)
</dt> </dl>

 

 



