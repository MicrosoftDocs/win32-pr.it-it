---
title: Metodo External.NavigateTaskPaneURL
description: Nota Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. | Metodo External.NavigateTaskPaneURL
ms.assetid: c3a888c0-6589-4d21-9d47-37372d9069f4
keywords:
- Metodo NavigateTaskPaneURL Windows Media Player
- Metodo NavigateTaskPaneURL Windows Media Player , classe External
- Classe esterna Windows Media Player, metodo NavigateTaskPaneURL
topic_type:
- apiref
api_name:
- External.NavigateTaskPaneURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eebcf8d799452a9966355f644f00ac5c4aecc4c066374254e8e580431b756b92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649031"
---
# <a name="externalnavigatetaskpaneurl-method"></a>Metodo External.NavigateTaskPaneURL

> [!Note]  
> In questo argomento vengono descritte le funzionalità progettate per l'utilizzo da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di uno store online non è supportato.

 

Il **metodo NavigateTaskPaneURL** apre una pagina Web nel riquadro attività specificato e passa lo stato attivo al riquadro specificato.

## <a name="syntax"></a>Sintassi


```JScript
External.NavigateTaskPaneURL(
  bstrKeyName,
  bstrTaskPane,
  bstrParams
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrKeyName* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il nome della chiave per lo store online. (obbligatorio)

</dd> <dt>

*bstrTaskPane* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il nome del riquadro attività in cui si apre la pagina Web. (obbligatorio)

</dd> <dt>

*bstrParams* \[ Pollici\]
</dt> <dd>

**Stringa** contenente i parametri della stringa di query da aggiungere all'URL specificato **dall'elemento Navigate** del documento ServiceInfo. (facoltativo).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il passaggio a un riquadro non supportati dal negozio online può causare la modifica dello store online corrente.

Il valore specificato per *bstrParams* è valido solo quando **NavigateTaskPaneURL** viene chiamato dalle pagine Web fornite dallo store online.

Nella tabella seguente sono elencati i valori validi per *bstrTaskPane* e il riquadro attività associato per ognuno.



| Valore            | Riquadro attività                      |
|------------------|--------------------------------|
| **Attività Servizio1** | Riquadro attività Primo negozio online.  |
| **Attività Servizio2** | Secondo riquadro attività dello store online. |
| **Attività Servizio3** | Terzo riquadro attività dello store online.  |



 

Il codice della pagina Web deve specificare un valore per [External.SelectedTaskPane](external-selectedtaskpane.md) durante il caricamento per assicurarsi che il pulsante del riquadro attività corretto sia evidenziato al termine della navigazione.

## <a name="examples"></a>Esempio

Il codice di esempio seguente mostra come **NavigateTaskPaneURL crea** l'URL della pagina Web da visualizzare per **ServiceTask1.**

Esempio **dell'elemento Navigate:**


```XML
<Navigate
    BaseURL = "https://www.proseware.com/online store/html/navigate.asp">
</Navigate>
```



Chiamata di esempio al **metodo NavigateTaskPaneURL:**


```XML
external.NavigateTaskPaneURL("Proseware", "ServiceTask1", "Pane=Store");
```



Esempio di URL risultante usato per la pagina Web visualizzata in **ServiceTask1:**


```XML
https://www.proseware.com/online store/html/navigate.asp?Pane=Store
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 10 o versione successiva<br/>                                        |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per negozi online di tipo 2**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**External.SelectedTaskPane**](external-selectedtaskpane.md)
</dt> </dl>

 

 





