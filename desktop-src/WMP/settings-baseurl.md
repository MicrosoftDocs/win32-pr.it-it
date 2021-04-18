---
title: Settings. baseURL
description: La proprietà baseURL specifica o recupera l'URL di base usato per la risoluzione del percorso relativo con i comandi script URL incorporati negli elementi multimediali.
ms.assetid: bb2db144-6d1e-4ed6-baed-dc5dbff44aa0
keywords:
- Impostazioni. baseURL Windows Media Player
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
ms.openlocfilehash: ed77d90c8ffadc4dd8da0951f7e6a477db3f9de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325132"
---
# <a name="settingsbaseurl"></a>Settings. baseURL

La proprietà **BaseUrl** specifica o recupera l'URL di base usato per la risoluzione del percorso relativo con i comandi script URL incorporati negli elementi multimediali.

## <a name="syntax"></a>Sintassi

Player. Settings. baseURL

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di lettura/scrittura.

## <a name="remarks"></a>Commenti

Questa proprietà specifica l'URL HTTP di base che viene passato come parametro Command dall'evento **ScriptCommand** . L'URL di base viene concatenato all'URL relativo, come indicato di seguito:

1.  Viene aggiunta una barra (/) finale al valore della proprietà **BaseUrl** .
2.  Un punto, una barra rovesciata o una barra (., \\ e/) iniziali vengono eliminati dall'URL relativo.
3.  L'URL relativo viene aggiunto alla fine dell'URL di base.
4.  Tutte le barre nell'URL completo risultante sono posizionate nella stessa direzione (convertite in avanti o in barre rovesciate) in base alla direzione del primo carattere barra rilevato nel nuovo URL.

**Nota**

Il controllo Player non supporta l'utilizzo di due punti (..) nell'URL relativo per indicare l'elemento padre della posizione corrente.

**Windows Media Player 10 Mobile**: questa proprietà è di sola lettura e restituisce sempre una stringa vuota.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Evento Player. ScriptCommand**](player-player-scriptcommand.md)
</dt> <dt>

[**Oggetto Settings**](settings-object.md)
</dt> </dl>

 

 





