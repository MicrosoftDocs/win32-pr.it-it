---
description: La proprietà SubpictureOn imposta o recupera lo stato corrente dell'immagine secondaria (attivo o disattivato).
ms.assetid: fa4500bc-48b4-41ed-8b88-0011a0e51c6f
title: Proprietà SubpictureOn
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692df6b69bc960562e9acd223a0e4e156fe00de2206146f609ba15d550b7a961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951770"
---
# <a name="subpictureon-property"></a>Proprietà SubpictureOn

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `SubpictureOn` proprietà imposta o recupera lo stato dell'immagine secondaria corrente (attivo o disattivato).

``` syntax
[ bState = ] MSWebDVD.SubpictureOn
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che indica se l'immagine secondaria viene visualizzata.

## <a name="remarks"></a>Commenti

Questa proprietà non influisce sulla visualizzazione dei sottotitoli codificati. I sottotitoli codificati sono incorporati nel flusso video. Le sotto-immagini DVD vengono trasportate in un flusso separato.

Quando il flusso di immagini secondarie viene modificato usando [**CurrentSubpictureStream,**](currentsubpicturestream-property.md)la `SubpictureOn` proprietà passa a **True.**

Questa proprietà è di lettura/scrittura con il valore predefinito false.

 

 



