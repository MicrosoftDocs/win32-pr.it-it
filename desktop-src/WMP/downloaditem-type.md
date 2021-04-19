---
title: DownloadItem. Type
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. La proprietà Type recupera il tipo di download.
ms.assetid: 58ffb8a3-5410-492b-bb0f-9130ed209b78
keywords:
- DownloadItem. Type Media Player Windows
topic_type:
- apiref
api_name:
- DownloadItem.type
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cdcf21ce7443d7730d4a75518fb4749af0b9e52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326022"
---
# <a name="downloaditemtype"></a>DownloadItem. Type

> [!Note]  
> In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

La proprietà **Type** Recupera il tipo di download.

## <a name="syntax"></a>Sintassi

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).item(
        itemId
        ).type
      
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di sola lettura contenente uno dei valori seguenti.



| Valore      | Descrizione                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| background | (Solo Windows XP). Il download viene eseguito come processo in background, in quanto il tempo del processore diventa disponibile. Gli Stati di download vengono mantenuti anche quando Windows Media Player o Windows XP viene arrestato. |
| tempo reale  | (Tutti i sistemi operativi supportati). Il download viene eseguito in una sola volta. Nessun stato di download viene mantenuto tra le sessioni.                                                                       |



 

## <a name="remarks"></a>Commenti

Ogni tipo di download presenta vantaggi e svantaggi. Il download in background consente all'utente di passare ad altre attività e persino di riavviare Windows senza annullare il download, ma richiede più tempo per completare il download ed è supportato solo per Windows XP. Il download in tempo reale richiede meno tempo, ma richiede che l'utente completi tutti i download prima di chiudere Windows Media Player.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





