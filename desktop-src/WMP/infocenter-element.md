---
title: Elemento InfoCenter
description: Nota Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. | Elemento InfoCenter
ms.assetid: 1a9cc513-5dd1-46d8-9409-16413695b4c8
keywords:
- Elemento InfoCenter Windows Media Player
topic_type:
- apiref
api_name:
- InfoCenter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1d89e7a35d0d9daacd87d3ac840f0ee87fa7c82b317afd54c9283344e204f8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118576260"
---
# <a name="infocenter-element"></a>Elemento InfoCenter

> [!Note]  
> Questa sezione descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di uno store online non è supportato.

 

**L'elemento InfoCenter** specifica l'URL della pagina Web Windows Media Player visualizzata nella  funzionalità Visualizzazione Info Center di Riproduzione in esecuzione quando lo store online è attivo.

``` syntax
<InfoCenter
    URL = "URL"
/>
```

## <a name="attributes"></a>Attributi

<dl> <dt>

<span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obbligatorio)
</dt> <dd>

URL per la pagina Web Windows Media Player visualizzata.

</dd> </dl>

## <a name="parentchild-elements"></a>Elementi padre/figlio



| Gerarchia       | Elemento         |
|-----------------|-----------------|
| Elementi padre | **ServiceInfo** |
| Elementi figlio  | nessuno            |



 

## <a name="remarks"></a>Osservazioni

L'utente controlla quando la visualizzazione Info Center è attiva.

Per recuperare informazioni sull'elemento multimediale attualmente in riproduzione, è necessario incorporare un'istanza del controllo Windows Media Player nella pagina Web e usare il modello a oggetti Player.

La tabella seguente contiene informazioni dettagliate sui parametri inviati con la richiesta URL. Altri possono essere presenti per motivi di compatibilità legacy.



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

 

 





