---
description: Il metodo GetKaraokeChannelContent recupera un valore che indica il tipo di contenuto nel canale specificato nel flusso specificato.
ms.assetid: e36a88b8-7184-44a4-8e02-204440f651bc
title: Metodo GetKaraokeChannelContent
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef0353ebda6469627b5f41209b780fc1403c51940705be72d6acaa139d8320f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812491"
---
# <a name="getkaraokechannelcontent-method"></a>Metodo GetKaraokeChannelContent

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il metodo recupera un valore che indica il tipo di contenuto `GetKaraokeChannelContent` nel canale specificato nel flusso specificato.

``` syntax
[ iContent = ] MSWebDVD.GetKaraokeChannelContent(iStream, iChannel)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Specifica il flusso audio come integer.

</dd> <dt>

<span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*Ichannel*
</dt> <dd>

Specifica il canale come integer. I valori possibili per ogni canale sono:



| Valore  | Descrizione    |
|--------|----------------|
| 0x0001 | Guide 1  |
| 0x0002 | Guide 2  |
| 0x0004 | Guide 1 |
| 0x0008 | Guide 2 |
| 0x0010 | Guida A |
| 0x0020 | Guida B |
| 0x0040 | Effetto sonoro A |
| 0x0080 | Effetto audio B |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero i cui singoli bit specificano il contenuto del canale del canale.

## <a name="remarks"></a>Commenti

La numerazione dei canali audio DVD è in base zero, quindi i canali 2, 3 e 4 sono i canali ausiliari. Dopo la fine del metodo, eseguire un'operazione AND bit per bit su *iContent* per determinare il contenuto di ogni canale. Poiché in un singolo canale possono essere registrati più tipi di contenuto, è consigliabile verificare tutti i valori possibili anche dopo aver trovato una corrispondenza.

Quando l'utente conosce il contenuto di ogni canale, deve essere in grado di regolare il volume o di attivare o disattivare i singoli canali in base alle esigenze. Implementare questa funzionalità nell'applicazione usando la [**proprietà TemaAudioPresentationMode.**](karaokeaudiopresentationmode-property.md)

> [!Note]  
> Per riprodurre i dischi, il decodificatore audio nel sistema dell'utente deve essere compatibile con l'implementazione DirectShow 8.

 

 

 



