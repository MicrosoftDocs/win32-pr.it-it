---
description: Il metodo Render Inizializza il grafico del filtro DVD.
ms.assetid: 910f1e3f-b3bb-498b-93da-3a974a3117e8
title: Metodo Render
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 677abab1c669642c1e51e0041c98949d923147c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303898"
---
# <a name="render-method"></a>Metodo Render

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `Render` metodo inizializza il grafico del filtro DVD.

``` syntax
MSWebDVD.Render(iRender = 0)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*iRender*
</dt> <dd>

Specifica un valore intero che indica se il grafico del filtro verrà eliminato e ricompilato.



| Valore | Descrizione                                                                                         |
|-------|-----------------------------------------------------------------------------------------------------|
| 0     | Il grafico del filtro non verrà eliminato e ricompilato se esiste già. Rappresenta il valore predefinito. |
| 1     | Il grafico del filtro verrà eliminato e ricompilato se esiste già.                                |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il `Render` metodo consente all'oggetto **mswebdvd** di inizializzare completamente il grafo del filtro DirectShow sottostante all'avvio. In questo modo si elimina il lieve ritardo che altrimenti si verifica quando l'utente rilascia il primo comando per riprodurre un disco o visualizzare un menu. Non esistono casi in cui `Render` deve essere chiamato prima di chiamare qualsiasi altro metodo. Se, ad esempio, l'applicazione chiama [**PlayTitle**](playtitle-method.md) prima che il grafico di filtro sia stato inizializzato, l'oggetto **mswebdvd** chiama `Render` automaticamente prima di provare a riprodurre il disco.

 

 



