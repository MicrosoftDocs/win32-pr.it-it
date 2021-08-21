---
title: Proprietà baseURL IWMPSettings
description: La proprietà baseURL ottiene o imposta l'URL di base usato per la risoluzione del percorso relativo con comandi di script URL incorporati nel contenuto multimediale digitale.
ms.assetid: e136303f-ba08-434f-ad7e-9fffa66785c4
keywords:
- proprietà baseURL Windows Media Player
- proprietà baseURL Windows Media Player, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player proprietà , baseURL
topic_type:
- apiref
api_name:
- IWMPSettings.baseURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3224a43a2689fd49dee2b2a66cc768250b1a829e61863d8cfbd029e3cdf783c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568419"
---
# <a name="iwmpsettingsbaseurl-property"></a>Proprietà IWMPSettings::baseURL

La **proprietà baseURL** ottiene o imposta l'URL di base usato per la risoluzione del percorso relativo con comandi di script URL incorporati nel contenuto multimediale digitale.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String baseURL {get; set;}
```


```VB

Public Property baseURL As System.String
```





## <a name="property-value"></a>Valore proprietà

Oggetto **System.String** che rappresenta l'URL di base.

## <a name="remarks"></a>Commenti

Questa proprietà specifica l'URL HTTP di base passato come parametro di comando dall'evento **ScriptCommandEvent di AxWindowsMediaPlayer \_ WMPOCXEvents. \_** L'URL di base viene concatenato con l'URL relativo come segue:

1.  Al valore recuperato dalla proprietà **baseURL** viene aggiunta una barra finale (/).
2.  Un punto iniziale, una barra all'indietro o una barra (., e /) viene \\ eliminato dall'URL relativo.
3.  L'URL relativo viene aggiunto alla fine dell'URL di base.
4.  Tutti i caratteri barra nell'URL completo risultante sono puntati nella stessa direzione (convertiti in barre avanti o indietro) in base alla direzione del primo carattere barra rilevato nel nuovo URL.

**Nota**

Il Windows Media Player controllo non supporta l'uso di due punti (..) nell'URL relativo per indicare l'elemento padre della posizione corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player serie 9 o successive<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Evento AxWindowsMediaPlayer.ScriptCommand (VB e C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





