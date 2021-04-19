---
title: THEME. showErrorDialog
description: Il metodo showErrorDialog Visualizza la finestra di dialogo di errore standard.
ms.assetid: cec9ecfd-6665-4b0a-a09c-49120d557a80
keywords:
- THEME. showErrorDialog Windows Media Player
topic_type:
- apiref
api_name:
- THEME.showErrorDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cdc1f9df13ec460ce780507e1bde38a2996f915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328387"
---
# <a name="themeshowerrordialog"></a>THEME. showErrorDialog

Il metodo **showErrorDialog** Visualizza la finestra di dialogo di errore standard.

``` syntax
        theme.showErrorDialog()
```

## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se **Settings. enableErrorDialogs** è false, questo metodo può essere utilizzato per visualizzare la finestra di dialogo di errore a livello di codice. Se non sono presenti errori nella coda degli errori, la finestra di dialogo di errore non viene visualizzata.

Per Windows Media Player 9 serie o versioni successive, questo metodo deve essere chiamato dal gestore eventi di errore. Windows Media Player 9 Series o versioni successive Cancella la coda degli errori per le interfacce dopo che è stato generato l'evento di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> <dt>

[**Settings. enableErrorDialogs**](settings-enableerrordialogs.md)
</dt> </dl>

 

 





