---
description: La proprietà CurrentSubpictureStream imposta o Recupera il flusso di sottoimmagine corrente.
ms.assetid: 66473c87-ddfe-4555-89ad-90e210a75694
title: Proprietà CurrentSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c954ad7cfb7aba6dd9bc800ac983d86b6325843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522569"
---
# <a name="currentsubpicturestream-property"></a>Proprietà CurrentSubpictureStream

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `CurrentSubpictureStream` proprietà imposta o Recupera il flusso di sottoimmagine corrente.

``` syntax
[ iSPStream = ] MSWebDVD.CurrentSubpictureStream
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta il flusso.

## <a name="remarks"></a>Commenti

I valori possibili di questa proprietà sono:



| Valore   | Descrizione              |
|---------|--------------------------|
| da 0 a 31 | Flusso di sottoimmagine    |
| 63      | Flusso a bitrate ridotto disattivato |



 

Questa proprietà è di lettura/scrittura e non prevede alcun valore predefinito. Prima di impostare un nuovo flusso di sottoimmagine, chiamare [**IsSubpictureStreamEnabled**](issubpicturestreamenabled-method.md) per verificare che il flusso sia disponibile.

L'impostazione di questa proprietà fa sì che la proprietà [**SubpictureOn**](subpictureon-property.md) sia impostata su **true**.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SubpictureOn**](subpictureon-property.md)
</dt> <dt>

[**SubpictureStreamsAvailable**](subpicturestreamsavailable-property.md)
</dt> </dl>

 

 



