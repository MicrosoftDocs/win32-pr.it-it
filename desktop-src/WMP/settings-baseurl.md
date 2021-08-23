---
title: Impostazioni.baseURL
description: La proprietà baseURL specifica o recupera l'URL di base usato per la risoluzione del percorso relativo con comandi script URL incorporati negli elementi multimediali.
ms.assetid: bb2db144-6d1e-4ed6-baed-dc5dbff44aa0
keywords:
- Impostazioni.baseURL Windows Media Player
topic_type:
- apiref
api_name:
- Settings.baseURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69e06275a3028df6b90d25665e11aab3c2a0961dfa6c525cde0636434f06986b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995381"
---
# <a name="settingsbaseurl"></a>Impostazioni.baseURL

La **proprietà baseURL** specifica o recupera l'URL di base usato per la risoluzione del percorso relativo con comandi di script URL incorporati negli elementi multimediali.

## <a name="syntax"></a>Sintassi

player.settings.baseURL

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di **lettura/scrittura.**

## <a name="remarks"></a>Commenti

Questa proprietà specifica l'URL HTTP di base passato come parametro di comando **dall'evento ScriptCommand.** L'URL di base viene concatenato all'URL relativo come segue:

1.  Al valore della proprietà **baseURL** viene aggiunta una barra finale (/).
2.  Un punto iniziale, una barra all'indietro o una barra (., e /) vengono \\ eliminati dall'URL relativo.
3.  L'URL relativo viene aggiunto alla fine dell'URL di base.
4.  Tutte le barre nell'URL completo risultante sono puntate nella stessa direzione (convertite in barre avanti o indietro) in base alla direzione del primo carattere barra rilevato nel nuovo URL.

**Nota**

Il controllo lettore non supporta l'uso di due punti (..) nell'URL relativo per indicare l'elemento padre della posizione corrente.

**Windows Media Player 10 Mobile:** questa proprietà è di sola lettura e restituisce sempre una stringa vuota.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Evento Player.ScriptCommand**](player-player-scriptcommand.md)
</dt> <dt>

[**Impostazioni Oggetto**](settings-object.md)
</dt> </dl>

 

 





