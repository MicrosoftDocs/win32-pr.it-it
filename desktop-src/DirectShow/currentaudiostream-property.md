---
description: La proprietà CurrentAudioStream imposta o recupera il numero del flusso audio abilitato.
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: Proprietà CurrentAudioStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd814d5b560ed55ea312fbebb8678c67b1422b0cf3d47917fbf772f56a0d3afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075971"
---
# <a name="currentaudiostream-property"></a>Proprietà CurrentAudioStream

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `CurrentAudioStream` proprietà imposta o recupera il numero del flusso audio abilitato.

``` syntax
[ iStream = ] MSWebDVD.CurrentAudioStream
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero compreso tra 0 e 7 che indica il flusso audio corrente.

## <a name="remarks"></a>Commenti

Questa proprietà è di lettura/scrittura senza alcun valore predefinito. Prima di tentare di impostare un nuovo flusso audio, chiamare [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) per verificare che il flusso sia disponibile.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AudioStreamsAvailable**](audiostreamsavailable-property.md)
</dt> </dl>

 

 



