---
description: La proprietà AudioStreamsAvailable recupera il numero di flussi audio disponibili nel titolo corrente.
ms.assetid: 4359ec30-920a-4b34-8e27-4cf1d9452aa8
title: Proprietà AudioStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07025a3a3bf54ad98d32c54ee3c147bc36489822ef451965e1e0e0da8fe586c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586731"
---
# <a name="audiostreamsavailable-property"></a>Proprietà AudioStreamsAvailable

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

La `AudioStreamsAvailable` proprietà recupera il numero di flussi audio disponibili nel titolo corrente.

``` syntax
[ iStreams = ] MSWebDVD.AudioStreamsAvailable
```

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero compreso tra 1 e 8 che rappresenta il numero di flussi audio disponibili nel titolo corrente.

## <a name="remarks"></a>Commenti

Questa proprietà è di sola lettura senza alcun valore predefinito. L'uso principale di più flussi audio è fornire colonne sonore di film in più lingue. In genere, non tutti i titoli di un disco hanno tutti i flussi audio abilitati. Ad esempio, il film potrebbe avere colonne sonore in tre lingue diverse, ma i trailer potrebbero avere solo una colonna sonora inglese. Prima che un utente possa selezionare un flusso, l'applicazione deve determinare quali flussi sono disponibili all'interno del titolo corrente. Si noti che flussi specifici sono identificati da un indice da zero a 7.

I dischi presentano in genere un menu che mostra le colonne sonore disponibili, consentendo all'utente di selezionare il flusso audio da abilitare.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetAudioLanguage**](getaudiolanguage-method.md)
</dt> </dl>

 

 



