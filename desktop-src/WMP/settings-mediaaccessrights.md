---
title: Settings. mediaAccessRights
description: La proprietà mediaAccessRights recupera un valore che indica i diritti attualmente concessi per l'accesso alla libreria.
ms.assetid: 744e696d-29d2-44b1-a296-5b5d007b689f
keywords:
- Impostazioni. mediaAccessRights Windows Media Player
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
ms.openlocfilehash: 36bcfb667a1aa09e84ae90324736291d421a3941
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327381"
---
# <a name="settingsmediaaccessrights"></a>Settings. mediaAccessRights

La proprietà **mediaAccessRights** recupera un valore che indica i diritti attualmente concessi per l'accesso alla libreria.

## <a name="syntax"></a>Sintassi

Player. Settings. mediaAccessRights

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di sola lettura.



| Valore | Descrizione                      |
|-------|----------------------------------|
| Nessuno  | Solo diritti di accesso agli elementi correnti. |
| lettura  | Solo diritti di accesso in lettura.         |
| completi  | Diritti di accesso in lettura/scrittura.        |



 

## <a name="remarks"></a>Commenti

Una pagina Web deve prima richiedere all'utente l'autorizzazione per la lettura o la scrittura di dati nella libreria. Ciò significa che determinati metodi, proprietà ed eventi saranno inaccessibili dal codice se non sono stati concessi i diritti di accesso appropriati. Per ottenere i diritti di accesso, l'applicazione chiama *le impostazioni*. **requestMediaAccessRights**, passando un parametro che specifica il livello di diritti di accesso desiderato.

**Windows Media Player 10 Mobile**: questa proprietà restituisce sempre **full**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto Settings**](settings-object.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





