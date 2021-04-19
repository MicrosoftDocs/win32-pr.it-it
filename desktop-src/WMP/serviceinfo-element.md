---
title: Elemento ServiceInfo
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. L'elemento ServiceInfo è l'elemento principale per il documento ServiceInfo.xml.
ms.assetid: d2f9e642-143e-405d-8588-c78e4355b9b9
keywords:
- Finestra elementi ServiceInfo Media Player
topic_type:
- apiref
api_name:
- ServiceInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ac41edd4ae8548ecdb6d3ef6631fba5d6175762
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328112"
---
# <a name="serviceinfo-element"></a>Elemento ServiceInfo

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'elemento **ServiceInfo** è l'elemento principale per il documento ServiceInfo.xml.

``` syntax
<ServiceInfo
    Version = 1.00
    Key = "service key"
    ContentPartner = "true|false"
/>
```

## <a name="attributes"></a>Attributi



| Termine                                                                                                                                             | Descrizione                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Versione** (facoltativa)<br/> | Versione del file di ServiceInfo.xml. La versione 1,00 è supportata per Windows Media Player.<br/>                                                                                                                                                            |
| <span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Chiave** (obbligatoria)<br/>                 | Stringa della chiave del servizio che identifica in modo univoco l'archivio online.<br/>                                                                                                                                                                                   |
| <span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**ContentPartner**<br/>                 | Indica se l'archivio online è un archivio di tipo 1. Il valore "true" indica che l'archivio è di tipo 1. Il valore "false" indica che l'archivio non è un archivio di tipo 1; ovvero, è un archivio di tipo 2. Il valore predefinito è "false".<br/> |



 

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento                                                                                                                                                                            |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementi padre | nessuno                                                                                                                                                                               |
| Elementi figlio  | **AlbumInfo**, **BuyCD**, **color**, **Description**, **FriendlyName**, **HtmlView**, **Image**, **centro** informazioni, **Install**, **ServiceTask1**, **ServiceTask2**, **ServiceTask3** |



 

## <a name="remarks"></a>Commenti

La tabella seguente illustra in dettaglio i parametri inviati con la richiesta URL. Altri possono essere presenti per motivi di compatibilità con le versioni precedenti. La richiesta includerà anche tutti i parametri specificati usando il parametro della riga di comando ServiceExtra del programma di installazione di Windows Media Player.



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

 

 





