---
title: External. saveCurrentViewToLibrary, metodo
description: Il metodo saveCurrentViewToLibrary crea una playlist dagli elementi multimediali nella visualizzazione corrente e salva la playlist nella libreria locale.
ms.assetid: cd87e932-d599-4298-bbee-6755999dda15
keywords:
- Metodo saveCurrentViewToLibrary Windows Media Player
- Metodo saveCurrentViewToLibrary Windows Media Player, classe esterna
- Classe esterna Media Player Windows, metodo saveCurrentViewToLibrary
topic_type:
- apiref
api_name:
- External.saveCurrentViewToLibrary
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 212f590f03c32821c0774c4898720c92558ecc73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324546"
---
# <a name="externalsavecurrentviewtolibrary-method"></a>External. saveCurrentViewToLibrary, metodo

Il metodo **saveCurrentViewToLibrary** crea una playlist dagli elementi multimediali nella visualizzazione corrente e salva la playlist nella libreria locale.

## <a name="syntax"></a>Sintassi


```JScript
External.saveCurrentViewToLibrary(
  FriendlyListName,
  Local
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FriendlyListName* \[ in\]
</dt> <dd>

**Stringa** che specifica un nome descrittivo per la playlist. Windows Media Player Visualizza questo nome nella relativa interfaccia utente.

</dd> <dt>

*Locale* \[ in\]
</dt> <dd>

**Valore booleano** che specifica se la playlist è dinamica o statica. **True** specifica Dynamic e **false** specifica static.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





