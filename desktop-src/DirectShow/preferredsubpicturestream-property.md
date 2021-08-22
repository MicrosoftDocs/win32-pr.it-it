---
description: La proprietà PreferredSubpictureStream recupera il flusso di immagini secondarie preferito per la sessione di visualizzazione corrente.
ms.assetid: 9c15dc6f-c016-41bf-b03d-e8e5415215ae
title: Proprietà PreferredSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e28b98163607e31a207bffb3974fee3b32505ff60ba3700b452b2dff2625f421
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583541"
---
# <a name="preferredsubpicturestream-property"></a>Proprietà PreferredSubpictureStream

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `PreferredSubpictureStream` proprietà recupera il flusso di immagini secondarie preferito per la sessione di visualizzazione corrente.

``` syntax
[iStream = ] MSWebDVD.PreferredSubpictureStream
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore Integer che rappresenta il flusso di immagini secondarie preferito corrente nel Registro di sistema.

## <a name="remarks"></a>Commenti

Il flusso di immagini secondarie preferito viene impostato con [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md)dell'oggetto [MSDVDAdm.](msdvdadm-object.md)

 

 



