---
description: L'oggetto di Recording è una raccolta di oggetti record. Prima di fare riferimento alle relative proprietà, è necessario verificare che l'oggetto di registrazione esista e non sia vuoto.
ms.assetid: 7f5ac153-8da1-4dc8-9bb7-defd4e821142
title: Oggetto Recording
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b3f09887333d8ddbf83de4bea2b2e654411883e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330918"
---
# <a name="recordlist-object"></a>Oggetto Recording

L'oggetto di **Recording** è una raccolta di oggetti [**record**](record-object.md) . Prima di fare riferimento alle relative proprietà, è necessario verificare che l'oggetto di **registrazione** esista e non sia vuoto.

## <a name="members"></a>Membri

Questo tipo di membri è costituito dall'oggetto **Recorder** :

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

Le proprietà dell'oggetto di **Recording** .



| Proprietà                                     | Descrizione                                                          |
|:---------------------------------------------|:---------------------------------------------------------------------|
| [**Conteggio**](recordlist-count.md)<br/> | Restituisce il numero di elementi contenuti nell'oggetto di **registrazione** .<br/> |
| [**Elemento**](recordlist-item.md)<br/>   | Restituisce un record in una raccolta di oggetti di un oggetto di **registrazione** .<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecordList è definito come 000C1096-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Registra**](record-object.md)
</dt> <dt>

[Esempi di script di Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




