---
title: External. NavigateTaskPaneURL, metodo
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. NavigateTaskPaneURL, metodo
ms.assetid: c3a888c0-6589-4d21-9d47-37372d9069f4
keywords:
- Metodo NavigateTaskPaneURL Windows Media Player
- Metodo NavigateTaskPaneURL Windows Media Player, classe esterna
- Classe esterna Media Player Windows, metodo NavigateTaskPaneURL
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
ms.openlocfilehash: 8e70558c7616738f67d9dc1d6d29eca15e5c30d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324562"
---
# <a name="externalnavigatetaskpaneurl-method"></a>External. NavigateTaskPaneURL, metodo

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Il metodo **NavigateTaskPaneURL** apre una pagina Web nel riquadro attività specificato e sposta lo stato attivo sul riquadro specificato.

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

*bstrKeyName* \[ in\]
</dt> <dd>

**Stringa** contenente il nome della chiave per l'archivio online. (obbligatorio)

</dd> <dt>

*bstrTaskPane* \[ in\]
</dt> <dd>

**Stringa** contenente il nome del riquadro attività in cui viene visualizzata la pagina Web. (obbligatorio)

</dd> <dt>

*bstrParams* \[ in\]
</dt> <dd>

**Stringa** contenente i parametri della stringa di query da accodare all'URL specificato dall'elemento **Navigate** del documento ServiceInfo. (facoltativo).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se si passa a un riquadro non supportato dall'archivio online, è possibile che si verifichi la modifica dell'archivio online corrente.

Il valore specificato per *bstrParams* è valido solo quando **NavigateTaskPaneURL** viene chiamato da pagine Web fornite dal negozio online.

Nella tabella seguente sono elencati i valori validi per *bstrTaskPane* e il riquadro attività associato per ciascuno di essi.



| Valore            | Riquadro attività                      |
|------------------|--------------------------------|
| **ServiceTask1** | Primo riquadro attività negozio online.  |
| **ServiceTask2** | Secondo riquadro attività archivio online. |
| **ServiceTask3** | Terzo riquadro attività negozio online.  |



 

Il codice della pagina Web deve specificare un valore per [External. SelectedTaskPane](external-selectedtaskpane.md) durante il caricamento per assicurarsi che il pulsante corretto del riquadro attività venga evidenziato dopo il completamento dello spostamento.

## <a name="examples"></a>Esempio

Il codice di esempio seguente mostra come **NavigateTaskPaneURL** crea l'URL della pagina Web da visualizzare per **ServiceTask1**.

Esempio dell'elemento **Navigate** :


```XML
<Navigate
    BaseURL = "https://www.proseware.com/online store/html/navigate.asp">
</Navigate>
```



Chiamata di esempio al metodo **NavigateTaskPaneURL** :


```XML
external.NavigateTaskPaneURL("Proseware", "ServiceTask1", "Pane=Store");
```



Esempio di URL risultante usato per la pagina Web visualizzata in **ServiceTask1**:


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

[**Oggetto esterno per i negozi di tipo 2 online**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**External. SelectedTaskPane**](external-selectedtaskpane.md)
</dt> </dl>

 

 





