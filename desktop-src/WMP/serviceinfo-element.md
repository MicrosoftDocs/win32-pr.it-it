---
title: Elemento ServiceInfo
description: Nota Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato. L'elemento ServiceInfo è l'elemento principale per il ServiceInfo.xml documento.
ms.assetid: d2f9e642-143e-405d-8588-c78e4355b9b9
keywords:
- Elemento ServiceInfo Windows Media Player
topic_type:
- apiref
api_name:
- ServiceInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b3be774d019555daa75b78edf6a7ed76351e7523712313365dd6c80bfee7cd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763641"
---
# <a name="serviceinfo-element"></a>Elemento ServiceInfo

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

**L'elemento ServiceInfo** è l'elemento principale per il ServiceInfo.xml documento.

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
| <span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Versione** (facoltativo)<br/> | Versione del file ServiceInfo.xml. La versione 1.00 è supportata per Windows Media Player.<br/>                                                                                                                                                            |
| <span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Chiave** (obbligatorio)<br/>                 | Stringa della chiave del servizio che identifica in modo univoco il negozio online.<br/>                                                                                                                                                                                   |
| <span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**ContentPartner**<br/>                 | Indica se il negozio online è di tipo 1. Il valore "true" indica che l'archivio è di tipo 1. Il valore "false" indica che l'archivio non è un archivio di tipo 1. si tratta di un archivio di tipo 2. Il valore predefinito è "false".<br/> |



 

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento                                                                                                                                                                            |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementi padre | Nessuno                                                                                                                                                                               |
| Elementi figlio  | **AlbumInfo,** **BuyCD,** **Color,** **Description,** **FriendlyName,** **HTMLView,** **Image,** **InfoCenter,** **Install,** **ServiceTask1,** **ServiceTask2,** **ServiceTask3** |



 

## <a name="remarks"></a>Commenti

Nella tabella seguente sono riportati i dettagli dei parametri inviati con la richiesta URL. Altri possono essere presenti per motivi di compatibilità legacy. La richiesta includerà anche tutti i parametri specificati usando il parametro della riga di comando ServiceExtra Windows Media Player configurazione.



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

 

 





