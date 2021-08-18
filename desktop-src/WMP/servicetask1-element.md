---
title: Elemento ServiceTask1
description: Nota Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato. L'elemento ServiceTask1 rappresenta il primo riquadro attività del negozio online.
ms.assetid: 39b149ae-ea67-4fba-812b-15a97044fcd8
keywords:
- Elemento ServiceTask1 Windows Media Player
topic_type:
- apiref
api_name:
- ServiceTask1 Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2fc22e01329728935e2953b5be7a3a1042cee00da3a3b9756915de2aeafe9b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995411"
---
# <a name="servicetask1-element"></a>Elemento ServiceTask1

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

**L'elemento ServiceTask1** rappresenta il primo riquadro attività del negozio online.

``` syntax
<ServiceTask1
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

**ServiceTask1 è** considerato il riquadro attività principale per l'attività commerciale. È il riquadro attività che viene visualizzato quando l'utente sceglie di acquistare musica.

> [!Note]  
> Windows Media Player 10 include tre riquadri attività in cui un negozio online può visualizzare le pagine Web. Lo Store online può scegliere di usare uno, due o tutti e tre i riquadri attività. Windows Media Player 11 ha un solo riquadro attività, rappresentato da **ServiceTask1,** che l'utente può visualizzare facendo clic sulla **scheda Negozi** online.

 

I riquadri attività del negozio online condividono una singola istanza del browser. Ciò significa che non è consigliabile scrivere codice script nella pagina Web che si prevede di continuare a eseguire quando l'utente si allontana dall'attività del servizio corrente.

Quando l'utente cambia riquadro attività, Windows Media Player l'URL e i cookie di sessione. Quando l'utente torna al riquadro attività, Player ripristina l'URL e i cookie. Se l'utente sceglie di usare un negozio online diverso, l'URL e i dati della sessione vengono cancellati.

Nella tabella seguente sono riportati i dettagli dei parametri inviati con la richiesta URL. Altri possono essere presenti per motivi di compatibilità legacy.



| Nome         | Valore                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Geoid*      | Windows ID località geografica. L'ID località viene specificato dall'utente nell'area **Località** delle impostazioni opzioni internazionali e della lingua in Pannello di controllo. |
| *locale*     | Windows Media Player ID impostazioni locali.                                                                                                                                     |
| *userlocale* | Windows ID impostazioni locali. Le impostazioni locali vengono specificate dall'utente nell'area **Standard** e formati delle impostazioni opzioni internazionali e della lingua Pannello di controllo.        |
| *version*    | Windows Media Player numero di versione usando il formato seguente: 10.0.x.xxxx o 11.0.x.xxxx.                                                                         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva.<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Esempio di documento ServiceInfo per un negozio online di tipo 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Esempio di documento ServiceInfo per un negozio online di tipo 2**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





