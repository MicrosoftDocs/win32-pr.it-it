---
title: Impostazioni.mediaAccessRights
description: La proprietà mediaAccessRights recupera un valore che indica i diritti attualmente concessi per l'accesso alla libreria.
ms.assetid: 744e696d-29d2-44b1-a296-5b5d007b689f
keywords:
- Impostazioni.mediaAccessRights Windows Media Player
topic_type:
- apiref
api_name:
- Settings.mediaAccessRights
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b78543adcdc36958c6fb2f8e4ea191156bd8c600112e4bd6e5d6e6f5427974
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117933661"
---
# <a name="settingsmediaaccessrights"></a>Impostazioni.mediaAccessRights

La **proprietà mediaAccessRights** recupera un valore che indica i diritti attualmente concessi per l'accesso alla libreria.

## <a name="syntax"></a>Sintassi

player.settings.mediaAccessRights

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di sola **lettura.**



| Valore | Descrizione                      |
|-------|----------------------------------|
| Nessuno  | Diritti di accesso all'elemento corrente. |
| lettura  | Solo diritti di accesso in lettura.         |
| completi  | Diritti di accesso in lettura/scrittura.        |



 

## <a name="remarks"></a>Commenti

Una pagina Web deve prima richiedere all'utente l'autorizzazione per leggere o scrivere dati nella libreria. Ciò significa che determinati metodi, proprietà ed eventi non saranno accessibili dal codice se non sono stati concessi i diritti di accesso appropriati. Per ottenere i diritti di accesso, l'applicazione *chiama Impostazioni*. **requestMediaAccessRights**, passando un parametro che specifica il livello di diritti di accesso desiderato.

**Windows Media Player 10 Mobile:** questa proprietà restituisce sempre **full.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostazioni Oggetto**](settings-object.md)
</dt> <dt>

[**Impostazioni.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





