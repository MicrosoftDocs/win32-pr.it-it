---
description: La proprietà CurrentSubpictureStream imposta o recupera il flusso di immagini secondarie corrente.
ms.assetid: 66473c87-ddfe-4555-89ad-90e210a75694
title: Proprietà CurrentSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e9c4af677180d4893ef56a9d2bff1fb034971969e2e64d648d53e19d0814a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821946"
---
# <a name="currentsubpicturestream-property"></a>Proprietà CurrentSubpictureStream

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `CurrentSubpictureStream` proprietà imposta o recupera il flusso di immagini secondarie corrente.

``` syntax
[ iSPStream = ] MSWebDVD.CurrentSubpictureStream
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta il flusso.

## <a name="remarks"></a>Commenti

I valori possibili di questa proprietà sono:



| Valore   | Descrizione              |
|---------|--------------------------|
| Da 0 a 31 | Flusso di immagini secondarie    |
| 63      | Flusso a bitrate basso disattivato |



 

Questa proprietà è di lettura/scrittura senza alcun valore predefinito. Prima di impostare un nuovo flusso di immagini secondarie, chiamare [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) per verificare che il flusso sia disponibile.

Se si imposta questa proprietà, [**la proprietà SubpictureOn**](subpictureon-property.md) viene impostata su **True.**

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Immagine secondariaOn**](subpictureon-property.md)
</dt> <dt>

[**SubpictureStreamsAvailable**](subpicturestreamsavailable-property.md)
</dt> </dl>

 

 



