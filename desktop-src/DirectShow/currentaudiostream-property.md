---
description: La proprietà CurrentAudioStream imposta o Recupera il numero del flusso audio abilitato.
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: Proprietà CurrentAudioStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b67d81eeec21aec164f3ca865ee3f2de4cd3f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304118"
---
# <a name="currentaudiostream-property"></a>Proprietà CurrentAudioStream

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `CurrentAudioStream` proprietà imposta o Recupera il numero del flusso audio abilitato.

``` syntax
[ iStream = ] MSWebDVD.CurrentAudioStream
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero compreso tra 0 e 7 che indica il flusso audio corrente.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura e non prevede alcun valore predefinito. Prima di provare a impostare un nuovo flusso audio, chiamare [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) per verificare che il flusso sia disponibile.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AudioStreamsAvailable**](audiostreamsavailable-property.md)
</dt> </dl>

 

 



