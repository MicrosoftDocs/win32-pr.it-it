---
title: Proprietà baseURL di IWMPSettings
description: La proprietà baseURL Ottiene o imposta l'URL di base usato per la risoluzione del percorso relativo con i comandi script URL incorporati nel contenuto multimediale digitale.
ms.assetid: e136303f-ba08-434f-ad7e-9fffa66785c4
keywords:
- Finestra delle proprietà di baseURL Media Player
- Proprietà di baseURL Media Player Windows, interfaccia IWMPSettings
- Interfaccia IWMPSettings Windows Media Player, proprietà baseURL
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
ms.openlocfilehash: 393575a93bf904f6fe312b13647ad5a7557b15bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324362"
---
# <a name="iwmpsettingsbaseurl-property"></a>Proprietà IWMPSettings:: baseURL

La proprietà **BaseUrl** Ottiene o imposta l'URL di base usato per la risoluzione del percorso relativo con i comandi script URL incorporati nel contenuto multimediale digitale.

## <a name="syntax"></a>Sintassi


```CSharp
public System.String baseURL {get; set;}
```


```VB

Public Property baseURL As System.String
```





## <a name="property-value"></a>Valore proprietà

**System. String** che rappresenta l'URL di base.

## <a name="remarks"></a>Commenti

Questa proprietà specifica l'URL HTTP di base che viene passato come parametro Command dall'evento **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** . L'URL di base viene concatenato all'URL relativo, come indicato di seguito:

1.  Viene aggiunta una barra (/) finale al valore recuperato dalla proprietà **BaseUrl** .
2.  Un punto principale, una barra rovesciata o un carattere barra rovesciata (., \\ e/) viene eliminato dall'URL relativo.
3.  L'URL relativo viene aggiunto alla fine dell'URL di base.
4.  Tutti i caratteri della barra nell'URL completo risultante vengono puntati nella stessa direzione (convertiti in avanti o in barra rovesciata) in base alla direzione del primo carattere barra rilevato nel nuovo URL.

**Nota**

Il controllo Media Player di Windows non supporta l'utilizzo di due punti (..) nell'URL relativo per indicare l'elemento padre della posizione corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versione<br/>   | Windows Media Player 9 serie o versione successiva<br/>                                                                      |
| Spazio dei nomi<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Evento AxWindowsMediaPlayer. ScriptCommand (VB e C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Interfaccia IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





