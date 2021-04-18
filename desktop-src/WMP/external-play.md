---
title: Metodo External. Play
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo Play indica a Windows Media Player di riprodurre un set di elementi multimediali.
ms.assetid: 3e1f45db-9e7f-4a1b-aaa2-513a19c46f70
keywords:
- Metodo di riproduzione Media Player Windows
- Metodo Play Media Player Windows, classe esterna
- Classe esterna Media Player Windows, metodo Play
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
ms.openlocfilehash: 94cfa40d96bbc67c7d41eb1a1a0188be68ec154e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324550"
---
# <a name="externalplay-method"></a>Metodo External. Play

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Il metodo **Play** indica a Windows Media Player di riprodurre un set di elementi multimediali.

## <a name="syntax"></a>Sintassi


```JScript
External.play(
  LibraryLocationType,
  LibraryLocationIDs
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LibraryLocationType* \[ in\]
</dt> <dd>

[Costante del percorso della libreria](library-location-constants.md) che specifica il tipo degli elementi multimediali da riprodurre. Ad esempio, CPAlbumID specifica che uno o più album devono essere riprodotti.

</dd> <dt>

*LibraryLocationIDs* \[ in\]
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

[**Oggetto esterno per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





