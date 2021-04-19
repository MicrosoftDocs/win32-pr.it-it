---
title: Elemento centro informazioni
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. | Elemento centro informazioni
ms.assetid: 1a9cc513-5dd1-46d8-9409-16413695b4c8
keywords:
- Finestra degli elementi del centro informazioni Media Player
topic_type:
- apiref
api_name:
- InfoCenter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef62e0f6b41090642400a7f0a8b88af72818da4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325447"
---
# <a name="infocenter-element"></a>Elemento centro informazioni

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L' **elemento centro** informazioni consente di specificare l'URL della pagina Web visualizzata da Windows Media Player nella funzionalità di visualizzazione del centro informazioni per la **riproduzione** quando lo Store online è attivo.

``` syntax
<InfoCenter
    URL = "URL"
/>
```

## <a name="attributes"></a>Attributi

<dl> <dt>

<span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obbligatorio)
</dt> <dd>

URL per la pagina Web visualizzata da Windows Media Player.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento         |
|-----------------|-----------------|
| Elementi padre | **ServiceInfo** |
| Elementi figlio  | nessuno            |



 

## <a name="remarks"></a>Osservazioni

L'utente controlla quando la visualizzazione Info Center è attiva.

Per recuperare informazioni sull'elemento multimediale attualmente in riproduzione, è necessario incorporare un'istanza di Windows Media Player Control nella pagina Web e utilizzare il modello a oggetti del lettore.

La tabella seguente illustra in dettaglio i parametri inviati con la richiesta URL. Altri possono essere presenti per motivi di compatibilità con le versioni precedenti.



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

 

 





