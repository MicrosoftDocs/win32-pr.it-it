---
description: Il metodo GetKaraokeChannelContent recupera un valore che indica il tipo di contenuto nel canale Karaoke specificato nel flusso specificato.
ms.assetid: e36a88b8-7184-44a4-8e02-204440f651bc
title: Metodo GetKaraokeChannelContent
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd35705f1fba65eaf5c6f7c67ea55078c68e5036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304004"
---
# <a name="getkaraokechannelcontent-method"></a>Metodo GetKaraokeChannelContent

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `GetKaraokeChannelContent` metodo recupera un valore che indica il tipo di contenuto nel canale Karaoke specificato nel flusso specificato.

``` syntax
[ iContent = ] MSWebDVD.GetKaraokeChannelContent(iStream, iChannel)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Specifica il flusso audio come intero.

</dd> <dt>

<span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*iChannel*
</dt> <dd>

Specifica il canale come intero. I valori possibili per ogni canale sono:



| Valore  | Descrizione    |
|--------|----------------|
| 0x0001 | Guida vocale 1  |
| 0x0002 | Guida vocale 2  |
| 0x0004 | Guida melodia 1 |
| 0x0008 | Guida melodia 2 |
| 0x0010 | Guida melodia A |
| 0x0020 | Guida melodia B |
| 0x0040 | Effetto audio A |
| 0x0080 | Effetto audio B |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero i cui singoli bit specificano il contenuto del canale Karaoke.

## <a name="remarks"></a>Commenti

La numerazione del canale audio DVD è in base zero, quindi i canali 2, 3 e 4 sono i canali karaoke ausiliari. Dopo la restituzione del metodo, eseguire un'operazione AND bit per bit su *IContent* per determinare il contenuto di ogni canale. Poiché un singolo canale potrebbe avere più di un tipo di contenuto registrato, è necessario verificare tutti i valori possibili anche dopo che è stata trovata una corrispondenza.

Quando l'utente conosce il contenuto di ogni canale, deve essere in grado di regolare il volume o di attivare o disattivare i singoli canali in base alle esigenze. Implementare questa funzionalità nell'applicazione usando la proprietà [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md) .

> [!Note]  
> Per riprodurre i dischi Karaoke, il decodificatore audio nel sistema dell'utente deve essere compatibile con l'implementazione del karaoke DirectShow 8.

 

 

 



