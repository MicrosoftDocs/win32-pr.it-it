---
title: Elemento ServiceTask3
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. L'elemento ServiceTask3 rappresenta il terzo riquadro attività negozio online.
ms.assetid: 3d08f9ff-d75b-4967-90f8-23ab71d38883
keywords:
- Finestra elementi ServiceTask3 Media Player
topic_type:
- apiref
api_name:
- ServiceTask3 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d78b9e70c7e6933693f4d29750e9e3c0b4e897a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333107"
---
# <a name="servicetask3-element"></a>Elemento ServiceTask3

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'elemento **ServiceTask3** rappresenta il terzo riquadro attività negozio online.

``` syntax
<ServiceTask3
    URL = "URL"
/>
```

## <a name="attributes"></a>Attributi



| Termine                                                                                                                             | Descrizione                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obbligatorio)<br/> | URL per la pagina Web visualizzata da Windows Media Player.<br/> |



 

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento                       |
|-----------------|-------------------------------|
| Elementi padre | **ServiceInfo**               |
| Elementi figlio  | **ButtonText**, **ButtonTip** |



 

## <a name="remarks"></a>Commenti

**ServiceTask1** viene considerato il riquadro attività principale per coinvolgere le attività commerciali. Si tratta del riquadro attività visualizzato quando l'utente sceglie di acquistare musica. Usare **ServiceTask3** per altre attività di archivio online.

> [!Note]  
> Windows Media Player 10 include tre riquadri attività in cui un negozio online può visualizzare le pagine Web. Lo Store online può scegliere di usare uno, due o tutti e tre i riquadri attività. Windows Media Player 11 dispone di un solo riquadro attività, che l'utente può visualizzare facendo clic sulla scheda **Store online** . Windows Media Player 11 ignora gli elementi **ServiceTask2** e **ServiceTask3** .

 

I riquadri attività negozi online condividono una singola istanza del browser. Ciò significa che non è necessario scrivere codice di script nella pagina Web che si prevede di continuare a eseguire quando l'utente passa dall'attività del servizio corrente.

Quando l'utente passa i riquadri attività, Windows Media Player archivia i cookie di sessione e l'URL. Quando l'utente torna al riquadro attività, il lettore ripristina l'URL e i cookie. Se l'utente sceglie di usare un archivio online diverso, i dati dell'URL e della sessione vengono cancellati.

La tabella seguente illustra in dettaglio i parametri inviati con la richiesta URL.



| Nome         | Valore                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Geoid*      | ID della posizione geografica di Windows. L'ID percorso viene specificato dall'utente nell'area **località** delle impostazioni Opzioni internazionali e della lingua nel pannello di controllo. |
| *locale*     | Windows Media Player ID impostazioni locali.                                                                                                                                     |
| *UserLocale* | ID delle impostazioni locali di Windows. Le impostazioni locali vengono specificate dall'utente nell'area **standard e formati** delle impostazioni Opzioni internazionali e della lingua nel pannello di controllo.        |
| *version*    | Il numero di versione di Windows Media Player usando il formato seguente: 10.0. x. xxxx o 11.0. x. xxxx.                                                                         |



 

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

 

 





