---
description: La proprietà PreferredSubpictureStream Recupera il flusso della sottoimmagine preferita per la sessione di visualizzazione corrente.
ms.assetid: 9c15dc6f-c016-41bf-b03d-e8e5415215ae
title: Proprietà PreferredSubpictureStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23377d74d3632c665b001ae415dc151ca73bd148
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876517"
---
# <a name="preferredsubpicturestream-property"></a>Proprietà PreferredSubpictureStream

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `PreferredSubpictureStream` proprietà recupera il flusso di sottoimmagine preferito per la sessione di visualizzazione corrente.

``` syntax
[iStream = ] MSWebDVD.PreferredSubpictureStream
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero che rappresenta il flusso dell'immagine preferita corrente nel registro di sistema.

## <a name="remarks"></a>Commenti

Il flusso di sottoimmagine preferito viene impostato con il [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md)dell'oggetto [MSDVDAdm](msdvdadm-object.md) .

 

 



