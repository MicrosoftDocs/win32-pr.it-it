---
title: Elemento ButtonText
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. | Elemento ButtonText
ms.assetid: 1afe1626-769a-40c8-883a-968ebd995a93
keywords:
- Finestra elementi ButtonText Media Player
topic_type:
- apiref
api_name:
- ButtonText Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c94577ad772a5c6fa198bd43f2475d53821da72c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333855"
---
# <a name="buttontext-element"></a>Elemento ButtonText

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'elemento **ButtonText** specifica la stringa di testo visualizzata da Windows Media Player per un pulsante del riquadro attività.

``` syntax
<ButtonText>
   text string
</ButtonText>
```

## <a name="attributes"></a>Attributi

Questo elemento non ha attributi.

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento                                              |
|-----------------|------------------------------------------------------|
| Elementi padre | **ServiceTask1**, **ServiceTask2**, **ServiceTask3** |
| Elementi figlio  | nessuno                                                 |



 

## <a name="remarks"></a>Osservazioni

Questo elemento è obbligatorio per ogni istanza di **ServiceTask1**, **ServiceTask2** o **ServiceTask3**.

> [!Note]  
> Windows Media Player 10 include tre riquadri attività in cui un negozio online può visualizzare le pagine Web. Lo Store online può scegliere di usare uno, due o tutti e tre i riquadri attività. Windows Media Player 11 dispone di un solo riquadro attività, che l'utente può visualizzare facendo clic sulla scheda **Store online** . Windows Media Player 11 ignora gli elementi **ServiceTask2** e **ServiceTask3** .

 

Windows Media Player possibile ritagliare il testo del pulsante per adattarlo allo spazio disponibile. Il lettore usa sempre il tipo di carattere Tahoma grassetto a 8 punti per questo testo. Sono disponibili due righe per visualizzare il testo del pulsante, ma il lettore non esegue automaticamente il wrapping del testo dalla prima riga al secondo. Per specificare un'interruzioni di riga nel testo del pulsante, inserire la nuova sequenza di escape di riga " \\ n" nella stringa di testo.

La stringa di testo viene visualizzata anche nel menu **Vai** nell'interfaccia utente di Windows Media Player.

È necessario testare il negozio online usando un'ampia gamma di impostazioni di visualizzazione per garantire che il testo venga visualizzato come previsto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





