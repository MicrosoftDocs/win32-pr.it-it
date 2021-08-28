---
title: Elemento ServiceTask3
description: Nota Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di uno store online non è supportato. L'elemento ServiceTask3 rappresenta il terzo riquadro attività dello store online.
ms.assetid: 3d08f9ff-d75b-4967-90f8-23ab71d38883
keywords:
- Elemento ServiceTask3 Windows Media Player
topic_type:
- apiref
api_name:
- ServiceTask3 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0c53ef9eb4a758e47d639446750465934fb4a6c031d8abd387276add2f0df519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763631"
---
# <a name="servicetask3-element"></a>Elemento ServiceTask3

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di uno store online non è supportato.

 

**L'elemento ServiceTask3** rappresenta il terzo riquadro attività dello store online.

``` syntax
<ServiceTask3
    URL = "URL"
/>
```

## <a name="attributes"></a>Attributi



| Termine                                                                                                                             | Descrizione                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obbligatorio)<br/> | URL per la pagina Web Windows Media Player visualizzata.<br/> |



 

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento                       |
|-----------------|-------------------------------|
| Elementi padre | **ServiceInfo**               |
| Elementi figlio  | **ButtonText**, **ButtonTip** |



 

## <a name="remarks"></a>Commenti

**ServiceTask1 è** considerato il riquadro attività principale per l'attività commerciale. È il riquadro attività che viene visualizzato quando l'utente sceglie di acquistare musica. Usare **ServiceTask3 per** altre attività di negozio online.

> [!Note]  
> Windows Media Player 10 include tre riquadri attività in cui un negozio online può visualizzare le pagine Web. Lo store online può scegliere di usare uno, due o tutti e tre i riquadri attività. Windows Media Player 11 ha un solo riquadro attività, che l'utente  può visualizzare facendo clic sulla scheda Negozi online. Windows Media Player 11 ignora gli elementi **ServiceTask2** e **ServiceTask3.**

 

I riquadri attività degli archivi online condividono una singola istanza del browser. Ciò significa che non è consigliabile scrivere codice script nella pagina Web che si prevede di continuare a eseguire quando l'utente si allontana dall'attività del servizio corrente.

Quando l'utente passa da un riquadro attività all'altro, Windows Media Player l'URL e i cookie di sessione. Quando l'utente torna al riquadro attività, player ripristina l'URL e i cookie. Se l'utente sceglie di usare un archivio online diverso, i dati dell'URL e della sessione vengono cancellati.

La tabella seguente contiene informazioni dettagliate sui parametri inviati con la richiesta URL.



| Nome         | Valore                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Geoid*      | Windows'ID della posizione geografica. L'ID località viene specificato dall'utente nell'area **Località** delle impostazioni Opzioni internazionali e della lingua Pannello di controllo. |
| *locale*     | Windows Media Player ID delle impostazioni locali.                                                                                                                                     |
| *userlocale* | Windows ID delle impostazioni locali. Le impostazioni locali vengono specificate dall'utente nell'area **Standard** e formati delle impostazioni Opzioni internazionali e della lingua Pannello di controllo.        |
| *version*    | Windows Media Player numero di versione usando il formato seguente: 10.0.x.xxxx o 11.0.x.xxxx.                                                                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Documento ServiceInfo di esempio per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo di esempio per uno store online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





