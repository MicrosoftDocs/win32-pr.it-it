---
description: La proprietà AudioStreamsAvailable Recupera il numero di flussi audio disponibili nel titolo corrente.
ms.assetid: 4359ec30-920a-4b34-8e27-4cf1d9452aa8
title: Proprietà AudioStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb68020b30f4349fcbbb464150624d75250a0dbf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876409"
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

Questa proprietà è di sola lettura e non prevede alcun valore predefinito. L'uso principale di più flussi audio consiste nel fornire colonne di film in più linguaggi. In genere, non tutti i titoli di un disco hanno tutti i flussi audio abilitati. Il film di funzionalità, ad esempio, potrebbe avere Soundtrack in tre lingue diverse, ma i trailer potrebbero avere solo una colonna della lingua inglese. Prima che un utente possa selezionare un flusso, l'applicazione deve determinare quali flussi sono disponibili nel titolo corrente. Si noti che determinati flussi sono identificati da un indice compreso tra 0 e 7.

I dischi di solito presentano un menu che mostra le Soundtrack disponibili, consentendo all'utente di selezionare il flusso audio da abilitare.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetAudioLanguage**](getaudiolanguage-method.md)
</dt> </dl>

 

 



