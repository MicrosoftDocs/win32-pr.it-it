---
title: Metodo External.play
description: Nota In questo argomento vengono descritte le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato. Il metodo play indica Windows Media Player riprodurre un set di elementi multimediali.
ms.assetid: 3e1f45db-9e7f-4a1b-aaa2-513a19c46f70
keywords:
- Metodo play Windows Media Player
- metodo play Windows Media Player , classe external
- Classe esterna Windows Media Player, metodo play
topic_type:
- apiref
api_name:
- External.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90644b357e56f40bfbdb576908b99aa6941f8153dc339daa996152f63d77372c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648631"
---
# <a name="externalplay-method"></a>Metodo External.play

> [!Note]  
> Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità all'esterno del contesto di un negozio online non è supportato.

 

Il **metodo play** indica Windows Media Player riprodurre un set di elementi multimediali.

## <a name="syntax"></a>Sintassi


```JScript
External.play(
  LibraryLocationType,
  LibraryLocationIDs
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LibraryLocationType* \[ Pollici\]
</dt> <dd>

Costante [di posizione della](library-location-constants.md) libreria che specifica il tipo di elementi multimediali da riprodurre. Ad esempio, CPAlbumID specifica che devono essere riprodotti uno o più album.

</dd> <dt>

*LibraryLocationIDs* \[ Pollici\]
</dt> <dd>

**Stringa** contenente gli identificatori, delimitati da punti e virgola, degli elementi multimediali da riprodurre.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





